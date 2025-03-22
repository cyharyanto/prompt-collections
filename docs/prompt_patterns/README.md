# Prompt Patterns

> **Navigation**: [Prompt Patterns](../prompt_patterns) / Overview
> 
> **Previous**: [Context Management](../fundamentals/context_management.md) | **Next**: [Chain of Thought](./chain_of_thought.md)
> 
> **Related**: [P.R.O.M.P.T Framework](../fundamentals/prompt_framework.md), [Evaluation](../fundamentals/evaluation.md)

## Quick Summary
**For beginners**: Standard prompt structures that consistently produce better results across different tasks, like recipes that give reliable outputs with minimal experimentation.

**For practitioners**: Systematic pattern taxonomy optimized for different task types, with documented tradeoffs in token efficiency, complexity, and model compatibility.

**Key takeaway**: Deliberate pattern application yields 30-70% quality improvement over ad-hoc prompting through structural optimization and constraint management.

---

# Prompt Pattern Classification Matrix

| Category | Core Mechanism | Strategic Intent | Implementation Complexity | Token Efficiency | Example Patterns |
|----------|----------------|------------------|---------------------------|------------------|------------------|
| **Trial-and-Error** | Iterative refinement + Output analysis + Progressive improvement | Output exploration + Boundary testing + Intuition development | Low initial/High cumulative | Variable (improves with iteration) | Prompt refinement + Error analysis + Progressive enhancement + A/B testing |
| **Goal-Oriented** | Process specification + Reasoning guidance + Step decomposition | Accuracy optimization + Reproducibility enhancement + Logic enforcement | Medium to High | Medium (additional instruction overhead) | [Chain of Thought](./chain_of_thought.md) + Self-consistency + Tree of thoughts + Process scaffolding |
| **Constraint-Focused** | Boundary definition + Format enforcement + Error prevention | Quality control + Consistency enhancement + Compliance assurance | Medium | High (explicit constraints reduce correction needs) | [Format Control](./format_control.md) + Boundary setting + Requirement specification + Guardrail implementation |

# Core Pattern Categories

## 1. Trial-and-Error Prompting
- **Framework**: Initial Hypothesis → Output Analysis → Targeted Revision → Comparative Evaluation → Pattern Extraction
- **Key Techniques**:
  - **Prompt Refinement**: Systematic adjustment based on output assessment
  - **Error Analysis**: Identifying specific failure points for improvement
  - **A/B Testing**: Comparing alternative structures for effectiveness
  - **Progressive Enhancement**: Incremental complexity addition based on success
- **Effectiveness**: 15-30% improvement per iteration, diminishing returns after 3-4 cycles

## 2. Goal-Oriented Prompting
- **Framework**: Outcome Definition + Process Specification + Step Decomposition + Verification Mechanism
- **Key Techniques**:
  - **Chain of Thought**: Explicit reasoning step guidance
  - **Self-Consistency**: Multiple solution path generation and verification
  - **Tree of Thoughts**: Multi-branch exploration with evaluation
  - **Process Scaffolding**: Explicit process framework provision
- **Effectiveness**: 50-70% improvement in analytical tasks, 30-40% higher reasoning accuracy

## 3. Constraint-Focused Prompting
- **Framework**: Boundary Definition + Format Specification + Requirement Enumeration + Error Prevention Rules
- **Key Techniques**:
  - **Format Control**: Output structure and organization enforcement
  - **Boundary Setting**: Explicit scope limitation to prevent drift
  - **Requirement Specification**: Mandatory element enumeration
  - **Guardrail Implementation**: Error prevention through explicit prohibitions
- **Effectiveness**: 60-80% reduction in format inconsistencies, 70-90% reduction in critical omissions

# Pattern Selection Guide

## Task-Based Selection Matrix
| Task Type | Primary Pattern | Secondary Pattern | Key Implementation Focus |
|-----------|----------------|-------------------|--------------------------|
| **Analysis/Reasoning** | Goal-Oriented | Constraint-Focused | Reasoning step specification + Output organization |
| **Creative Generation** | Trial-and-Error | Constraint-Focused | Progressive refinement + Boundary definition |
| **Factual Output** | Constraint-Focused | Goal-Oriented | Accuracy requirements + Verification steps |
| **Code Generation** | Goal-Oriented | Constraint-Focused | Implementation steps + Technical requirements |
| **Conversion/Translation** | Constraint-Focused | Trial-and-Error | Format specification + Quality refinement |

## Selection Factors
- **Task Characteristics**: Complexity, structure importance, exploration value, error sensitivity
- **Resource Considerations**: Available tokens, iteration time, quality requirements, reproducibility needs

## Implementation Strategy
- **Phased Approach**: Trial-and-Error → Goal-Oriented → Constraint-Focused → Composite patterns
- **Hybrid Pattern Structure**: {Constraint-Focused Boundaries} + {Goal-Oriented Process} + {Trial-and-Error Refinement}

# Pattern Documentation Index
- [Chain of Thought](./chain_of_thought.md): Explicit reasoning steps for complex problem-solving
- [Few-Shot Learning](./few_shot.md): Example-based learning for pattern replication
- [Role Prompting](./role_prompting.md): Expert framing for specialized knowledge access
- [Format Control](./format_control.md): Output structure enforcement for consistency