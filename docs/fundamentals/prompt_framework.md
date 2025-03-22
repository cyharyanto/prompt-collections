# The P.R.O.M.P.T Framework

> **Navigation**: [Fundamentals](../fundamentals) / [P.R.O.M.P.T Framework](./prompt_framework.md)
> 
> **Previous**: [Mental Models](./mental_models.md) | **Next**: [Context Management](./context_management.md)
> 
> **Related**: [Evaluation](./evaluation.md), [Chain of Thought](../prompt_patterns/chain_of_thought.md)

## Quick Summary
**For beginners**: Six-component system for designing effective prompts: Purpose (clear goals), Reference (necessary context), Organization (logical structure), Model (LLM-specific optimization), Precision (unambiguous language), and Testing (systematic improvement).

**For practitioners**: Comprehensive prompt engineering methodology addressing the full lifecycle from intent definition to iteration, with specific implementation patterns for each component and cross-component interactions.

**Key takeaway**: Systematic prompt design through the P.R.O.M.P.T framework consistently outperforms ad-hoc approaches by addressing all critical elements of effective LLM interaction.

---

# P.R.O.M.P.T Framework Matrix

| Component | Core Function | Implementation Techniques | Common Failure Modes | Optimization Approaches |
|-----------|---------------|---------------------------|----------------------|-------------------------|
| **Purpose** | Define clear objectives and success criteria | Explicit task definition + Success metrics + Scope boundaries + Output requirements | Vague goals + Missing success criteria + Scope creep + Undefined audience | Task clarification matrices + Success metric specification + Scope limitation statements + User persona definition |
| **Reference** | Provide relevant context and examples | Background information + Exemplars + Constraints + Domain knowledge + Previous attempts | Insufficient context + Irrelevant details + Missing examples + Omitted constraints | Informationally-dense context + Few-shot examples + Explicit constraint listing + Domain terminology inclusion |
| **Organization** | Structure information logically and prioritize | Sequential ordering + Hierarchical structuring + Priority positioning + Categorical grouping + Visual formatting | Middle-content dilution + Logical inconsistency + Priority inversion + Structural ambiguity | Attention-curve optimization + Hierarchical nesting + Beginning/end positioning + Delimiter usage + Explicit sectioning |
| **Model** | Leverage LLM capabilities and limitations | Parameter optimization + Capability alignment + Limitation awareness + Format adaptation + Training cutoff consideration | Capability overestimation + Ignorance of limitations + Training boundary issues + Parameter misalignment | Model-specific formatting + Capability-aligned requests + Limitation workarounds + Parameter tuning |
| **Precision** | Use specific, unambiguous language | Concrete terminology + Quantitative specifications + Term definition + Explicit constraints + Format directives | Ambiguous wording + Subjective language + Undefined terms + Implicit assumptions | Specific over general terms + Numeric specifications + Glossary inclusion + Constraint matrices + Format templates |
| **Test** | Iterate and refine based on outputs | Result evaluation + Failure analysis + Targeted adjustments + Version tracking + Comparative testing | Single-iteration acceptance + Non-specific feedback + Unfocused adjustments + No baseline comparison | Systematic evaluation protocols + Error categorization + Controlled variable testing + Version control + A/B testing |

# Component Implementation Guide

## 1. Purpose: Define clear objectives and success criteria

### Implementation Framework
```
PURPOSE = {Specific Task} + {Success Criteria} + {Scope Definition} + {Audience Specification}
```

### Application Template
```
Task: [Specific action required]
Success Criteria: [How to measure successful completion]
Scope: [What to include/exclude]
For: [Target audience and their needs]
```

### Before/After Transformation
Before (Vague Purpose):
```
Write about artificial intelligence.
```

After (Defined Purpose):
```
Create a 500-word explanation of how artificial intelligence is changing manufacturing for factory floor supervisors with no technical background. Success means readers understand how to identify potential AI applications in their workflows. Focus on practical applications, not technical details or future speculation.
```

### Purpose Component Decision Tree
1. Primary objective identification
   - Information retrieval → Format specification + Knowledge scope
   - Content creation → Style parameters + Quality metrics
   - Analysis/reasoning → Methodology specification + Conclusion format
   - Code generation → Function requirements + Performance criteria
2. Success criteria definition
   - Quantitative metrics (word count, metrics, timeframe)
   - Qualitative attributes (tone, style, structure)
   - Functional requirements (features, capabilities)
   - Target audience impact (understanding, action, response)

## 2. Reference: Provide relevant context and examples

### Reference Density Optimization
| Context Type | When to Include | Implementation Pattern | Example |
|--------------|-----------------|------------------------|---------|
| **Background Information** | Historical/factual context needed | Concise summaries with key facts | "Project background: 3-month-old React application with 15K daily users, PostgreSQL backend" |
| **Examples** | Format guidance or demonstrating quality | Canonically correct instances | "Example function: `calculateTotal(items) → {function body}` Follow this pattern." |
| **Constraints** | Limiting scope or adding requirements | Explicit boundary statements | "Must work in browsers supporting ES6+. Must not use jQuery." |
| **Domain Knowledge** | Specialized information models need | Terminology + relationships | "Our user system has three roles: Admin, Editor, Viewer. Admins can create/delete, Editors can modify, Viewers can only read." |
| **Previous Attempts** | When iterating solutions | Problem + attempt + result | "Previously tried using Redux but encountered performance issues with large state objects." |

### Implementation Pattern
```
REFERENCE = {Essential Background} + {Canonical Examples} + {Technical Constraints} + {Domain Specifics} + {Prior Approaches}
```

## 3. Organize: Structure information logically and prioritize

### Attention Optimization Map
Prioritize information based on the LLM attention curve:
```
[HIGH ATTENTION] Beginning of prompt (critical framing)
                 ↓
[LOWER ATTENTION] Middle of prompt (supporting details)
                 ↓
[HIGH ATTENTION] End of prompt (specific instructions)
```

### Organization Structures by Task Type

| Task Type | Optimal Structure | Implementation | Example Pattern |
|-----------|-------------------|----------------|-----------------|
| **Sequential Operations** | Chronological ordering + Step numbering + Dependency mapping | 1→2→3 flow with explicit transitions | "First, analyze X. Once complete, transform using Y. Finally, output Z." |
| **Hierarchical Information** | Semantic nesting + Category-subcategory grouping + Importance weighting | Tree structure with clear relationships | "Main task: subtask1, subtask2. For subtask1: step1a, step1b..." |
| **Comparative Analysis** | Dimension specification + Element juxtaposition + Criteria prioritization | Matrix mapping with explicit dimensions | "Compare options A/B across dimensions X/Y/Z, prioritizing dimension X." |
| **Reference Documentation** | Section demarcation + Content classification + Cross-reference linking | Semantic sectioning with clear boundaries | "SECTION: Background... SECTION: Requirements... See Background for terminology." |

### Implementation Pattern
```
ORGANIZATION = {Structural Framework} + {Priority Indicators} + {Relationship Mapping} + {Visual Formatting}
```

## 4. Model: Understand the LLM's capabilities and limitations

### Model-Specific Optimization Matrix
| Model Characteristic | Assessment Questions | Adaptation Strategy | Implementation Pattern |
|----------------------|----------------------|---------------------|------------------------|
| **Knowledge Boundary** | When was model trained? What domains are covered? | Provide missing information + Verify date-sensitive content | "As of 2023, the regulations stated X. The current 2025 regulation has changed to Y." |
| **Context Window** | How much context can model hold? Is task complexity appropriate? | Chunk information + Priority encoding + Efficient tokenization | "Context: [essential only]. Additional details available if needed." |
| **Reasoning Capability** | What reasoning depth can model handle? | Chain-of-thought guidance + Decomposed reasoning + Verification steps | "Think step by step. First identify variables, then calculate, then verify result." |
| **Output Formats** | What output structures does model handle well? | Format templates + Example outputs + Structure specification | "Output as JSON with fields: 'summary', 'analysis', 'recommendation'." |
| **Known Limitations** | What recurring issues affect this model? | Preventative constraints + Explicit workarounds + Self-verification instructions | "Verify all numeric calculations. Double-check that all 5 points are addressed." |

### Implementation Pattern
```
MODEL ALIGNMENT = {Capability Leverage} + {Limitation Mitigation} + {Format Optimization} + {Knowledge Boundary Management}
```

## 5. Precision: Use specific, unambiguous language

### Precision Enhancement Techniques
| Ambiguity Type | Detection Pattern | Resolution Strategy | Implementation Example |
|----------------|-------------------|---------------------|------------------------|
| **Terminology Ambiguity** | General terms with multiple interpretations | Domain-specific definitions + Term qualification | "Optimize performance (specifically: reduce database query time)" |
| **Scope Uncertainty** | Unclear boundaries of what to include/exclude | Explicit inclusion/exclusion statements | "Include only REST API endpoints. Exclude WebSocket handlers." |
| **Quantitative Vagueness** | Subjective quantity descriptors | Exact numeric specifications | "Provide exactly 3 examples, each between 50-75 words." |
| **Qualitative Ambiguity** | Subjective quality descriptors | Objective criteria + Examples | "High-quality code means: commented, error-handled, and following PEP 8." |
| **Format Ambiguity** | Unspecified structure or layout | Template provision + Structural markers | "Format as Markdown table with columns: Feature | Benefit | Implementation Time" |

### Implementation Pattern
```
PRECISION = {Specific Terminology} + {Boundary Definition} + {Quantitative Specification} + {Qualitative Criteria} + {Format Template}
```

## 6. Test: Iterate and refine based on outputs

### Systematic Iteration Protocol
1. **Baseline Establishment**
   - Initial prompt execution
   - Response quality assessment against purpose criteria
   - Success/failure point identification
   - Error type categorization

2. **Controlled Modification**
   - Single-variable adjustments
   - Component-focused changes
   - Progressive refinement
   - Variant comparison

3. **Performance Tracking**
   - Version documentation + Change rationale
   - Improvement metrics + Failure reduction
   - Effectiveness rating + Efficiency measurement
   - Pattern extraction + Reusability assessment

### Implementation Pattern
```
TEST = {Evaluation Criteria} + {Failure Analysis} + {Refinement Strategy} + {Version Control} + {Comparative Assessment}
```

# Integrated Implementation Matrix

| Task Type | Purpose Focus | Reference Priority | Organization Pattern | Model Adaptation | Precision Elements | Testing Approach |
|-----------|---------------|-------------------|----------------------|------------------|-------------------|------------------|
| **Creative Writing** | Audience, style, emotional impact | Examples, constraints, style guides | Narrative structure, theme organization | Temperature adjustment, creative capability leverage | Tone specification, style parameters | Engagement metrics, style consistency |
| **Technical Analysis** | Analysis scope, decision criteria | Domain context, technical parameters | Logical framework, evidence hierarchy | Reasoning capability, knowledge domains | Technical definitions, analysis boundaries | Accuracy verification, completeness check |
| **Code Generation** | Function requirements, standards | Language context, system constraints | Component architecture, dependency map | Coding strengths, documentation style | API specifications, edge cases | Functional testing, performance assessment |
| **Data Processing** | Transformation goals, output format | Data schema, processing context | Pipeline structure, validation steps | Data handling capacity, format capabilities | Field definitions, transformation rules | Output validation, edge case handling |
| **Decision Support** | Decision criteria, alternatives | Situation context, constraints | Evaluation framework, criteria weighting | Reasoning capability, objectivity | Parameter definitions, assumption listing | Decision validity, criteria coverage |

# Case Study: Bug Diagnosis and Fixing

## Initial Prompt → P.R.O.M.P.T-Enhanced Prompt → Result Comparison

### Initial Prompt
```
Fix this bug in my code.
```

### P.R.O.M.P.T-Enhanced Prompt
```
PURPOSE: Diagnose and fix a pagination bug in a React application where page numbers don't update when filtering results.

REFERENCE:
1. Bug: When filtering table data, page count stays based on unfiltered data count
2. Expected: Page count should reflect filtered data count
3. Component code:
```jsx
function Pagination({ totalItems, itemsPerPage, currentPage, onPageChange }) {
  const pageCount = Math.ceil(totalItems / itemsPerPage);
  const pages = Array.from({ length: pageCount }, (_, i) => i + 1);
  
  return (
    <div className="pagination">
      {pages.map(page => (
        <button 
          key={page} 
          className={page === currentPage ? 'active' : ''} 
          onClick={() => onPageChange(page)}
        >
          {page}
        </button>
      ))}
    </div>
  );
}
```
4. Parent component:
```jsx
function DataTable() {
  const [data, setData] = useState(originalData);
  const [filteredData, setFilteredData] = useState(originalData);
  const [currentPage, setCurrentPage] = useState(1);
  const [itemsPerPage] = useState(10);
  
  const handleFilter = (term) => {
    const filtered = data.filter(item => 
      item.name.toLowerCase().includes(term.toLowerCase())
    );
    setFilteredData(filtered);
  };
  
  return (
    <>
      <SearchBar onSearch={handleFilter} />
      <Table data={filteredData.slice(/* pagination logic */)} />
      <Pagination 
        totalItems={data.length} // BUG LOCATION
        itemsPerPage={itemsPerPage}
        currentPage={currentPage}
        onPageChange={setCurrentPage}
      />
    </>
  );
}
```

ORGANIZE:
1. First identify the bug source in the provided code
2. Explain why this causes the observed behavior
3. Provide the exact code fix
4. Explain how the fix resolves the issue

MODEL: Using React component knowledge and state management patterns.

PRECISION: Focus specifically on the pagination calculation bug. Provide the exact line to change with before/after code.

TEST: After implementing, verify by:
1. Filter to reduce visible items below one page length
2. Confirm page count reduces appropriately
3. Filter to zero results to confirm no pagination appears
```

### Result Effectiveness Comparison
| Quality Dimension | Initial Prompt | P.R.O.M.P.T-Enhanced Prompt |
|-------------------|----------------|------------------------------|
| **Problem Identification** | Undefined scope, no context | Precise bug definition, complete context |
| **Solution Accuracy** | Guesswork based on limited info | Direct targeting of actual issue |
| **Implementation Clarity** | Vague suggestions | Exact code change with explanation |
| **Verification Process** | None provided | Specific test cases for validation |
| **Learning Value** | Minimal explanation | Root cause analysis and prevention |

# Component Integration Optimization

The components form an integrated system with clear relationships:

## Interdependence Matrix
| Component | Provides To | Depends On |
|-----------|-------------|------------|
| **Purpose** | Context boundaries for Reference, priority framework for Organization, success metrics for Testing | Model capabilities, Testing feedback for refinement |
| **Reference** | Knowledge foundation for Precision, context for Model | Purpose scope, Organization structure |
| **Organization** | Attention optimization for all components, structure for Testing | Purpose priorities, Model attention patterns |
| **Model** | Capability framework for Precision, format guidance for Organization | Purpose requirements, Reference knowledge |
| **Precision** | Implementation specificity, evaluation criteria | Reference details, Model capabilities, Organization structure |
| **Testing** | Feedback for all components, improvement metrics | Purpose criteria, Precision specifications |

## Implementation Workflow
```
1. PURPOSE definition → 2. MODEL capability assessment → 3. REFERENCE assembly
   ↓                                                           ↓
6. TEST and iterate ← 5. PRECISION enhancement ← 4. ORGANIZATION structuring
```

# Integration with Prompt Patterns

| Pattern | P.R.O.M.P.T Integration Point | Implementation Approach |
|---------|-------------------------------|-------------------------|
| **Chain of Thought** | Purpose + Precision | Specify reasoning requirements, structure thinking steps |
| **Few-Shot Learning** | Reference + Organization | Provide exemplars in strategic locations, maintain consistent structure |
| **Role Prompting** | Model + Purpose | Align role with model capabilities, define role-specific success criteria |
| **Format Control** | Precision + Organization | Specify output structure, include templates and delimiters |

The P.R.O.M.P.T framework transforms ad-hoc prompt writing into systematic prompt engineering through structured component integration optimized for LLM interaction. Each task type has unique component emphasis patterns, but all benefit from comprehensive framework application.