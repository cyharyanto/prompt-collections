<!-- Navigation Guide -->
<!-- Previous: [Evaluation](../fundamentals/evaluation.md) | Next: [Few-Shot Learning](few_shot.md) -->
<!-- Path: [Fundamentals](../fundamentals/) → Prompt Patterns → Chain of Thought → [Few-Shot](few_shot.md) → [Role Prompting](role_prompting.md) -->
<!-- Related: [Context Management](../fundamentals/context_management.md) -->

# Chain-of-Thought Prompting Framework

## Mechanism Matrix
| Variant | Implementation | Application Context | Effectiveness Factors |
|---------|----------------|---------------------|----------------------|
| **Standard CoT** | Explicit reasoning request + step indicator | General problems requiring decomposition | Problem complexity, instruction clarity, step granularity |
| **Zero-shot CoT** | "Let's think step by step" trigger phrase | Novel problems without examples | Task familiarity to model, reasoning type match, problem structure |
| **Few-shot CoT** | 2-5 worked examples with visible reasoning | Complex/specialized domains | Example selection quality, progression design, similarity to target |
| **Self-consistency CoT** | Multiple reasoning paths + majority outcome | High-stakes decisions, verification needs | Sampling temperature, path diversity, aggregation method |

## Pattern Implementation

### Core Structure
```
1. Problem framing: [clear problem statement] + [context] + [constraints]
2. Reasoning instruction: [explicit reasoning request] + [granularity guidance]
3. Cognitive scaffolding: [decomposition strategy] + [intermediate verification points]
4. Output structure: [format requirements] + [precision expectations]
```

### Optimal Triggers
- **Direct instruction**: "Think through this step by step..."
- **Metacognitive framing**: "To solve this systematically, I should first..."
- **Process specification**: "Solve this by breaking it into the following steps: 1)..."
- **Workspace creation**: "Let me work through this problem: First,..."

## Application Optimization

### Mathematical Reasoning
| Problem Type | Decomposition Strategy | Example Implementation |
|--------------|------------------------|------------------------|
| Arithmetic | Value tracking + operation sequencing | "Identify values → apply operations in order → track running total" |
| Algebra | Variable isolation + constraint application | "Define variables → translate to equations → manipulate step-by-step → verify solution" |
| Probability | Event identification + rule application | "Define events → identify probability type → apply appropriate formula → check bounds" |
| Geometry | Property extraction + theorem mapping | "List given properties → identify applicable theorems → chain relationships → verify constraints" |

### Logical Analysis
| Task Type | CoT Structure | Critical Components |
|-----------|---------------|---------------------|
| Deduction | Premise evaluation → rule application → conclusion validation | Exhaustive premise identification, constraint tracking, contradiction checking |
| Classification | Feature extraction → criteria application → boundary evaluation | Systematic feature assessment, multi-criteria weighting, edge case analysis |
| Causality | Variable isolation → relationship mapping → confound elimination | Temporal sequencing, interaction identification, alternative explanation testing |
| Argument analysis | Claim identification → evidence assessment → logic verification | Assumption surfacing, validity testing, fallacy identification |

## Implementation Examples

### Problem-Solving Template
```
Problem: [complex problem statement]

I'll solve this step-by-step:

1. Understanding phase:
   - Key elements: [identify core components]
   - Relationships: [map connections between elements]
   - Constraints: [list boundaries/limitations]

2. Strategy selection:
   - Applicable methods: [identify relevant approaches]
   - Optimal approach: [select best method based on problem characteristics]

3. Execution:
   - Step 1: [specific operation with justification]
   - Step 2: [build on previous step with clear logic]
   - Step 3: [continue systematic progression]
   
4. Verification:
   - Solution check: [verify against original constraints]
   - Alternative validation: [test through different method if applicable]

Therefore, the solution is [final answer with confidence assessment].
``` 