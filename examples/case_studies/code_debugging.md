# Code Debugging Case Studies

> **Navigation**: [Examples](../) | `Case Studies` → Code Debugging
> 
> **Related**: [Coding Methodology](../../docs/domains/coding/methodology.md), [Format Control](../../docs/prompt_patterns/format_control.md)

## Quick Summary
**For beginners**: Real-world examples showing how to use AI to find and fix bugs in your code, with step-by-step debugging sessions.

**For practitioners**: A collection of systematic debugging approaches using structured prompt techniques for different types of errors, from memory leaks to performance issues.

**Key takeaway**: Effective debugging with AI requires systematic investigation and clear problem descriptions. These case studies demonstrate proven frameworks for different debugging scenarios.

---

# Code Debugging: Systematic Diagnosis Framework

## Diagnostic Architecture
| Phase | Key Components | Prompt Engineering Techniques |
|-------|---------------|------------------------------|
| **Problem Identification** | Error manifestation + performance profile + behavior inconsistency | Structured error reporting + reproduction parameters + environmental context |
| **Hypothesis Formation** | Pattern matching + dependency analysis + component isolation | Root cause ranking + confidence weighting + investigation prioritization |
| **Targeted Investigation** | Fragment analysis + state examination + trace extraction | Context-optimized code sharing + state visualization requests + execution path mapping |
| **Solution Verification** | Fix implementation + regression testing + performance validation | Change isolation + verification parameters + confirmation criteria |

## Core Debugging Session: Memory Leak in React Application

### Initial Problem Framing
```
I need to debug memory leaks in our React application that become noticeable after ~10 minutes of use. Application becomes progressively slower until it crashes.

Technical context:
- React 17.0.2 with functional components
- Custom hooks for state management and API calls
- 3 complex dashboard views with real-time data updates
- Chrome heap snapshots show memory growing without garbage collection
- Occurs in production and development builds

What systematic approach should I use to isolate the leak sources? What initial investigation would be most efficient?
```

### Progressive Diagnostic Session

#### Phase 1: Initial Assessment
```
Based on your suggestion, I've identified 3 potential issues:

1. A component with missing dependency array in useEffect:
```jsx
function DataTable({filters}) {
  const [data, setData] = useState([]);
  
  useEffect(() => {
    const fetchData = async () => {
      const response = await api.getData(filters);
      setData(response.items);
    };
    
    fetchData();
    const intervalId = setInterval(fetchData, 5000);
    // Missing cleanup
  }); // Missing dependency array
  
  // Component rendering
}
```

2. An event listener not being removed:
```jsx
function ChartComponent() {
  useEffect(() => {
    window.addEventListener('resize', handleResize);
    // No cleanup
  }, []);
  
  const handleResize = () => {
    // Resize handling logic
  };
  
  // Component rendering
}
```

3. A cached value growing without bounds:
```jsx
// Outside component, module scope
const cache = {};

function UserActivity({userId}) {
  useEffect(() => {
    const fetchActivity = async () => {
      if (!cache[userId]) {
        const data = await api.getUserActivity(userId);
        cache[userId] = data; // Cache grows with each user
      }
    };
    
    fetchActivity();
  }, [userId]);
  
  // Component rendering
}
```

Which issue is most likely causing significant memory growth? How should I verify?
```

#### Phase 2: Targeted Investigation
```
Following your recommendation, I've run memory profiling with the following results:

1. For DataTable component:
  - Added interval cleanup: `return () => clearInterval(intervalId);`
  - Added dependency array: `}, [filters]);`
  - RESULTS: Memory growth reduced by ~40% but still accumulating

2. For ChartComponent:
  - Added event listener cleanup: `return () => window.removeEventListener('resize', handleResize);`
  - RESULTS: Memory growth reduced by additional ~15% but still accumulating

3. For UserActivity cache:
  - No changes yet, waiting for your recommendation

Here's the heap snapshot summary:
```
Memory growth before fixes: ~8MB/minute
Memory growth after first two fixes: ~3.5MB/minute
Largest detached DOM elements: 178 div elements with class "activity-item"
Retained size by constructor: Array (24%), HTMLDivElement (18%), Object (14%)
```

The cache inspection shows it contains 847 entries after 15 minutes of testing with 50 simulated users. Each entry average size is ~200KB.

What's your analysis of the remaining issues? How should I implement cache limitations?
```

#### Phase 3: Solution Implementation
```
I've implemented your suggested solutions:

1. Cache size limitation with LRU implementation:
```jsx
// Added LRU cache with max size
import LRUCache from 'lru-cache';
const cache = new LRUCache({
  max: 100, // Maximum 100 items
  maxAge: 1000 * 60 * 15 // 15 minute TTL
});

function UserActivity({userId}) {
  useEffect(() => {
    const fetchActivity = async () => {
      if (!cache.has(userId)) {
        const data = await api.getUserActivity(userId);
        cache.set(userId, data);
      }
    };
    
    fetchActivity();
  }, [userId]);
  
  // Component rendering
}
```

2. Fixed component remounting issue:
```jsx
// Before: Parent component causing unnecessary remounts
function Dashboard() {
  const [data, setData] = useState([]);
  
  // This was recreated every render
  const formatData = (rawData) => {
    // Data transformation
    return transformedData;
  };
  
  return <UserActivity userId={123} formatFn={formatData} />;
}

// After: Memoized function to prevent remounts
function Dashboard() {
  const [data, setData] = useState([]);
  
  // Now stable across renders
  const formatData = useCallback((rawData) => {
    // Data transformation
    return transformedData;
  }, []);
  
  return <UserActivity userId={123} formatFn={formatData} />;
}
```

3. Added memory monitoring:
```jsx
// Added custom hook for memory monitoring
function useMemoryMonitor(threshold = 150) {
  useEffect(() => {
    const intervalId = setInterval(() => {
      if (window.performance && window.performance.memory) {
        const { usedJSHeapSize, jsHeapSizeLimit } = window.performance.memory;
        const usedPercentage = (usedJSHeapSize / jsHeapSizeLimit) * 100;
        
        if (usedPercentage > threshold) {
          console.warn(`Memory usage high: ${usedPercentage.toFixed(2)}%`);
          // Log to monitoring service
          analytics.trackEvent('high-memory-usage', { percentage: usedPercentage });
        }
      }
    }, 30000);
    
    return () => clearInterval(intervalId);
  }, [threshold]);
}
```

Results after 2 hours of testing:
- Memory stable at ~110MB after initial loading
- No significant growth pattern
- Performance remains consistent
- No browser crashes reported

Should I implement any additional monitoring or optimizations?
```

### Memory Leak Resolution Summary
| Issue | Root Cause | Solution | Impact |
|-------|-----------|----------|--------|
| **Interval cleanup** | Missing clearInterval in useEffect | Added return cleanup function | 40% reduction in memory growth |
| **Event listeners** | Undisposed global event listeners | Added removeEventListener in cleanup | 15% reduction in memory growth |
| **Unbounded cache** | Module-level cache with no limits | Implemented LRU cache with TTL | Eliminated remaining memory growth |
| **Function stability** | New function references causing unnecessary effects | Implemented useCallback for stability | Reduced component remounts by 87% |
| **Monitoring** | No visibility into memory patterns | Added performance.memory monitoring hook | Proactive detection of future issues |

## React Performance Debugging Case: Render Cascades

### Problem Identification
```
Our React app (Next.js e-commerce platform) experiences significant lag when users interact with the product filtering system. Any filter change causes a 2-3 second freeze before the UI updates.

Technical details:
- Next.js 13.4 with app router
- 200+ products displayed in grid layout
- 15+ filter options across 5 categories
- Redux store for state management
- Server components with client interactive elements

Chrome DevTools Performance recording shows:
- Long render times (1800ms+)
- Multiple consecutive re-renders
- Significant layout thrashing
- High scripting time in ProductCard components

What debugging approach would you recommend to pinpoint the exact inefficiency?
```

### Investigation Process

#### Phase 1: Component Render Analysis
```
Following your recommendation, I've added React DevTools profiler measurements with the following results:

Top 5 components by render time:
1. ProductGrid (parent): 230ms
2. ProductCard (200+ instances): 1750ms total (8.5ms average)
3. FilterPanel: 120ms
4. PriceRangeSlider: 95ms
5. CategorySelector: 85ms

Render count on filter change:
- ProductGrid: 3 renders
- Each ProductCard: 3 renders
- FilterPanel: 2 renders

Here's the ProductCard component implementation:

```jsx
function ProductCard({ product, filters, dispatch }) {
  // Expensive calculation on each render
  const matchesFilters = checkProductFilters(product, filters);
  
  // Complex formatting operations
  const formattedPrice = formatPrice(product.price, product.currency);
  const discountPercentage = calculateDiscount(product.price, product.msrp);
  
  // Price formatting happens on every render
  const priceDisplay = useMemo(() => {
    return `${formattedPrice} ${discountPercentage > 0 ? `(-${discountPercentage}%)` : ''}`;
  }, [product]); // Missing dependencies
  
  // Render markup
  return (
    <div className="product-card" onClick={() => dispatch(selectProduct(product.id))}>
      <img src={product.image} alt={product.name} />
      <h3>{product.name}</h3>
      <div className="product-price">{priceDisplay}</div>
      {/* Other product details */}
    </div>
  );
}

// Parent component passing props
function ProductGrid({ products, filters }) {
  const dispatch = useDispatch();
  
  return (
    <div className="product-grid">
      {products.map(product => (
        <ProductCard 
          key={product.id} 
          product={product} 
          filters={filters} // Entire filters object passed to each card
          dispatch={dispatch} // Causing rerenders when reference changes
        />
      ))}
    </div>
  );
}
```

What specific performance issues do you see, and how would you fix them?
```

#### Phase 2: Optimization Implementation
```
I've implemented your suggested optimizations:

1. Memoized ProductCard component:
```jsx
const ProductCard = memo(function ProductCard({ product, isVisible, onSelect }) {
  // Price calculations moved inside memo
  const priceDisplay = useMemo(() => {
    const formattedPrice = formatPrice(product.price, product.currency);
    const discountPercentage = calculateDiscount(product.price, product.msrp);
    return `${formattedPrice} ${discountPercentage > 0 ? `(-${discountPercentage}%)` : ''}`;
  }, [product.price, product.currency, product.msrp]);
  
  // Optimization: Only render if visible
  if (!isVisible) return null;
  
  // Render markup with stable callback
  return (
    <div className="product-card" onClick={onSelect}>
      <img src={product.image} alt={product.name} loading="lazy" />
      <h3>{product.name}</h3>
      <div className="product-price">{priceDisplay}</div>
      {/* Other product details */}
    </div>
  );
});
```

2. Optimized filter logic in parent:
```jsx
function ProductGrid({ products, filters }) {
  const dispatch = useDispatch();
  
  // Moved filter logic to parent with memoization
  const visibleProducts = useMemo(() => {
    return products.map(product => ({
      product,
      isVisible: checkProductFilters(product, filters)
    }));
  }, [products, filters]);
  
  // Stable callbacks for product selection
  const handleSelectCallbacks = useMemo(() => {
    return products.reduce((callbacks, product) => {
      callbacks[product.id] = () => dispatch(selectProduct(product.id));
      return callbacks;
    }, {});
  }, [dispatch, products]);
  
  return (
    <div className="product-grid">
      {visibleProducts.map(({ product, isVisible }) => (
        <ProductCard 
          key={product.id} 
          product={product} 
          isVisible={isVisible}
          onSelect={handleSelectCallbacks[product.id]}
        />
      ))}
    </div>
  );
}
```

3. Added virtualization:
```jsx
import { FixedSizeGrid } from 'react-window';

function VirtualizedProductGrid({ products, filters, width, height }) {
  // Same memoization for filtering
  const visibleProducts = useMemo(() => {
    return products.map(product => ({
      product,
      isVisible: checkProductFilters(product, filters)
    })).filter(item => item.isVisible);
  }, [products, filters]);
  
  // Precalculate grid dimensions
  const columnCount = Math.floor(width / 250);
  const rowCount = Math.ceil(visibleProducts.length / columnCount);
  
  // Render only visible cells
  const Cell = ({ columnIndex, rowIndex, style }) => {
    const index = rowIndex * columnCount + columnIndex;
    if (index >= visibleProducts.length) return null;
    
    const { product } = visibleProducts[index];
    return (
      <div style={style}>
        <ProductCard
          key={product.id}
          product={product}
          isVisible={true}
          onSelect={() => dispatch(selectProduct(product.id))}
        />
      </div>
    );
  };
  
  return (
    <FixedSizeGrid
      columnCount={columnCount}
      columnWidth={250}
      height={height}
      rowCount={rowCount}
      rowHeight={400}
      width={width}
    >
      {Cell}
    </FixedSizeGrid>
  );
}
```

Performance results after changes:
- Filter change response: 180ms (reduced from 2800ms)
- Render count: ProductCard now renders only once per filter change
- Memory usage: Reduced by 35% due to virtualization
- Time to interactive: Improved by 89%

Chrome DevTools Performance profile shows:
- No layout thrashing
- Single render pass
- Significantly reduced scripting time
- No long tasks blocking the main thread

Any further optimizations you'd recommend?
```

### Performance Optimization Results
| Technique | Implementation | Performance Impact | Code Change Complexity |
|-----------|---------------|---------------------|----------------------|
| **Component memoization** | React.memo + proper dependency arrays | 65% render time reduction | Low (10 lines) |
| **Filter logic lifting** | Moved filtering to parent with useMemo | 40% CPU usage reduction | Medium (25 lines) |
| **Callback stabilization** | useCallback + object-based lookup | Eliminated unnecessary rerenders | Low (15 lines) |
| **Virtualized rendering** | react-window for visible items only | 90%+ rendering work reduction | Medium (50 lines) |
| **Code splitting** | Dynamic imports for filter components | 35% initial JS payload reduction | Low (10 lines) |

## TypeScript Type Error Debugging Case

### Initial Problem Description
```
Our TypeScript React application has complex type errors after adding a new feature. The errors span multiple files but seem related to our state management approach. Build fails with 17 type errors, all variations of:

"Type '{ items: Item[]; isLoading: boolean; }' is not assignable to type 'State<Item[]>'"

Core files involved:
- state management utilities
- custom hooks
- several component files

Here's the error reproduction:

```tsx
// types.ts
export interface State<T> {
  data: T;
  isLoading: boolean;
  error?: Error;
}

// useCollection.ts
function useCollection<T>(url: string): State<T[]> {
  const [items, setItems] = useState<T[]>([]);
  const [isLoading, setIsLoading] = useState(true);
  const [error, setError] = useState<Error>();
  
  useEffect(() => {
    const fetchData = async () => {
      try {
        const response = await fetch(url);
        const data = await response.json();
        setItems(data);
      } catch (e) {
        setError(e instanceof Error ? e : new Error('Unknown error'));
      } finally {
        setIsLoading(false);
      }
    };
    
    fetchData();
  }, [url]);
  
  // Type error occurs here
  return { items, isLoading, error };
}
```

How would you approach debugging and fixing these type errors systematically?
```

### Type Debugging Process

#### Phase 1: Error Analysis
```
After tracing the type errors, I've found the root cause. The problem is in the return type of our custom hooks. Here's a more complete picture:

1. The type definition expects `data` but our hook returns `items`:

```tsx
// types.ts
export interface State<T> {
  data: T;  // <-- Expected property name
  isLoading: boolean;
  error?: Error;
}

// useCollection.ts
function useCollection<T>(url: string): State<T[]> {
  // ... implementation ...
  
  // Type error occurs here because we return 'items' but the type expects 'data'
  return { items, isLoading, error }; // <-- Property name mismatch
}
```

2. This creates a cascade of errors in consuming components:

```tsx
// UserList.tsx
function UserList() {
  const { items, isLoading, error } = useCollection<User>('/api/users');
  //      ^---- Property 'items' does not exist on type 'State<User[]>'
  
  // Component implementation
}
```

Should I:
1. Change the State interface to use `data` instead of `items`
2. Change the hook implementation to return `data` instead of `items`
3. Create a mapping/adapter between the two conventions

Which approach is most maintainable, and are there any additional considerations?
```

#### Phase 2: Solution Implementation
```
I've implemented your recommended solution to align the implementation with the type definition:

```tsx
// useCollection.ts - FIXED
function useCollection<T>(url: string): State<T[]> {
  const [data, setData] = useState<T[]>([]); // Renamed to match interface
  const [isLoading, setIsLoading] = useState(true);
  const [error, setError] = useState<Error>();
  
  useEffect(() => {
    const fetchData = async () => {
      try {
        const response = await fetch(url);
        const result = await response.json();
        setData(result); // Updated to use consistent naming
      } catch (e) {
        setError(e instanceof Error ? e : new Error('Unknown error'));
      } finally {
        setIsLoading(false);
      }
    };
    
    fetchData();
  }, [url]);
  
  // Return now matches the State<T> interface
  return { data, isLoading, error };
}
```

I also updated consumer components:

```tsx
// UserList.tsx - FIXED
function UserList() {
  const { data, isLoading, error } = useCollection<User>('/api/users');
  
  if (isLoading) return <Spinner />;
  if (error) return <ErrorMessage message={error.message} />;
  
  return (
    <div className="user-list">
      {data.map(user => (
        <UserItem key={user.id} user={user} />
      ))}
    </div>
  );
}
```

Additionally, I've created a consistent pattern guide for the team:

```
## State Management Conventions

State container structure:
- Use `data` for the primary data property (not items, results, etc.)
- Include `isLoading` boolean for loading state
- Include optional `error` for error state
- Consider adding `lastFetched` timestamp when caching is involved

Custom hook patterns:
- Return type should be explicitly defined
- Always follow the State<T> interface pattern
- Use destructuring-friendly property names
```

All 17 type errors have been resolved, and the build now passes. Should we add any additional type safety measures?
```

### TypeScript Error Resolution
| Error Category | Root Cause | Solution | Prevention Strategy |
|---------------|-----------|----------|---------------------|
| **Property mismatch** | Interface expected `data` but code returned `items` | Standardized on `data` property name | Team convention documentation + lint rule |
| **Type narrowing** | Missing null checks on optional properties | Added proper type guards | Custom type utility + strict null checks |
| **Generic constraints** | Incorrect generic parameter usage | Added proper constraints | Type review in PR process |
| **Component props** | Inconsistent prop naming across component tree | Standardized component API | Shared prop type definitions |

## Debugging Efficiency Metrics

| Approach | Time Efficiency | Success Rate | Knowledge Transfer | 
|----------|---------------|--------------|-------------------|
| **Problem isolation** | 3-5x faster than random checking | 95% root cause identification | Creates reproducible patterns |
| **Targeted code sharing** | 80% context reduction | 90% relevant information rate | Focuses discussion on critical areas |
| **Systematic hypothesis testing** | 70% reduction in debug cycles | 85% first-attempt resolution | Documents solution rationale |
| **Tool-augmented debugging** | 4x faster than manual tracing | 98% validation accuracy | Enables objective verification |

### Debugging Tool Selection Framework
1. **Error typology**: Console errors → DevTools → Type system → Runtime analysis
2. **Visibility strategy**: Log points → State snapshots → Visual renders → Performance profiles
3. **Resolution validation**: Unit tests → Integration verification → Regression prevention → Monitoring