# Role Prompting

> **Navigation**: `Prompt Patterns` | [Chain of Thought](chain_of_thought.md) | [Few-Shot Learning](few_shot.md) | Role Prompting | [Format Control](format_control.md)
> 
> **Previous**: [Few-Shot Learning](few_shot.md) | **Next**: [Format Control](format_control.md)
> 
> **Related**: [Context Management](../fundamentals/context_management.md) | [Mental Models](../fundamentals/mental_models.md) | [Limitations](../fundamentals/limitations.md)

## Quick Summary
**For beginners**: This document shows how to get better responses by directing AI to adopt a specific expert perspective, like "analyze this code from a security expert's viewpoint" or "respond with UX design considerations."

**For practitioners**: A framework for human-directed role engineering that leverages persona design, expertise framing, and domain-specific behavior to guide AI responses toward specific knowledge domains and reasoning patterns.

**Key takeaway**: Role prompting, when properly directed by human expertise, can improve AI responses by activating domain-specific knowledge patterns. The right role framing, combined with human oversight, helps AI apply relevant expertise to specific problems.

---

# Role Prompting Framework

## Mechanism & Effectiveness
| Role Category | Cognitive Function | Implementation Strategy | Performance Impact |
|---------------|-------------------|-------------------------|-------------------|
| **Domain Expert** | Knowledge activation + specialized terminology access | Specific credentials + experience markers + domain-specific language | Accuracy in specialized domains, terminology precision, conceptual depth |
| **Process Guide** | Procedural framework activation + methodological constraints | Process identification + step sequencing + quality criteria | Structured outputs, comprehensive coverage, methodical approach |
| **Perspective Holder** | Viewpoint framing + value system alignment | Identity markers + value indicators + contextual positioning | Novel insights, balanced analysis, contextually appropriate framing |
| **Creative Archetype** | Style modeling + genre constraints | Stylistic exemplars + format conventions + creative parameters | Consistent tone, genre adherence, aesthetic alignment |
| **System Component** | Function-bound behavior + interface constraints | Capability boundaries + input/output specifications + interaction patterns | Predictable responses, specialized functionality, reduced hallucination |

## Implementation Framework

### Role Construction Components
```
1. Identity establishment: [role title] + [expertise level] + [experience quantification]

2. Knowledge domain specification:
   - Core expertise: [primary domain knowledge]
   - Auxiliary knowledge: [supporting knowledge areas]
   - Methodological approach: [how the role processes information]

3. Behavioral parameters:
   - Communication style: [linguistic markers + formality level + terminology density]
   - Decision framework: [evaluation criteria + prioritization framework + constraint handling]
   - Interaction pattern: [response structure + dialogue approach + collaboration mode]

4. Context integration:
   - Situational awareness: [relevant contextual factors to consider]
   - Task alignment: [specific role contribution to the current objective]
   - Boundary conditions: [scope limitations + ethical constraints + uncertainty handling]
```

### Role-Task Alignment Matrix
| Task Type | Optimal Role Category | Implementation Example |
|-----------|------------------------|------------------------|
| **Technical explanation** | Field-specific expert with teaching experience | `{senior engineer} + {15+ years experience} + {specialization} + {teaching background}` |
| **Process development** | Methodology specialist with implementation history | `{process consultant} + {framework expertise} + {implementation experience} + {adaptation capability}` |
| **Creative content** | Genre practitioner with stylistic specificity | `{creative professional} + {genre specialist} + {stylistic tradition} + {audience awareness}` |
| **Critical analysis** | Multi-perspective evaluator with methodical approach | `{analytical role} + {evaluation framework} + {balanced perspective} + {structured methodology}` |
| **Decision guidance** | Domain-specific advisor with risk assessment capability | `{advisory position} + {decision framework} + {risk evaluation} + {outcome optimization}` |

## Advanced Techniques

### Human-Directed Role Orchestration
- **Human-guided role transition**: `[human selects initial analysis role] → [human reviews and selects synthesis role] → [human identifies critique perspective]`
- **Complementary human-AI perspectives**: `[human expertise: domain knowledge] + [AI role: systematic processing]`
- **Human-moderated perspective exploration**: `[human identifies position] ↔ [AI explores counterposition] → [human synthesizes insights]`

### Human-Centered Role Direction Strategies
- **Expertise-guided role selection**: Apply human domain knowledge to identify most appropriate expert roles
- **Effectiveness evaluation**: Assess response quality against human expert standards
- **Adaptive refinement**: Iteratively adjust role framing based on output evaluation
- **Complementary expertise**: Identify areas where human expertise differs from typical AI knowledge
- **Critical evaluation framework**: Apply domain-specific criteria to verify output correctness
- **Credential specificity**: Replace "expert" with specific, verifiable credentials matching the human's needs
- **Experience quantification**: Specify relevant experience aligned with the human's objectives
- **Methodological anchoring**: Reference methodologies that align with human objectives
- **Value system articulation**: Define principles that reflect human priorities and ethical standards

## Collaborative Implementation Example
```
# Human-AI Collaborative Systems Architecture Review

## Human Role (Architecture Team Lead)
As the Architecture Team Lead, I will:
- Provide system requirements and business context
- Review and validate architectural recommendations
- Make final decisions on trade-offs and implementation priorities
- Apply organizational knowledge and constraints
- Evaluate recommendations for alignment with business goals

## AI Support Role (Systems Architecture Advisor)
I need you to analyze our system design from the perspective of a Systems Architecture Advisor with:
- Experience designing distributed systems at scale
- Knowledge of fault-tolerant microservice architectures
- Familiarity with cloud architecture patterns
- Understanding of service mesh implementation patterns
- Experience with legacy-to-microservice transitions

When analyzing the system design I'll share:
1. First assess overall architectural soundness based on industry standards
2. Identify potential scalability bottlenecks 
3. Evaluate fault-tolerance mechanisms
4. Suggest specific improvements with implementation considerations
5. Highlight trade-offs in your recommended approach

Present your analysis as a structured architecture review document with clear sections and recommendations. I will evaluate each recommendation based on our specific business context and implementation constraints.

## Review Process
1. I'll share our current architecture diagram and requirements
2. You'll provide initial analysis following the structure above
3. I'll ask clarifying questions and provide additional context
4. We'll collaboratively refine recommendations
5. I'll make implementation decisions based on our discussion 