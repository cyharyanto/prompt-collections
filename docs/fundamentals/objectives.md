# Objective Framework for LLMs

> **Navigation**: `Fundamentals` | [Mental Models](mental_models.md) | [Limitations](limitations.md) | [Context Management](context_management.md) | Objectives
> 
> **Previous**: [Assumptions](assumptions.md) | **Next**: [Evaluation](evaluation.md)
> 
> **Related**: [Evaluation](evaluation.md), [Format Control](../prompt_patterns/format_control.md)

## Quick Summary
**For beginners**: This document helps you set clear goals and expectations when working with AI, so you get exactly what you need rather than vague responses.

**For practitioners**: A comprehensive framework for structuring AI objectives across different domains, with precise guidance on defining quality criteria, measurement approaches, and evaluation standards.

**Key takeaway**: Clear objectives dramatically improve AI outputs. This guide provides frameworks for specifying exactly what you want in terms of content, format, approach, and quality.

---

# LLM Objective Framework

## System Request Architecture
```
                      ┌───────────────────┐
                      │   Goal Definition │
                      └─────────┬─────────┘
                                │
                                ▼
┌───────────────┐     ┌───────────────────┐     ┌───────────────┐
│ Input Context │────▶│ Processing Intent │────▶│ Output Intent │
└───────────────┘     └───────────────────┘     └───────────────┘
                                │                       │
                                ▼                       ▼
                      ┌───────────────────┐     ┌───────────────┐
                      │ Quality Standards │     │ Delivery Mode │
                      └───────────────────┘     └───────────────┘
```

## Foundational Objective Matrix
| Objective Type | Core Components | Implementation Elements | Evaluation Criteria |
|----------------|----------------|-----------------------|---------------------|
| **Information Extraction** | Query specification + scope definition + precision requirements | Entity isolation + relationship mapping + confidence indicators | Accuracy (factual correctness) + recall (completeness) + relevance (alignment) |
| **Content Generation** | Output parameters + style specifications + functional requirements | Structure framework + tone calibration + purpose alignment | Coherence (logical flow) + adherence (requirement matching) + utility (fitness for purpose) |
| **Analytical Processing** | Question framing + evidence requirements + reasoning structure | Information assessment + inference construction + conclusion formation | Logical validity + evidential support + analytical depth + bias minimization |
| **Instructional Guidance** | Capability assessment + task decomposition + success criteria | Step sequencing + option presentation + verification guidance | Implementability + comprehensiveness + adaptation capability + error handling |

## Direct Observation Framework

### Observation Layer Architecture
1. **Direct Observation Layer**
   - Visible components: [explicitly seen code + examined structures + observed patterns]
   - Boundary markers: [visibility limits + context constraints + inaccessible elements]
   - Certainty indicators: [confidence level + evidence strength + verification status]

2. **Inference Architecture**
   - Pattern-based inferences: [recognized structures + common implementations + standard practices]
   - Relationship-based inferences: [component connections + dependency implications + architectural constraints]
   - Experience-based inferences: [training-derived knowledge + general principles + cross-project patterns]

3. **Knowledge Gap Framework**
   - Critical missing information: [required dependencies + essential context + necessary configurations]
   - Uncertainty zones: [ambiguous implementations + multiple interpretations + partial patterns]
   - Verification needs: [assumption checks + pattern confirmation + implementation validation]

### Communication Strategy Matrix
| Communication Mode | Implementation Pattern | Application Context | Quality Indicators |
|--------------------|------------------------|---------------------|-------------------|
| **Visibility Declaration** | Explicit boundary articulation + context limitation acknowledgment | Initial analysis, large codebases, complex systems | Self-awareness accuracy, contextual honesty, assumption avoidance |
| **Pattern Analysis** | Standard pattern identification + deviation highlighting + adaptation assessment | Architecture exploration, design evaluation, implementation review | Pattern accuracy, adaptation recognition, project-specific insight |
| **Relationship Analysis** | Component interaction mapping + dependency qualification + system impact assessment | Integration points, cross-module functionality, architectural decisions | Connection accuracy, interaction insight, system comprehension |
| **Certainty Calibration** | Confidence level expression + evidence sourcing + verification requesting | Critical functionality, security-sensitive code, complex algorithms | Uncertainty transparency, appropriate confidence, verification clarity |

## Measurement & Evaluation Framework

### Objective-Quality Mapping
| Objective Class | Primary Metrics | Secondary Metrics | Verification Methods |
|-----------------|----------------|------------------|---------------------|
| **Factual Extraction** | Accuracy rate + completeness percentage + error frequency | Source utilization + context relevance + inference minimization | Cross-source validation + expert verification + inconsistency analysis |
| **Creative Generation** | Relevance alignment + constraint adherence + coherence score | Novelty degree + adaptability range + stylistic consistency | Requirement comparison + output validation + purpose fulfillment |
| **Analytical Processing** | Logical validity + evidence incorporation + conclusion soundness | Consideration breadth + alternative accounting + limitation acknowledgment | Reasoning path examination + inference validation + counterexample testing |
| **Instructional Guidance** | Implementation success rate + error reduction + completion efficiency | Adaptability to contexts + scalability across instances + resilience to variations | Process implementation + outcome comparison + feedback incorporation |

### Quantitative Performance Metrics
| Metric Category | Implementation Measures | Quality Considerations | Potential Issues |
|-----------------|------------------------|-------------------|-------------------|
| **Accuracy Metrics** | Factual correctness + error rate + hallucination frequency | Aim for high factual alignment, minimal hallucinations, and low error rates | Watch for low factual accuracy, high hallucination rates, frequent errors |
| **Completion Metrics** | Requirement fulfillment + information coverage + omission rate | Try to address all requirements, include critical information, avoid important omissions | Be aware of missed requirements, insufficient coverage, critical omissions |
| **Coherence Metrics** | Logical consistency + structural integrity + flow cohesion | Strive for logical integrity, solid structure, and smooth flow | Check for logical inconsistencies, structural problems, flow disruptions |
| **Efficiency Metrics** | Token utilization + processing steps + rework requirements | Consider token efficiency, optimal process steps, minimal rework | Watch for poor token efficiency, excessive steps, high rework needs |

## Application Domains

### Software Development Framework
```
# Code Generation Objective Matrix

1. Functionality Requirements
   - Feature completeness: [core behavior + edge cases + failure modes]
   - Performance parameters: [execution efficiency + resource utilization + scaling behavior]
   - Integration specifications: [system interaction + API compatibility + dependency management]

2. Code Quality Standards
   - Structure coherence: [architectural patterns + component organization + module boundaries]
   - Implementation practices: [language idioms + optimization techniques + security patterns]
   - Maintainability factors: [readability conventions + documentation standards + testing approach]

3. Verification Framework
   - Functional validation: [core requirements + contract fulfillment + integration testing]
   - Error handling: [boundary testing + failure recovery + exception management]
   - Performance assessment: [resource consumption + execution profiling + bottleneck analysis]
```

### Content Creation Framework
```
# Content Generation Objective Framework

1. Content Purpose Specification
   - Primary goals: [information delivery + persuasion intent + entertainment value]
   - Target response: [cognitive outcome + emotional impact + action initiation]
   - Success criteria: [engagement metrics + comprehension indicators + response triggers]

2. Structural Parameters
   - Organization pattern: [logical flow + information hierarchy + transition framework]
   - Density calibration: [terminology concentration + concept-to-word ratio + example proportion]
   - Format requirements: [section organization + visual elements + reference framework]

3. Stylistic Guidelines
   - Voice characteristics: [formality level + technical density + personality indicators]
   - Rhetorical approach: [persuasive techniques + evidential standards + narrative elements]
   - Adaptation parameters: [audience calibration + context sensitivity + knowledge assumptions]
```

### Data Analysis Framework
```
# Analytical Processing Objective Framework

1. Investigation Parameters
   - Analysis scope: [dataset boundaries + temporal range + variable inclusion]
   - Exploration focus: [relationship examination + pattern identification + anomaly detection]
   - Insight priorities: [actionable findings + decision support + hypothesis evaluation]

2. Methodological Requirements
   - Analytical approach: [statistical techniques + modeling methods + visualization formats]
   - Validation standards: [confidence thresholds + error tolerance + assumption testing]
   - Interpretation framework: [significance assessment + limitation acknowledgment + alternative consideration]

3. Output Specifications
   - Finding presentation: [result prioritization + evidence inclusion + uncertainty communication]
   - Recommendation framework: [action orientation + implementation guidance + impact assessment]
   - Future direction: [additional investigation + methodology refinement + hypothesis generation]
```

### Educational Framework
```
# Learning Objective Framework

1. Knowledge Transfer Parameters
   - Conceptual coverage: [core principles + supporting details + practical applications]
   - Comprehension levels: [introductory explanation + intermediate depth + advanced nuance]
   - Connection framework: [prerequisite linking + interdisciplinary relationships + knowledge scaffolding]

2. Pedagogical Approach
   - Explanation methods: [conceptual models + concrete examples + analogy usage]
   - Engagement techniques: [question framing + interactive elements + reflection prompts]
   - Reinforcement strategies: [retrieval practice + application opportunities + extension challenges]

3. Assessment Components
   - Understanding verification: [concept checking + misunderstanding identification + knowledge application]
   - Progress indicators: [learning milestone tracking + competency assessment + mastery evidence]
   - Adaptation guidance: [difficulty adjustment + remediation suggestions + enhancement opportunities]
```

## Objective Implementation Architecture

### Requirement Specification Framework
```
# Specification Architecture

1. Purpose + Scope Definition
   - Primary goal: [explicit statement of core intent]
   - Outcome targets: [specific deliverables and artifacts]
   - Boundary conditions: [explicit scope limitations and exclusions]

2. Quality Dimensional Hierarchy
   - Primary quality dimensions: [critical attributes (accuracy, completeness, etc.)]
   - Secondary quality dimensions: [important but non-critical attributes]
   - Trade-off parameters: [explicit balancing instructions for competing qualities]

3. Format + Structure Definition
   - Organizational pattern: [hierarchical structure, flow, relationships]
   - Component requirements: [specific sections, elements, features]
   - Presentation parameters: [style, tone, density, technical level]
```

### Cross-Domain Translation Framework
| Primary Domain | Translation Techniques | Secondary Domain | Implementation Pattern |
|----------------|------------------------|-----------------|------------------------|
| **Software Engineering** | Requirement mapping + constraint translation + verification alignment | Education | Tutorial structure + incremental complexity + verification exercises |
| **Content Creation** | Purpose adaptation + structure modification + tone calibration | Technical Documentation | Implementation focus + precision increase + example specificity |
| **Data Analysis** | Goal reframing + methodology adaptation + output reformatting | Business Strategy | Decision framework + action orientation + implementation prioritization |
| **Academic Research** | Precision maintenance + evidence standards + certainty calibration | General Communication | Accessibility increase + example enrichment + terminology simplification |

### Example: Multi-Domain Objective Implementation

```
# DOMAIN: Software Engineering → Documentation

## Original Software Testing Objective
Create a test suite for the authentication module that:
- Verifies all API endpoints function according to specification
- Tests boundary conditions and error states
- Achieves >90% code coverage
- Includes performance benchmarks

## Translated Documentation Objective
Create comprehensive testing documentation that:
- Explains testing strategy for each authentication endpoint with examples
- Catalogues all boundary conditions and error states with expected behaviors
- Provides coverage analysis with rationale for uncovered sections
- Documents performance benchmarks with analysis methods and baselines

## Implementation Parameters
- Organization: Endpoint-by-endpoint with subsections for normal/boundary/error cases
- Code inclusion: Test code snippets paired with explanation
- Technical level: Appropriate for junior developers with testing fundamentals
- Visual elements: Coverage maps, performance graphs, test flow diagrams
```

## Evaluation Guidelines

### Success Evaluation Matrix
| Dimension | High Quality | Acceptable Quality | Needs Improvement |
|-----------|----------------------|---------------------|------------------------|
| **Requirement Fulfillment** | All critical and most secondary requirements addressed | All critical and many secondary requirements addressed | Missing critical or most secondary requirements |
| **Accuracy Standards** | Minimal errors with thorough verification | No critical errors with few minor errors | Contains critical errors or many minor errors |
| **Usability Metrics** | Readily actionable, self-sufficient, extensible | Actionable with minor clarification, mostly self-sufficient | Requires significant clarification, incomplete implementation |
| **Efficiency Factors** | Efficient resource use, straightforward implementation | Reasonable resource use, clear implementation | Excessive resource use, inefficient implementation |

### Scoring Framework
```
# Quality Evaluation System

1. Requirement Compliance [40%]
   - Critical requirements: [essential functionality + core constraints + primary outputs]
   - Extended requirements: [secondary features + optimization goals + enhancement requests]
   - Implicit requirements: [standard practices + typical expectations + conventional inclusions]

2. Implementation Quality [30%]
   - Technical correctness: [factual accuracy + functional validity + error avoidance]
   - Structural integrity: [organization logic + relationship coherence + flow optimization]
   - Adaptability characteristics: [modification ease + extension capacity + context flexibility]

3. Utility Assessment [30%]
   - Purpose fulfillment: [goal achievement + problem resolution + need satisfaction]
   - User experience: [clarity + accessibility + engagement factors]
   - Value delivery: [efficiency improvement + capability enhancement + knowledge transfer]
```

### Continuous Improvement Framework
| Feedback Source | Analysis Approach | Implementation Method | Success Indicators |
|-----------------|-------------------|---------------------|---------------------|
| **Requirement Gaps** | Pattern identification + root cause analysis + classification system | Specification template enhancement + pre-check validation + example enrichment | 50% reduction in specification-execution gaps per iteration |
| **Quality Issues** | Defect categorization + frequency analysis + severity assessment | Quality parameter refinement + verification enhancement + standard improvement | 40% reduction in same-category defects across iterations |
| **Efficiency Opportunities** | Process examination + comparative analysis + bottleneck identification | Workflow enhancement + template optimization + automation increase | 30% improvement in time-to-completion per major iteration |

## Advanced Implementation

### Objective Decomposition Framework
```
# Task Decomposition Architecture

1. Component Analysis
   - Functional units: [discrete components with specific purposes]
   - Dependency mapping: [prerequisite relationships + sequential dependencies]
   - Complexity assessment: [difficulty gradation + expertise requirements]

2. Process Sequencing
   - Critical path definition: [essential sequence + gate requirements]
   - Parallel opportunities: [independent components + concurrent possibilities]
   - Checkpoint establishment: [verification points + progress validation]

3. Resource Allocation
   - Effort distribution: [time allocation + attention focusing + complexity balancing]
   - Context management: [knowledge carryover + state maintenance + information accessibility]
   - Optimization targets: [efficiency priorities + quality focus points + enhancement opportunities]
```

### Multi-Agent Collaboration Model
| Agent Role | Responsibility Focus | Integration Points | Quality Assurance |
|------------|---------------------|-------------------|-------------------|
| **Requirement Manager** | Specification clarification + priority assignment + completeness verification | Output validation parameters + quality definition | Specification compliance + requirement traceability |
| **Solution Architect** | Structure design + approach selection + integration planning | Requirement mapping + implementation framework | Design coherence + pattern appropriateness |
| **Implementation Specialist** | Component development + detail refinement + technical optimization | Architecture alignment + specific requirements | Technical accuracy + efficiency optimization |
| **Quality Validator** | Verification execution + defect identification + improvement guidance | Implementation assessment + requirement alignment | Defect detection + improvement identification |

### Advanced Scoring System
```
# Comprehensive Evaluation Framework

1. Absolute Quality Metrics
   - Requirement fulfillment: [critical + secondary + implicit requirements]
   - Technical accuracy: [factual correctness + functional validity + error rate]
   - Usability factors: [clarity + accessibility + actionability]

2. Relative Performance Indicators
   - Comparative efficiency: [resource utilization vs. alternative approaches]
   - Innovation assessment: [novel techniques + creative solutions + pattern improvements]
   - Adaptability evaluation: [robustness across contexts + modification ease]

3. Impact Factors
   - Problem resolution: [issue elimination + challenge mitigation + obstacle navigation]
   - Capability enhancement: [skill development + knowledge transfer + tool provision]
   - Future readiness: [maintainability + extensibility + evolution capacity]
```
