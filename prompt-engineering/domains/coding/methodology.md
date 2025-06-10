# AI-Assisted Coding Methodology

> **Navigation**: [Fundamentals](../../fundamentals/) | [Prompt Patterns](../../prompt_patterns/) | `Domains` → Coding → Methodology
> 
> **Previous**: [Domains](../) | **Next**: [Tailoring](tailoring.md)
> 
> **Related**: [Chain of Thought](../../prompt_patterns/chain_of_thought.md), [Format Control](../../prompt_patterns/format_control.md)

## Quick Summary
**For beginners**: This document shows you practical techniques for using AI to help with coding tasks, from generating code to debugging problems.

**For practitioners**: A comprehensive framework for effectively integrating AI into your development workflow, with specific prompt strategies for different coding scenarios.

**Key takeaway**: AI can help accelerate coding tasks when used strategically. This guide provides specific techniques for code generation, analysis, debugging, and optimization.

---

# A Systematic Approach to AI Code Analysis

Just as we have methodologies for code review, testing, and deployment, we need a systematic approach for working with AI code assistants. This methodology accounts for AI's fundamental characteristics: session-based memory, pattern-matching nature, and training-based understanding.

## Starting with Basics

Before diving into complex analysis, we need to establish foundational understanding with our AI assistant. Let's look at how this works in practice.

### Building Initial Context

Start with the simplest complete unit of code that demonstrates what you want to analyze:

```python
# Begin with core functionality
def process_order(order_id: str) -> Order:
    """Basic order processing implementation"""
    order = Order.get_by_id(order_id)
    if not order:
        raise OrderNotFoundError(order_id)
    return order

# Then add relevant context
ORDER_STATES = {
    'PENDING': 'Order received but not processed',
    'PROCESSING': 'Order is being handled',
    'COMPLETED': 'Order has been fulfilled'
}
```

Good Initial Questions:
1. "What can you see about the basic order processing flow?"
2. "What context might be missing for a complete understanding?"

This establishes a baseline before moving to more complex aspects.

### Progressive Context Building

As you confirm the AI's understanding, gradually add more context:

```python
# Add error handling patterns
def process_order(order_id: str) -> Order:
    try:
        order = Order.get_by_id(order_id)
        if not order:
            raise OrderNotFoundError(order_id)
        
        # Add business logic
        if order.status not in VALID_NEXT_STATES[order.status]:
            raise InvalidStateTransitionError(
                order.status, 
                VALID_NEXT_STATES[order.status]
            )
            
        return order
    except DatabaseError as e:
        logger.error(f"Database error processing order {order_id}: {e}")
        raise OrderProcessingError("Database error") from e
```

Now you can explore deeper questions:
- "How does this implementation handle different types of failures?"
- "What assumptions is it making about state transitions?"

## Working with Different Model Capabilities

Your methodology should adapt based on the AI model you're working with. Here's how:

### For Models with More Limited Context Windows

Consider breaking down analysis into focused sessions:

Session 1 - Basic Flow:
```python
# Focus on core logic first
def process_order(order_id: str) -> Order:
    """Discuss basic flow and error handling"""
```

Session 2 - State Management:
```python
# Focus on state transitions
VALID_NEXT_STATES = {
    'PENDING': ['PROCESSING'],
    'PROCESSING': ['COMPLETED', 'FAILED'],
    'COMPLETED': []
}
```

### For Models with Larger Context Windows

You might be able to provide more comprehensive context:

```python
# Consider including implementation with related components
class OrderProcessor:
    def __init__(self, db, logger, metrics):
        self.db = db
        self.logger = logger
        self.metrics = metrics
    
    def process_order(self, order_id: str) -> Order:
        """Full implementation"""
    
    def validate_state_transition(self, order: Order) -> bool:
        """State validation logic"""
    
    def handle_failure(self, order: Order, error: Exception) -> None:
        """Failure handling logic"""

# Plus tests and configuration
class TestOrderProcessor:
    """Test cases showing expected behavior"""
```

## Pattern Recognition and Novel Code

When working with familiar patterns, help the AI understand project-specific adaptations:

```python
# Standard repository pattern with custom additions
class OrderRepository:
    def get_by_id(self, order_id: str) -> Optional[Order]:
        # Standard implementation
        order = self.db.query(Order).filter_by(id=order_id).first()
        
        # Custom audit logging - explain this deviation
        if order:
            self.audit_logger.log_access(
                entity_type="Order",
                entity_id=order_id,
                access_type="read"
            )
        
        return order
```

When working with novel patterns, break them down into recognizable components:

```python
# Novel implementation broken down into familiar concepts
class CustomOrderProcessor:
    def process_with_retry(self, order_id: str) -> Order:
        """
        Custom processing with circuit breaker and back-pressure handling.
        Break it down into recognizable parts:
        1. Basic retry logic (familiar pattern)
        2. Circuit breaker state management
        3. Back-pressure calculations
        """
        # Implementation...
```

## Verification and Validation

Establish clear verification points throughout your analysis:

```python
class PaymentProcessor:
    def process_payment(self, payment: Payment) -> bool:
        """
        Verification points:
        1. Input validation ✓
        2. Payment gateway interaction ✓
        3. Error handling patterns ✓
        4. Need to verify: transaction rollback behavior
        5. Need to verify: audit logging requirements
        """
        # Implementation...
```

Create explicit checkpoints for understanding:

```python
# Checkpoint 1: Basic Flow
assert processor.can_process_payment(payment)

# Checkpoint 2: Error Handling
with pytest.raises(PaymentValidationError):
    processor.process_payment(invalid_payment)

# Checkpoint 3: Integration Points
# Verify interaction with external systems
```

## Documentation and Knowledge Capture

While AI assistants don't maintain context between sessions, we can use their analysis to improve our documentation:

```python
class OrderManager:
    """
    Order management system with custom workflow.
    
    Key insights from AI analysis:
    1. Non-standard state transitions need documentation
    2. Audit logging patterns differ from other modules
    3. Error handling has specific business requirements
    
    Implementation notes:
    - Uses optimistic locking for concurrent modifications
    - Implements custom retry logic for external service calls
    - Requires specific configuration for different environments
    """
```

## Continuous Improvement

Track effective patterns for working with AI:

```python
# Document successful interaction patterns
"""
Analysis Pattern Log:

Pattern: Component Breakdown
Effectiveness: High
Example: Breaking down custom retry logic into standard patterns
Result: Better understanding of novel implementations

Pattern: Progressive Context Building
Effectiveness: High
Example: Starting with core logic, then adding error handling
Result: More accurate analysis of complex systems
"""
```

## Adapting to Different Types of Code

Different types of code require different analytical approaches:

### Infrastructure Code
```python
# Focus on system boundaries and operational impact
class DatabaseConnectionPool:
    """
    Connection pool implementation.
    
    Key analysis points:
    1. Resource management patterns
    2. Error handling and recovery
    3. Monitoring integration
    4. Configuration management
    """
```

### Business Logic
```python
# Focus on requirements and domain rules
class OrderValidator:
    """
    Order validation with business rules.
    
    Key analysis points:
    1. Business rule implementation
    2. Validation sequences
    3. Error categorization
    4. Regulatory compliance
    """
```

### UI Components
```python
# Focus on user interaction and state management
class OrderForm extends Component:
    """
    Order entry form component.
    
    Key analysis points:
    1. State management
    2. User input handling
    3. Error presentation
    4. Accessibility requirements
    """
```

By following this methodology and adapting it to different scenarios, we can work more effectively with AI code assistants while accounting for their capabilities and limitations.
