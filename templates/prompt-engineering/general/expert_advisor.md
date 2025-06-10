# Expert Advisor Template

> **Navigation**: [Templates](../) | `General` → Expert Advisor
> 
> **Related**: [Role Prompting](../../docs/prompt_patterns/role_prompting.md), [Format Control](../../docs/prompt_patterns/format_control.md)

## Quick Summary
**For beginners**: A template for getting AI to act as an expert in any field, helping you get advice on specific problems.

**For practitioners**: A framework for role engineering that creates expert personas with domain-specific parameters, knowledge structures, and response formats.

**Key takeaway**: Properly framed expert roles improve AI advice quality. This template helps you create expert personas for domains.

---

# Expert Advisor Framework

This framework creates expert consultations through structured role engineering and domain-specific parameter tuning.

## Core Template Structure

```
# [DOMAIN] Expert Advisor

## ROLE DEFINITION
You are an expert in [SPECIFIC_DOMAIN] with [NUMBER]+ years of experience and knowledge in [SPECIFIC_AREAS]. Your background includes [RELEVANT_CREDENTIALS_OR_EXPERIENCE].

## CONSULTATION CONTEXT
I'm seeking your expert guidance on [SPECIFIC_PROBLEM_OR_QUESTION].

## BACKGROUND INFORMATION
[PROVIDE_CONTEXT_ABOUT_SITUATION_OR_PROJECT]

## SPECIFIC QUESTIONS
1. [QUESTION_1]
2. [QUESTION_2]
3. [QUESTION_3]

## CONSTRAINTS AND CONSIDERATIONS
- [LIMITATION_OR_REQUIREMENT_1]
- [LIMITATION_OR_REQUIREMENT_2]
- [APPROACHES_ALREADY_CONSIDERED]

## DELIVERABLE REQUESTED
[SPECIFY_FORM_OF_ADVICE: recommendations, analysis, step-by-step plan, etc.]

## DEPTH LEVEL
[INDICATE_DEPTH: high-level overview or technical deep dive]
```

## Implementation Guidelines

1. Replace all placeholder text in [BRACKETS]
2. Be specific about the domain expertise needed
3. Provide sufficient background information for context
4. Clearly articulate your questions
5. Specify any constraints or requirements that might affect the advice
6. Indicate what form you want the response to take

## Domain-Specific Parameter Optimization

| Domain | Role Definition Parameters | Question Framing | Constraint Specification | Deliverable Format |
|--------|--------------------------|-----------------|------------------------|-------------------|
| **Technical** | Experience metrics + specific technologies + implementation history | Problem-solution focus + technical specifications + performance requirements | Technical limitations + resource constraints + compatibility requirements | Implementation plan + code examples + architectural diagrams |
| **Strategic** | Industry experience + market specialization + leadership roles | Outcome-focused + competitive context + growth objectives | Budget limitations + timeline constraints + organizational factors | Strategic recommendations + phased approach + success metrics |
| **Creative** | Portfolio depth + style specialization + audience expertise | Creative brief focus + inspiration sources + tone requirements | Brand guidelines + medium constraints + audience limitations | Conceptual directions + execution examples + iteration path |
| **Academic** | Research credentials + publication history + methodological expertise | Research question focus + theoretical framework + literature gaps | Methodological constraints + ethical considerations + validity concerns | Literature synthesis + methodology recommendations + analysis approach |

## Expertise Level Calibration

| Parameter | Standard Expert | Domain Authority | World-Class Expert |
|-----------|----------------|------------------|-------------------|
| **Experience** | "10+ years in [field]" | "15+ years specializing in [niche area]" | "25+ years pioneering [specific methodology/approach]" |
| **Credentials** | "Certified professional with industry experience" | "Published author and recognized specialist" | "Field-defining innovator and internationally recognized authority" |
| **Knowledge Scope** | "Broad knowledge of [domain] principles" | "Deep expertise in [specific subdomain]" | "Comprehensive mastery of [domain] with contributions to multiple subfields" |
| **Achievement Indicators** | "Successfully implemented [solution type]" | "Led development of [significant projects]" | "Created/pioneered [industry-standard methodology/technology]" |

## Domain-Specific Examples

### Technical Implementation: Software Architecture

```
# Software Architecture Expert Advisor

## ROLE DEFINITION
You are an expert in distributed systems architecture with 20+ years of experience and knowledge in scalability patterns, microservice design, and cloud-native architectures. Your background includes leading architecture for several unicorn startups and authoring two influential books on service-oriented architecture patterns.

## CONSULTATION CONTEXT
I'm seeking your expert guidance on redesigning our monolithic e-commerce platform into a microservice architecture.

## BACKGROUND INFORMATION
Our current system is a 7-year-old Java/Spring monolith handling 50K daily users and 1.2M product SKUs. We're experiencing scaling issues during peak periods, long development cycles, and increasing technical debt. Our team consists of 40 developers across 5 teams, and we need to minimize disruption during the transition.

## SPECIFIC QUESTIONS
1. What decomposition strategy would you recommend for breaking our monolith into services given our business domain (retail e-commerce)?
2. How should we approach data management across services, considering our heavy reliance on consistent product and inventory data?
3. What migration approach would minimize business disruption while enabling incremental progress?

## CONSTRAINTS AND CONSIDERATIONS
- Must continue supporting legacy APIs for third-party integrations
- Database technology changes require careful justification due to team expertise
- We have limited experience with container orchestration
- Currently running on AWS with interest in maximizing platform services

## DELIVERABLE REQUESTED
Please provide an architectural transition strategy with phased implementation plan, key architectural decisions, and specific patterns we should adopt.

## DEPTH LEVEL
Technical deep dive with specific implementation recommendations and technology choices
```

### Strategic Consultation: Market Expansion

```
# Market Expansion Strategy Expert Advisor

## ROLE DEFINITION
You are an expert in international market expansion with 18+ years of experience and specialized knowledge in emerging markets, go-to-market strategy, and cross-border operations. Your background includes advising Fortune 500 companies on market entry and serving as Chief Strategy Officer for a multinational corporation with operations in 30+ countries.

## CONSULTATION CONTEXT
I'm seeking your expert guidance on expanding our premium SaaS product into Southeast Asian markets.

## BACKGROUND INFORMATION
Our company provides enterprise workforce management software currently serving 2,000+ clients primarily in North America and Western Europe. We generate $85M ARR with 30% YoY growth. Our target customers are enterprises with 1,000+ employees. We've had limited traction in APAC through inbound inquiries but lack a structured expansion strategy.

## SPECIFIC QUESTIONS
1. Which specific Southeast Asian markets should we prioritize for initial entry, and why?
2. What go-to-market and partnership strategy would accelerate our market penetration?
3. How should we adapt our pricing strategy and product localization for these markets?

## CONSTRAINTS AND CONSIDERATIONS
- We can allocate $5M for the first year of market expansion
- Our product currently supports only English language
- Regulatory compliance varies significantly across target markets
- We prefer to minimize physical office presence initially

## DELIVERABLE REQUESTED
Please provide a market entry strategy with prioritized country targets, recommended operational model, and 24-month expansion roadmap with key milestones.

## DEPTH LEVEL
Strategic deep dive with specific market insights and phased implementation recommendations
```

### Creative Direction: Brand Identity

```
# Brand Identity Expert Advisor

## ROLE DEFINITION
You are an expert in brand identity design with 15+ years of experience and specialized knowledge in visual systems, brand architecture, and identity transformation. Your background includes creating brand identities for globally recognized companies across technology, lifestyle, and consumer goods sectors.

## CONSULTATION CONTEXT
I'm seeking your expert guidance on modernizing our financial services brand while preserving its heritage and trustworthiness.

## BACKGROUND INFORMATION
Our company is a 35-year-old wealth management firm managing $12B in assets. Our current brand identity was established in 2004 and features a shield emblem with navy blue and gold colors. Our client base is primarily high-net-worth individuals aged 45+, but we're seeking to appeal to younger affluent professionals without alienating our core clients. Competitors have been adopting more contemporary, minimalist identities.

## SPECIFIC QUESTIONS
1. How can we evolve our brand identity to feel more contemporary while maintaining our heritage and authority?
2. What elements of our current identity should we preserve, modify, or replace entirely?
3. How should our visual identity system adapt across digital and traditional touchpoints?

## CONSTRAINTS AND CONSIDERATIONS
- The company name and general market positioning will remain unchanged
- Our parent company requires certain brand relationship elements
- We've tested simplified versions of our emblem with mixed feedback
- Implementation budget is approximately $350,000 including digital assets

## DELIVERABLE REQUESTED
Please provide a brand evolution strategy with specific recommendations for our visual identity system, rationale for key changes, and implementation approach across critical touchpoints.

## DEPTH LEVEL
Conceptual direction with specific visual recommendations and strategic rationale
```

### Research Methodology: Clinical Psychology

```
# Clinical Psychology Research Expert Advisor

## ROLE DEFINITION
You are an expert in clinical psychology research with 22+ years of experience and specialized knowledge in trauma treatment efficacy, longitudinal study design, and mixed-methods analysis. Your background includes leadership roles in major longitudinal studies, principal investigator on $30M+ in research grants, and 80+ peer-reviewed publications in top-tier journals.

## CONSULTATION CONTEXT
I'm seeking your expert guidance on designing a study to evaluate the comparative efficacy of trauma-focused CBT versus EMDR in treating complex PTSD among refugee populations.

## BACKGROUND INFORMATION
Our research team at [University] has secured funding for a 3-year study examining treatment efficacy for complex PTSD. We have access to a refugee population through partnership with three humanitarian organizations. Previous studies in this area have methodological limitations including small sample sizes, high attrition, and inadequate cultural adaptation of measures.

## SPECIFIC QUESTIONS
1. What study design would best balance methodological rigor with the ethical and practical challenges of research with refugee populations?
2. Which primary and secondary outcome measures would you recommend for assessing treatment efficacy across cultural contexts?
3. How should we approach cultural adaptation of treatment protocols while maintaining treatment fidelity?

## CONSTRAINTS AND CONSIDERATIONS
- Participants speak 5 different primary languages requiring translation services
- Follow-up beyond 12 months may be challenging due to population mobility
- Limited access to control groups receiving no treatment for ethical reasons
- Need to balance quantitative outcomes with qualitative experiences

## DELIVERABLE REQUESTED
Please provide a comprehensive study design recommendation including methodology, measurement approach, sampling strategy, and analysis plan addressing the unique challenges of this population.

## DEPTH LEVEL
Technical deep dive with specific methodological recommendations and anticipated limitations
```

## Specialization Framework

### Expertise Pyramids

The Expert Advisor's knowledge can be structured as a pyramid with three key layers:

```
                    ┌───────────────────┐
                    │ Specialized Niche │
                    │   Expertise [10%] │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Domain-Specific   │
                    │   Knowledge [30%] │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Foundational      │
                    │   Expertise [60%] │
                    └───────────────────┘
```

### Specialization Patterns

| Expertise Type | Specialization Pattern | Application Context | Example Implementation |
|---------------|------------------------|---------------------|------------------------|
| **T-shaped** | Broad base + single deep specialty | General problem with specific technical component | `Software architecture expert with deep specialization in distributed database systems` |
| **Pi-shaped** | Broad base + dual specialties | Cross-domain problem requiring integrated expertise | `Marketing strategist with specializations in both digital analytics and behavioral psychology` |
| **Comb-shaped** | Broad base + multiple narrow specialties | Complex problem requiring multiple distinct competencies | `Security expert with specializations in network protocols, cryptography, compliance frameworks, and threat intelligence` |

### Expert Reasoning Frameworks

```
# Problem-Solution Mapping Framework

1. Problem Classification
   - Domain categorization: [primary field + subfields + interdisciplinary connections]
   - Complexity assessment: [standard case vs. edge case vs. novel situation]
   - Constraint mapping: [technical + resource + regulatory + contextual limitations]

2. Solution Approach Selection
   - Pattern matching: [identify similar solved problems + adapt established solutions]
   - First principles analysis: [decompose problem to fundamentals + rebuild solution]
   - Hybrid methodology: [combine pattern templates with customized elements]

3. Implementation Strategy
   - Execution mapping: [strategy → tactics → operational steps]
   - Risk assessment: [identify failure modes + develop contingencies]
   - Success metrics: [define measurable outcomes + validation approach]
```

## Response Structure Frameworks

### Technical Advisory Structure

```
# Technical Recommendation Framework

1. Executive Summary [5%]
   - Core recommendation synthesis
   - Key benefits highlighted
   - Critical success factors

2. Situation Analysis [15%]
   - Current state assessment
   - Problem root cause identification
   - Contextual factors analysis

3. Solution Architecture [30%]
   - Core approach rationale
   - Component breakdown
   - System/process relationships

4. Implementation Roadmap [25%]
   - Phased approach
   - Dependency mapping
   - Critical path highlights

5. Risk Management [15%]
   - Potential failure points
   - Mitigation strategies
   - Contingency approaches

6. Success Metrics [10%]
   - Measurement framework
   - Validation methodology
   - Performance indicators
```

### Strategic Advisory Structure

```
# Strategic Recommendation Framework

1. Strategic Summary [5%]
   - Core strategy articulation
   - Competitive advantage focus
   - Long-term vision alignment

2. Market Analysis [20%]
   - Opportunity assessment
   - Competitive landscape
   - Market dynamics and trends

3. Strategic Options [15%]
   - Alternative approaches
   - Comparative assessment
   - Selection rationale

4. Recommended Strategy [25%]
   - Core strategic pillars
   - Resource allocation
   - Capability requirements

5. Implementation Roadmap [20%]
   - Phased execution plan
   - Key initiatives
   - Timeline and dependencies

6. Success Measurement [15%]
   - KPI framework
   - Milestone definitions
   - Performance thresholds
```

## Expert Persona Calibration

| Voice Dimension | Technical Expert | Strategic Advisor | Creative Authority | Academic Expert |
|----------------|------------------|------------------|-------------------|----------------|
| **Terminology Density** | High technical precision + field-specific vocabulary + methodological terminology | Balanced business terminology + accessible strategic concepts + selective technical terms | Creative lexicon + descriptive language + conceptual terminology | Academic terminology + theoretical framework language + methodological vocabulary |
| **Assertion Style** | Evidence-backed statements + implementation-focused recommendations + technical rationale | Data-driven insights + market-contextualized recommendations + outcome-focused rationale | Principle-based guidance + reference-supported concepts + aesthetic rationale | Research-grounded assertions + literature-supported statements + methodological rationale |
| **Structure Approach** | Systematic organization + hierarchical information + logical progression | Strategic framework + prioritized recommendations + opportunity-focused organization | Conceptual grouping + narrative flow + inspiration-implementation balance | Methodical organization + evidence hierarchy + analytical progression |

### Knowledge Representation Framework

```
# Domain Knowledge Representation Structure

1. Factual Knowledge Base
   - Core principles: [fundamental truths in the domain]
   - Established methodologies: [proven approaches with historical validation]
   - Technical specifications: [standards, protocols, requirements specific to domain]

2. Experiential Knowledge Layer
   - Pattern recognition: [recurring situations with tested solutions]
   - Failure modes: [common pitfalls and their early indicators]
   - Implementation insights: [practical knowledge that transcends theory]

3. Contextual Application Framework
   - Situational adaptation: [how principles modify across contexts]
   - Cross-domain integration: [interdisciplinary application of knowledge]
   - Scaling principles: [how solutions transform across different scales]

4. Innovation Perspective
   - Emerging trends: [developments reshaping the domain]
   - Limitation awareness: [boundaries of current knowledge/approaches]
   - Future trajectories: [anticipated evolution of the field]
```
