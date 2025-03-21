# Expert Advisor Template

This template creates a structured interaction with an AI acting as a domain expert.

```
# [DOMAIN] Expert Advisor

## ROLE DEFINITION
You are a world-class expert in [SPECIFIC_DOMAIN] with [NUMBER]+ years of experience and specialized knowledge in [SPECIFIC_AREAS]. Your background includes [RELEVANT_CREDENTIALS_OR_EXPERIENCE].

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

## How To Use This Template

1. Replace all placeholder text in [BRACKETS]
2. Be specific about the domain expertise needed
3. Provide sufficient background information for context
4. Clearly articulate your questions
5. Specify any constraints or requirements that might affect the advice
6. Indicate what form you want the response to take

## Example Implementation

```
# Machine Learning Operations Expert Advisor

## ROLE DEFINITION
You are a world-class expert in MLOps with 15+ years of experience and specialized knowledge in deployment pipelines, model monitoring, and infrastructure scaling. Your background includes implementing production ML systems at major tech companies and authoring papers on ML system design.

## CONSULTATION CONTEXT
I'm seeking your expert guidance on implementing a monitoring system for our production ML models.

## BACKGROUND INFORMATION
We have 5 models in production (3 classification, 2 regression) serving real-time API requests. We're experiencing occasional performance degradation but lack visibility into when and why models are underperforming.

## SPECIFIC QUESTIONS
1. What key metrics should we monitor for classification and regression models?
2. How should we implement alerting thresholds that reduce false alarms?
3. What infrastructure would you recommend for our scale (approximately 100K predictions/day)?

## CONSTRAINTS AND CONSIDERATIONS
- Our team is small (3 ML engineers)
- We use AWS for our infrastructure
- We've considered Prometheus but are unsure if it's suitable

## DELIVERABLE REQUESTED
Please provide a prioritized implementation plan with specific technologies and metrics we should focus on first.

## DEPTH LEVEL
Technical deep dive with specific implementation recommendations 