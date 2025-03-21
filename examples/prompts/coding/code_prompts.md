# Coding Prompt Examples

> **Navigation**: [Examples](../../) | `Prompts` → Coding
> 
> **Related**: [Coding Methodology](../../../docs/domains/coding/methodology.md), [Chain of Thought](../../../docs/prompt_patterns/chain_of_thought.md)

## Quick Summary
**For beginners**: Ready-to-use coding prompts you can copy and adapt for your projects, covering tasks from code generation to debugging.

**For practitioners**: A curated collection of optimized prompts for different coding scenarios, demonstrating effective application of prompt engineering patterns.

**Key takeaway**: These examples show effective prompt patterns in action. Use them as starting points and modify them for your specific coding needs.

---

MODEL:
[Specify how you want the LLM to approach the task. What role should it take? What tone, style, or perspective should it adopt?]

PRECISION:
[Be explicit about requirements, constraints, and specifications. Include formats, lengths, or other measurable criteria.]

TEST:
[Include evaluation criteria or how you'll judge success. Mention any specific areas where you want the model to focus its quality efforts.]

CONTEXT: [Add any additional domain-specific information or requirements here]
```

### Chain-of-Thought Reasoning Template

```
Task: [Describe complex problem to solve]

To solve this problem effectively, I need you to approach it using step-by-step reasoning.

Please:
1. First, identify the key components of the problem
2. Break down the problem into manageable sub-problems
3. Solve each sub-problem sequentially, showing your work
4. Explain your reasoning at each step
5. Consider alternative approaches where relevant
6. Identify and address potential pitfalls or edge cases
7. Synthesize the sub-solutions into a complete solution
8. Verify the solution against the original problem requirements

If you encounter uncertainties or need to make assumptions, explicitly state them and explain why they're reasonable.

Problem details:
[Provide the specific problem details here]
```

### Few-Shot Learning Template

```
I need help with [specific task]. Here are a few examples of what I'm looking for:

EXAMPLE 1:
Input: [example input 1]
Output: [example output 1]

EXAMPLE 2:
Input: [example input 2]
Output: [example output 2]

EXAMPLE 3:
Input: [example input 3]
Output: [example output 3]

Please follow the same pattern for the following:

Input: [your actual input]
```

### Expert Consultation Template

```
You are a world-class expert in [specific domain] with 20+ years of experience and deep knowledge of [relevant subdomain or techniques].

CONSULTATION REQUEST: I need your expert guidance on [specific problem or question].

BACKGROUND:
[Provide context about your situation, project, or challenge]

SPECIFIC QUESTIONS:
1. [First specific question]
2. [Second specific question]
3. [Third specific question]

CONSTRAINTS AND CONSIDERATIONS:
- [List any limitations or requirements]
- [Include relevant factors that might affect the advice]
- [Mention specific approaches you've already considered]

DELIVERABLE REQUESTED:
[Specify what form you want the advice to take - recommendations, step-by-step plan, analysis, etc.]

LEVEL OF DETAIL: [Indicate whether you want a high-level overview or in-depth technical response]
```

### Role-Based Simulation Template

```
You will act as [specific role or profession] with expertise in [relevant specialty areas].

SCENARIO: [Describe the situation or context]

YOUR ROLE: As a [role], your responsibilities include [key aspects of this role] and you have access to [tools, resources, or information available].

TASK: [Describe what you need the role-played expert to do]

AUDIENCE: [Describe who will receive this information and their level of familiarity with the subject]

CONSTRAINTS:
- [List any limitations or requirements]
- [Include format specifications]
- [Mention tone, style, or approach preferences]

ADDITIONAL INFORMATION:
[Provide any other context or details that would help the role-player respond appropriately]

Please respond as this professional would, drawing on standard practices and knowledge in the field of [relevant domain].
```

## Software Development Prompts

### Code Architecture Transformation

```
You are a senior software architect specializing in modern microservice design patterns. 

I have a monolithic class that handles user authentication, profile management, and notification preferences. The code is becoming unwieldy as we scale.

PURPOSE: Transform this monolithic class into a microservices architecture.

CONTEXT: Our application is a SaaS platform with 100k+ users. We're experiencing performance bottlenecks and deployment challenges.

CONSTRAINTS:
- Each microservice should have a single responsibility
- Services should communicate via well-defined APIs
- Authentication should use JWT
- Consider data consistency across services

Here's the current class structure:
[paste your code here]

Please provide:
1. A diagram (in text form) showing the proposed microservices
2. Sample code for each microservice
3. API specifications for service communication
4. Migration strategy with steps
```

### Test Suite Generation

```
Act as a quality assurance engineer with expertise in test-driven development.

TASK: Generate a comprehensive test suite for the following method.

METHOD:
function validateUserCredentials(username, password, options = {}) {
  if (!username || typeof username !== 'string') return false;
  if (!password || typeof password !== 'string') return false;
  
  const minUsernameLength = options.minUsernameLength || 5;
  const minPasswordLength = options.minPasswordLength || 8;
  const requireSpecialChar = options.requireSpecialChar !== false;
  
  if (username.length < minUsernameLength) return false;
  if (password.length < minPasswordLength) return false;
  if (requireSpecialChar && !/[!@#$%^&*(),.?":{}|<>]/.test(password)) return false;
  
  return true;
}

TEST REQUIREMENTS:
- Include unit tests for all success and failure paths
- Test edge cases and boundary conditions
- Use a modern testing framework (Jest preferred)
- Include mocks where appropriate
- Aim for 100% code coverage
- Tests should be descriptive and maintainable

FORMAT: Provide the complete test file with organized test cases grouped by functionality.
```

### API Development Specification

```
You are developing a RESTful API for a new e-commerce platform.

GOAL: Design a comprehensive API specification for the product catalog and shopping cart functionality.

REQUIREMENTS:
1. The API should follow REST principles and use JSON
2. Include authentication/authorization mechanisms
3. Support pagination, filtering, and sorting for product listings
4. Handle product variants (size, color, etc.)
5. Support shopping cart operations (add, remove, update quantity)
6. Include error handling and status codes

DELIVERABLES:
1. API endpoints with HTTP methods, URL patterns, and descriptions
2. Request/response examples for each endpoint
3. Authentication scheme
4. Error response format
5. Data models for products and shopping cart items

CONSTRAINTS:
- API should be versioned
- Security best practices must be followed
- Optimize for mobile client usage
```

## Data Science & Analytics

### Exploratory Data Analysis

```
You are a data scientist analyzing customer churn data for a subscription service.

TASK: Design an exploratory data analysis plan for identifying factors that contribute to customer churn.

DATASET DESCRIPTION:
- 50,000 customer records
- Features include: demographics, subscription plan, usage patterns, customer service interactions, payment history
- Target variable: churned (yes/no)
- Class imbalance: 85% retained, 15% churned

DELIVERABLES:
1. Data cleaning and preprocessing steps
2. Statistical analysis approach
3. Visualization plan with specific chart types and purposes
4. Feature importance analysis method
5. Key metrics to measure
6. Hypothesis testing approach

CONSTRAINTS:
- Focus on actionable insights for business stakeholders
- Analysis should be reproducible
- Prioritize methods that handle class imbalance
- Include both statistical significance and business impact
```

### Data Visualization Guidance

```
As a data visualization expert, help me create effective visualizations for quarterly sales performance data.

DATA DESCRIPTION:
- Sales figures across 4 product categories
- 5 geographic regions
- 3 customer segments
- Year-over-year comparison (2023 vs 2024)
- Also have profit margins and marketing spend

AUDIENCE: Executive leadership team in quarterly business review

GOALS:
1. Highlight key trends and patterns
2. Show regional performance differences
3. Identify underperforming and overperforming segments
4. Demonstrate ROI on marketing spend

DELIVERABLES:
1. Recommended chart types with rationale
2. Visualization hierarchy and layout suggestions
3. Color scheme recommendations
4. Annotation strategies for key insights
5. Interactive elements (if applicable)

NOTES:
- Avoid information overload
- Focus on actionable insights
- Consider accessibility in design choices
```

## Healthcare & Medicine

### Patient Education Materials

```
You are a healthcare communication specialist working with a primary care clinic.

TASK: Transform these technical medical instructions into patient-friendly educational material.

MEDICAL TEXT:
"Patient is prescribed Metformin HCl 500mg PO BID with meals for Type 2 Diabetes Mellitus. Monitor blood glucose QD fasting and BID postprandial. Report hypoglycemic symptoms. Follow low-glycemic diet as per nutritionist recommendations. Return for HbA1c evaluation in 3 months."

REQUIREMENTS:
1. Use plain language at 6th-8th grade reading level
2. Organize information chronologically
3. Include simple explanations for medical terms
4. Add clear action items for the patient
5. Include warning signs that require medical attention
6. Format for easy scanning and comprehension

TARGET AUDIENCE: 65-year-old patient with newly diagnosed Type 2 Diabetes who has limited health literacy.
```

### Medical Diagnostic Reasoning

```
Act as an experienced diagnostician in internal medicine with 20+ years of clinical practice.

PATIENT CASE:
A 57-year-old male presents with progressive fatigue, unexplained weight loss of 15 pounds over 3 months, occasional night sweats, and a persistent dry cough. Patient has a 30-pack-year smoking history but quit 5 years ago. Physical examination reveals palpable cervical lymphadenopathy.

TASK: Using clinical reasoning, provide:

1. Top 3 differential diagnoses with supporting evidence from the case
2. For each diagnosis, list:
   - Additional history questions to ask
   - Physical examination elements to focus on
   - Appropriate diagnostic tests in order of priority
   - Reasoning behind each recommendation

3. Discuss how your diagnostic approach would change if:
   - The patient had never smoked
   - The patient had a history of occupational asbestos exposure
   - The lymphadenopathy was absent

FORMAT: Structure your response as a clinical reasoning exercise, explaining your thought process at each step.
```

## Education & Tutoring

### Math Concept Explanation

```
You are a math tutor specializing in making complex concepts accessible to high school students.

TASK: Create an explanation of the concept of derivatives in calculus for a 11th-grade student who is strong in algebra but new to calculus.

REQUIREMENTS:
1. Start with an intuitive, real-world explanation before formal definitions
2. Use clear, concrete examples that build in complexity
3. Include 2-3 practice problems with step-by-step solutions
4. Anticipate common misconceptions and address them
5. Connect the concept to previously learned mathematics (slopes, rates of change)
6. Include visualizations that could be drawn on paper
7. Use language appropriate for a 16-17 year old student

CONSTRAINTS:
- Explanation should take no more than 10 minutes to read
- Avoid technical jargon without explanation
- Emphasize conceptual understanding over memorization of rules
```

### Lesson Plan Development

```
You are a curriculum designer for secondary education.

TASK: Create a detailed lesson plan on the causes and effects of climate change for a 10th-grade environmental science class.

LESSON SPECIFICATIONS:
- Duration: 60-minute class period
- Learning objectives: Students will be able to (1) identify at least three major causes of climate change, (2) explain three significant environmental impacts, and (3) evaluate one potential solution
- Prior knowledge: Students have basic understanding of the greenhouse effect and carbon cycle
- Classroom resources: Internet access, projector, whiteboards

REQUIRED ELEMENTS:
1. Attention-grabbing opening activity (5-7 minutes)
2. Direct instruction component with key content (15 minutes)
3. Interactive student-centered activity (20 minutes)
4. Assessment method to gauge understanding (10 minutes)
5. Closing discussion and homework assignment (5 minutes)
6. Differentiation strategies for diverse learners
7. List of required materials and resources
8. Extensions or modifications for different time constraints

FORMAT: Structured lesson plan with timed segments and detailed instructions for each component.
```

## Business & Marketing

### Marketing Campaign Development

```
You are a senior marketing strategist at a digital agency.

CLIENT: A direct-to-consumer sustainable home goods brand targeting environmentally-conscious millennials.

OBJECTIVE: Create a comprehensive holiday season marketing campaign to:
- Increase Q4 sales by 30% YoY
- Grow email subscriber list by 15%
- Improve customer retention rate

BACKGROUND:
- Brand values: sustainability, ethical production, minimalist design
- Average customer value: $120
- Current marketing channels: Instagram, Facebook, Email, Google Search
- Top-performing products: bamboo bedding, recycled glassware, organic cotton towels
- Budget: $75,000

DELIVERABLES:
1. Campaign concept and messaging strategy
2. Channel-specific tactics with budget allocation
3. Content calendar for November-December
4. Key performance indicators and measurement approach
5. Customer journey mapping
6. Post-holiday retention strategy

CONSTRAINTS:
- Must emphasize sustainability during a traditionally high-consumption season
- Need to compete with larger brands offering steep discounts
- Production capacity limits flash sales to 72 hours maximum
```

### Executive Communication

```
You are a communications specialist preparing the CEO for a critical investor presentation.

CONTEXT: The company missed its Q3 revenue targets by 12% but has a promising product pipeline and strategic acquisition in progress.

TASK: Craft talking points for the CEO to address investor concerns while maintaining confidence in the company's direction.

AUDIENCE: Institutional investors, financial analysts, and major shareholders

KEY MESSAGES TO CONVEY:
1. Acknowledgment of missed targets with specific factors (not excuses)
2. Short-term correction strategy already in implementation
3. Long-term growth vision remains solid
4. Pipeline innovations with market potential
5. Strategic acquisition synergies and timeline
6. Updated guidance for Q4 and next fiscal year

FORMAT REQUIREMENTS:
1. Opening statement (2 minutes)
2. 5-7 concise talking points on key issues
3. Anticipated challenging questions with suggested responses
4. Data points and metrics to reference
5. Closing statement emphasizing confidence and action

TONE: Transparent, confident, and forward-looking without dismissing concerns
```

## Content Creation

### Blog Article Outline

```
You are a content strategist for a SaaS company that provides project management software.

ASSIGNMENT: Create a detailed outline for a blog article titled "Agile Project Management for Remote Teams: Overcoming the Distance Challenge."

TARGET AUDIENCE: Mid-level project managers and team leads who are struggling with remote team coordination.

MARKETING GOALS:
- Position our software as a solution for remote team challenges
- Generate leads from project managers searching for remote collaboration solutions
- Establish thought leadership in remote work project management

SEO REQUIREMENTS:
- Primary keyword: "agile project management for remote teams"
- Secondary keywords: "virtual stand-ups," "remote scrum," "distributed agile teams"

ARTICLE SPECIFICATIONS:
1. Comprehensive outline with H2 and H3 subheadings
2. Include statistics and potential research to reference
3. Specify where to include practical examples
4. Note opportunities for product mentions (max 2, non-promotional)
5. Suggest pull quotes for social media
6. Recommend internal and external linking strategy
7. Propose call-to-action

TONE: Professional, practical, solution-oriented
```

### Video Script Development

```
You are a video content creator specializing in educational content.

PROJECT: Create a script for a 5-7 minute YouTube video explaining blockchain technology to complete beginners.

TARGET AUDIENCE: 18-30 year olds interested in technology but with no background in cryptocurrency or blockchain.

VIDEO OBJECTIVES:
1. Explain what blockchain is in simple, relatable terms
2. Illustrate how blockchain works with visual metaphors
3. Highlight 2-3 real-world applications beyond cryptocurrency
4. Address common misconceptions
5. Engage viewers to want to learn more

SCRIPT REQUIREMENTS:
1. Conversational, jargon-free language
2. Opening hook to capture attention in first 15 seconds
3. Visual directions and animation cues in [brackets]
4. Clear section breaks with timestamps
5. Analogies and metaphors for complex concepts
6. Questions to maintain viewer engagement
7. Concise closing with call-to-action

TONE: Friendly, curious, mildly humorous but educational
```

## Customer Support & Service

### Customer Service Response Templates

```
You are the customer experience manager for an online fitness subscription service.

TASK: Create a set of response templates for common customer service scenarios.

BRAND VOICE: Supportive, encouraging, solution-oriented, health-focused

SCENARIOS TO ADDRESS:
1. Customer requesting to cancel their subscription
2. Customer reporting technical difficulties with streaming workouts
3. Customer complaining about being charged after free trial
4. Customer asking for workout modifications due to injury
5. Customer requesting a refund due to dissatisfaction
6. Customer inquiring about nutrition plan options
7. Customer having trouble with account login

FOR EACH TEMPLATE, INCLUDE:
- Empathetic acknowledgment of the issue
- Clear next steps or resolution path
- Relevant policy information (when applicable)
- Personalization placeholders
- Upsell or retention opportunity where appropriate
- Professional closing

SPECIAL REQUIREMENTS:
- Templates should be modular with customizable elements
- Include alternate versions for email and chat
- Max 150 words per template
- Flag points where agents need to insert specific information
```

### Technical Support Troubleshooting Guide

```
You are a senior technical support specialist for a company that develops productivity software.

TASK: Create a structured troubleshooting guide for support agents handling the most common synchronization issues between the desktop and mobile applications.

USER CONTEXT: Customers report that files created or edited on one device are not appearing on their other devices, leading to workflow disruptions and duplicate work.

GUIDE REQUIREMENTS:
1. Diagnostic decision tree with clear yes/no questions
2. Step-by-step resolution instructions for each identified cause
3. Screenshots or visual indicators at critical steps (described in [brackets])
4. Technical explanation for support agents to understand underlying issues
5. Simplified explanation that agents can relay to customers
6. Escalation criteria for engineering team involvement
7. Workarounds for unresolved issues

COMMON CAUSES TO ADDRESS:
- Network connectivity problems
- Authentication issues
- Version incompatibility
- Storage limitations
- Permission settings
- Corrupt local data
- Account configuration errors

FORMAT: Structured troubleshooting flow with clear progression logic and resolution paths
```

## Research & Academic

### Literature Review Framework

```
You are a research methodologist working with doctoral candidates.

TASK: Create a structured framework for conducting a comprehensive literature review on the impact of artificial intelligence on employment in the manufacturing sector.

RESEARCH SCOPE:
- Timeframe: Literature from 2015-2025
- Geographic focus: Global, with emphasis on developed economies
- Industries: Manufacturing, with subsectors in automotive, electronics, and textiles
- AI technologies: Machine learning, computer vision, robotics process automation
- Impact areas: Job displacement, job creation, skill requirements, wage effects

FRAMEWORK COMPONENTS:
1. Research question formulation and refinement
2. Database selection with search strategy
3. Inclusion and exclusion criteria
4. Data extraction methodology
5. Quality assessment parameters
6. Synthesis approach (narrative, meta-analysis, or thematic)
7. Gap identification method
8. Theoretical framework integration

DELIVERABLES:
1. Step-by-step protocol for literature search and review
2. Templates for data extraction and synthesis
3. Quality assessment checklist
4. Common pitfalls and mitigation strategies
5. Timeline for each stage of the review process

ACADEMIC STANDARDS: The framework should adhere to PRISMA guidelines for systematic reviews and meta-analyses.
```

### Research Hypothesis Development

```
You are a research methods consultant advising graduate students in psychology.

TASK: Help develop testable hypotheses for a study on the relationship between social media use and young adult mental health.

RESEARCH INTEREST: Investigating how different patterns of social media engagement affect anxiety, depression, and self-esteem in adults aged 18-25.

AVAILABLE RESOURCES:
- Access to 300 university students for survey research
- Validated psychological assessment tools
- Social media usage tracking (with permission)
- 4-month timeframe for data collection
- Statistical analysis software

DELIVERABLES:
1. 3-5 specific, testable hypotheses
2. Variables to measure for each hypothesis (independent, dependent, and control)
3. Operational definitions of key concepts
4. Potential confounding variables to address
5. Statistical analyses appropriate for testing each hypothesis
6. Methodological considerations for each hypothesis
7. Theoretical framework alignment

SCIENTIFIC CONSTRAINTS:
- Hypotheses must be falsifiable
- Based on existing literature and theory
- Feasible within resource constraints
- Address potential ethical considerations
- Consider statistical power requirements
```

## Legal & Compliance

### Legal Document Simplification

```
You are a legal communication specialist working with a consumer rights law firm.

TASK: Transform this complex legal language into a clear, comprehensible explanation for the average consumer while preserving all substantive legal information.

LEGAL TEXT:
"The party of the first part hereby acknowledges and affirms that, in consideration of the sum specified in Section 3(b), all rights, title, and interest in and to the intellectual property described in Exhibit A, including without limitation all patents, copyrights, trademarks, trade secrets, and other proprietary rights associated therewith, shall be irrevocably assigned, transferred, and conveyed to the party of the second part, and that such assignment, transfer, and conveyance shall be deemed effective as of the Effective Date defined in Section 1(a) hereinabove."

REQUIREMENTS:
1. Reduce reading level to approximately 8th grade
2. Maintain all legally significant information
3. Organize with clear headings and bulleted lists where appropriate
4. Define legal terms when first used
5. Use active voice and direct address
6. Add contextual explanations where needed

TARGET AUDIENCE: Consumers with no legal background who need to understand their rights in a contract.
```

### Compliance Training Module

```
You are an instructional designer specializing in corporate compliance training.

TASK: Create an outline for an interactive compliance training module on data privacy regulations for customer service employees.

LEARNING OBJECTIVES:
After completing this module, employees will be able to:
1. Identify types of personally identifiable information (PII) they encounter
2. Apply proper data handling procedures for customer information
3. Recognize and respond to potential data breach scenarios
4. Understand consent requirements for data collection and use
5. Explain the company's obligations under GDPR, CCPA, and internal policies

TARGET AUDIENCE: Customer service representatives who regularly access customer data but have minimal technical background.

MODULE REQUIREMENTS:
1. Module structure with estimated time for each section (total: 45 minutes)
2. Interactive elements and knowledge checks
3. Real-world scenarios specific to customer service situations
4. Decision points with consequence explanations
5. Visual aids and infographic concepts
6. Assessment methodology
7. Implementation notes for technical team

SPECIAL CONSIDERATIONS:
- Must accommodate different learning styles
- Need reinforcement of critical compliance points
- Should address common misconceptions
- Must be updatable as regulations change
```

## Technical Documentation

### API Documentation Template

```
You are a technical documentation specialist creating developer resources for a new API.

TASK: Design a comprehensive API documentation template that will be used for all endpoints in our payment processing API.

API CONTEXT: RESTful API for payment processing, including transactions, refunds, subscriptions, and customer management.

TEMPLATE REQUIREMENTS:
1. Endpoint overview section with:
   - HTTP method and URL pattern
   - Authentication requirements
   - Rate limiting information
   - Brief functional description

2. Request details section with:
   - Header parameters with types, requirements, and descriptions
   - Path parameters with validation rules
   - Query parameters with defaults and constraints
   - Request body schema with example JSON
   - Required vs. optional parameters clearly marked

3. Response details section with:
   - Success response codes and meanings
   - Error response codes with troubleshooting guidance
   - Response body schema with example JSON
   - Pagination details (if applicable)

4. Code examples section with:
   - Implementation in 3 popular languages
   - Common use cases demonstrated

5. Additional sections for:
   - Versioning information
   - Deprecation notices and migration paths
   - Related endpoints
   - SDK support details

FORMAT: The template should follow OpenAPI 3.0 specification standards while being accessible to developers of varying experience levels.
```

### User Manual Development

```
You are a technical writer creating documentation for a smart home security system.

TASK: Develop a comprehensive user manual for a new smart home security system that includes cameras, door/window sensors, motion detectors, and a mobile app.

TARGET AUDIENCE: Homeowners with varying levels of technical proficiency, from beginners to tech-savvy users.

MANUAL SECTIONS:
1. System Overview and Components
2. Installation and Setup
3. Mobile App Configuration
4. Daily Operation
5. Alert Management
6. Remote Access Features
7. Maintenance and Troubleshooting
8. Privacy and Security Settings
9. Advanced Configurations
10. Warranty and Support Information

REQUIREMENTS:
1. Clear step-by-step instructions with visual indicators
2. Troubleshooting decision trees for common issues
3. Safety warnings and regulatory compliance information
4. Beginner-friendly language with technical terms explained
5. Hierarchical organization with logical progression
6. Cross-references between related sections
7. Icons and visual cues for important information
8. Both quick-start and in-depth content for different users

SPECIAL CONSIDERATIONS:
- Include accessibility features explanation
- Emphasize privacy best practices
- Address common user concerns
- Provide both basic and advanced setup options
```

## Security & Risk Management

### Security Incident Response Plan

```
You are a cybersecurity consultant developing incident response protocols.

TASK: Create a structured incident response plan for ransomware attacks targeting a mid-sized financial services company.

ORGANIZATION CONTEXT:
- 200 employees across 3 locations
- Manages sensitive financial and personal data
- Regulatory requirements: SOC 2, PCI DSS, GDPR
- IT infrastructure: Hybrid cloud and on-premises
- Current backup strategy: Daily incremental, weekly full backups

PLAN REQUIREMENTS:
1. Incident classification criteria and severity levels
2. Roles and responsibilities for the incident response team
3. Step-by-step containment procedures
4. Forensic investigation protocol
5. Communication plan (internal, customers, regulators, law enforcement)
6. Recovery and business continuity steps
7. Post-incident analysis framework
8. Documentation requirements throughout the process

SPECIAL CONSIDERATIONS:
- Legal and regulatory reporting obligations
- Evidence preservation requirements
- Decision framework for ransom payment considerations
- Customer data breach notification process
- Media response strategy
- Staff training recommendations

FORMAT: Structured plan with clear action items, decision points, and responsibilities for each stage of incident response.
```

### Risk Assessment Framework

```
You are a risk management consultant working with a healthcare organization.

TASK: Develop a comprehensive risk assessment framework for evaluating third-party vendors who will have access to patient data.

REGULATORY CONTEXT: Organization must comply with HIPAA, HITECH, and state healthcare privacy regulations.

FRAMEWORK COMPONENTS:
1. Pre-assessment vendor questionnaire
2. Document request list for due diligence
3. Technical security assessment criteria
4. Data handling and privacy evaluation metrics
5. Compliance verification methodology
6. Business continuity and disaster recovery requirements
7. Risk scoring methodology with weighted factors
8. Remediation planning template
9. Ongoing monitoring protocol

RISK CATEGORIES TO ASSESS:
- Data security controls
- Privacy policy and practices
- Technical infrastructure
- Physical security measures
- Staff training and awareness
- Incident response capabilities
- Subcontractor management
- Business stability and longevity
- Geographic/jurisdictional considerations

DELIVERABLES:
1. Assessment process workflow
2. Evaluation templates and checklists
3. Risk scoring matrix with thresholds
4. Approval/rejection criteria
5. Conditional approval requirements
6. Reassessment frequency guidelines

FORMAT: Structured framework with clear evaluation criteria, scoring methodology, and decision guidance.
```

## Product Management

### Product Requirements Document

```
You are a product manager for a SaaS company developing project management software.

TASK: Create a product requirements document (PRD) for a new resource allocation feature that helps teams optimize staff assignments across multiple projects.

BUSINESS CONTEXT:
- User feedback indicates difficulty tracking team member availability
- Competitors have basic workload visualization but lack predictive features
- Company strategy emphasizes AI-powered efficiency tools
- Revenue goal: increase enterprise plan adoption by 20%

PRD SECTIONS:
1. Executive Summary
   - Problem statement
   - Proposed solution
   - Success metrics

2. User Stories and Requirements
   - Primary user stories with acceptance criteria
   - Functional requirements
   - Non-functional requirements (performance, scalability, etc.)
   - Technical constraints

3. Feature Specifications
   - Resource visualization component
   - Capacity planning tools
   - Conflict detection and resolution
   - Reporting and analytics
   - Integration requirements with existing modules

4. User Experience
   - User flow diagrams
   - Wireframe concepts
   - Key interaction points
   - Accessibility requirements

5. Implementation Considerations
   - Phasing strategy
   - Dependencies
   - Testing requirements
   - Migration and backward compatibility

6. Success Metrics
   - KPIs to measure feature success
   - Analytics implementation needs
   - Baseline metrics and targets

FORMAT: Comprehensive PRD with clear, prioritized requirements and explicit acceptance criteria.
```

### User Research Discussion Guide

```
You are a UX researcher planning to conduct user interviews for a mobile banking app redesign.

TASK: Create a discussion guide for 60-minute user interviews to understand pain points in the current app and validate proposed improvements.

RESEARCH OBJECTIVES:
1. Identify frustrations with current transaction workflows
2. Understand mental models around financial categorization
3. Validate new budget visualization concepts
4. Explore user attitudes toward automated financial insights
5. Assess comprehension of security features

PARTICIPANT PROFILE:
- Primary banking app users
- Mix of frequent (daily/weekly) and occasional users
- Age range 25-55
- Various financial literacy levels

DISCUSSION GUIDE COMPONENTS:
1. Introduction script with research purpose and confidentiality information
2. Warm-up questions to establish rapport and usage patterns
3. Current experience exploration
   - Task completion questions
   - Pain point identification
   - Satisfaction assessment
4. Concept testing protocol
   - Introduction of new design concepts
   - Reaction questions
   - Comprehension checks
   - Preference explorations
5. Prioritization exercise for potential features
6. Wrap-up questions and next steps

SPECIAL INSTRUCTIONS:
- Include timing for each section
- Note probing questions for deeper insights
- Include instructions for presenting prototypes
- Highlight areas to customize based on user profile
- Suggest documentation method for each section

FORMAT: Structured discussion guide with clear questions, moderator instructions, and time allocations.
```

## Financial Planning & Investment

### Investment Portfolio Analysis

```
You are a Certified Financial Analyst with expertise in portfolio optimization and risk management.

TASK: Analyze the following investment portfolio and provide recommendations for rebalancing to better align with the client's goals and risk tolerance.

CLIENT PROFILE:
- 45-year-old technology professional
- Retirement goal: age 60
- Risk tolerance: Moderate
- Time horizon: 15 years for retirement, 5 years for home purchase
- Annual income: $150,000
- Monthly investment capacity: $3,000

CURRENT PORTFOLIO:
- U.S. Large Cap Stocks: 45% ($225,000)
- U.S. Small Cap Stocks: 15% ($75,000)
- International Developed Markets: 10% ($50,000)
- Emerging Markets: 5% ($25,000)
- Corporate Bonds: 15% ($75,000)
- Treasury Bonds: 5% ($25,000)
- Cash: 5% ($25,000)
- Total: $500,000

ECONOMIC CONTEXT:
- Current interest rate environment: Rising rates
- Inflation outlook: Moderate concern (3-4%)
- Market valuations: U.S. equities at high historical P/E ratios
- Global economic outlook: Slowing growth in developed markets

DELIVERABLES:
1. Portfolio analysis including risk metrics and diversification assessment
2. Recommended target allocation with justification
3. Specific rebalancing actions with tax efficiency considerations
4. Investment vehicle recommendations (ETFs, mutual funds, etc.)
5. Monitoring schedule and trigger events for future rebalancing

CONSTRAINTS:
- Minimize tax implications where possible
- Keep transaction costs under 0.5% of portfolio value
- Maintain sufficient liquidity for emergency fund (6 months of expenses)
- Consider ESG factors in recommendations
```

### Personal Financial Planning Framework

```
You are a Certified Financial Planner working with a newly married couple.

TASK: Create a comprehensive 5-year financial plan addressing their key life goals and financial situation.

CLIENT PROFILE:
- Couple ages: 32 and 34
- Combined annual income: $180,000
- Current savings: $60,000 emergency fund, $120,000 in retirement accounts
- Debts: $350,000 mortgage, $45,000 student loans, $8,000 car loan
- Short-term goals: Start a family within 2 years, home renovation
- Medium-term goals: College savings, career transitions
- Long-term goals: Early retirement at age 55

PLAN REQUIREMENTS:
1. Cash flow analysis and budget optimization
   - Income projection with potential career changes
   - Essential vs. discretionary spending breakdown
   - Saving rate recommendations

2. Debt management strategy
   - Prioritization framework
   - Refinancing opportunities
   - Payoff schedule

3. Insurance needs analysis
   - Life insurance recommendations
   - Disability coverage assessment
   - Property and liability protection

4. Investment strategy
   - Asset allocation based on goals and time horizons
   - Account type recommendations (taxable vs. tax-advantaged)
   - Specific investment vehicle suggestions

5. Tax optimization approaches
   - Income tax reduction strategies
   - Tax-efficient investment methods
   - Deduction and credit opportunities

6. Estate planning basics
   - Essential documents needed
   - Beneficiary designation review
   - Guardian recommendations for future children

FORMAT: Provide a detailed financial plan with specific actionable steps, divided by timeframe (immediate, year 1, years 2-3, years 4-5) and priority level.
```

## Project Management

### Project Recovery Plan

```
You are a senior project management consultant brought in to help rescue a troubled software implementation project.

SITUATION: A mid-sized manufacturing company is 8 months into a 12-month ERP implementation. The project is currently:
- 40% over budget
- 3 months behind schedule
- Experiencing significant scope creep
- Suffering from low stakeholder engagement
- Facing resistance from end users
- Dealing with vendor relationship issues

TASK: Develop a comprehensive project recovery plan to get the implementation back on track.

REQUIREMENTS:
1. Diagnostic assessment
   - Root cause analysis of current issues
   - Critical path evaluation
   - Resource allocation assessment
   - Stakeholder impact analysis

2. Recovery strategy
   - Revised project schedule with milestones
   - Budget mitigation measures
   - Scope management recommendations
   - Resource reallocation plan
   - Risk mitigation strategies

3. Governance improvements
   - Decision-making framework
   - Escalation procedures
   - Communication plan
   - Progress tracking methodology
   - Change control process

4. Stakeholder management
   - Engagement tactics for executive sponsors
   - User adoption strategies
   - Vendor relationship repair approach
   - Communication templates for different audiences

DELIVERABLES:
1. Executive summary with key recommendations
2. 30-60-90 day action plan
3. Revised project timeline with critical milestones
4. Responsibility assignment matrix (RACI chart)
5. Key performance indicators for measuring recovery progress

CONSTRAINTS:
- Company cannot increase budget by more than 15%
- Go-live date cannot be delayed beyond 6 months
- Core ERP vendor cannot be changed
- Minimal disruption to normal business operations
```

### Agile Team Retrospective Facilitation

```
You are an Agile coach facilitating a sprint retrospective for a software development team.

CONTEXT:
- Team of 8 developers, 1 product owner, and 1 scrum master
- Recently completed their fourth sprint of a new product development
- Delivered 70% of planned story points in the last sprint
- Experiencing challenges with estimation accuracy and cross-team dependencies
- Three new team members joined two sprints ago
- Several production issues emerged from previously completed work

TASK: Design a 90-minute retrospective session that will help the team identify improvement opportunities and create actionable next steps.

RETROSPECTIVE REQUIREMENTS:
1. Opening (10 minutes)
   - Check-in activity to gauge team mood
   - Review of retrospective purpose and previous action items
   - Establishment of psychological safety guidelines

2. Data Gathering (25 minutes)
   - Structured activity to collect insights about the sprint
   - Technique for ensuring all voices are heard
   - Method to categorize feedback constructively

3. Insight Generation (20 minutes)
   - Process for identifying patterns and themes
   - Approach for prioritizing issues to address
   - Technique for root cause analysis of top concerns

4. Action Planning (25 minutes)
   - Framework for generating solutions
   - Method for converting ideas into specific, measurable actions
   - Process for assigning ownership and timelines
   - Approach for limiting actions to a manageable number

5. Closing (10 minutes)
   - Session summary technique
   - Method for evaluating the retrospective itself
   - Next steps and follow-up plan

DELIVERABLES:
1. Detailed retrospective agenda with timeboxed activities
2. Facilitation instructions for each section
3. Required materials and preparation steps
4. Virtual/remote adaptation options
5. Follow-up plan for action item tracking

TONE: Constructive, blame-free, future-focused, and empowering
```

## Human Resources & Talent Management

### Employee Performance Improvement Plan

```
You are an HR Business Partner working with a manager who needs to develop a performance improvement plan for an underperforming employee.

EMPLOYEE CONTEXT:
- Mid-level software developer with 4 years at the company
- Previously strong performer who has shown declining results over the past 6 months
- Key performance gaps: missed deadlines, code quality issues, communication deficiencies
- Recent organizational changes have affected their team structure
- Employee has expressed feeling overwhelmed and disconnected

MANAGER CONTEXT:
- Engineering manager overseeing a team of 12 developers
- Wants to support employee improvement rather than immediate termination
- Has documented performance concerns in the past two quarterly reviews
- Limited experience creating formal performance improvement plans

TASK: Create a comprehensive 90-day Performance Improvement Plan (PIP) that is fair, specific, and focused on development.

REQUIREMENTS:
1. Plan Structure
   - Clear performance expectations with measurable outcomes
   - Specific, observable behaviors that need to change
   - Concrete examples of current performance gaps
   - Progressive milestones at 30/60/90 days

2. Support Elements
   - Training and resources to be provided
   - Frequency and format of check-in meetings
   - Documentation requirements for both manager and employee
   - Mentoring or coaching recommendations

3. Success Criteria
   - Specific metrics that define successful improvement
   - Evaluation methodology
   - Consequences for meeting/not meeting requirements
   - Transition plan after completion

4. Legal and Policy Compliance
   - Alignment with company policies
   - Documentation requirements
   - Confidentiality guidelines
   - HR involvement touchpoints

FORMAT: Provide a structured template with guidance notes for the manager, including specific examples of how to word sensitive feedback constructively.
```

### Diversity & Inclusion Training Module

```
You are a Diversity, Equity, and Inclusion (DEI) specialist designing training for a multinational corporation.

TASK: Create an outline for a comprehensive 3-hour DEI training workshop focused on building inclusive leadership skills for mid-level managers.

ORGANIZATIONAL CONTEXT:
- Global technology company with 15,000 employees across 12 countries
- Industry with historical underrepresentation of women and minorities
- Company has set goals to increase leadership diversity by 30% within 3 years
- Recent employee engagement survey indicated concerns about unequal advancement opportunities
- Managers have varying levels of DEI awareness and commitment

TRAINING OBJECTIVES:
After completing this workshop, managers will be able to:
1. Recognize their own unconscious biases and how these affect decision-making
2. Implement inclusive meeting and communication practices
3. Apply fair and equitable approaches to performance evaluation
4. Create development opportunities for team members from underrepresented groups
5. Address microaggressions and non-inclusive behaviors effectively
6. Measure and track inclusion within their teams

WORKSHOP COMPONENTS:
1. Self-Awareness Module
   - Activities to identify personal biases and privileges
   - Reflection exercises on cultural influences
   - Assessment of inclusive leadership behaviors

2. Inclusive Practices Module
   - Techniques for ensuring equitable participation
   - Methods for fair assignment of opportunities
   - Strategies for balanced recognition

3. Intervention Strategies Module
   - Scripts for addressing problematic behaviors
   - Role-playing scenarios for difficult conversations
   - Escalation frameworks for serious concerns

4. Accountability Systems Module
   - Metrics for measuring inclusion
   - Goal-setting for team diversity
   - Integration with performance management

DELIVERABLES:
1. Detailed workshop outline with timing for each activity
2. Facilitator notes with key talking points
3. Participant materials and handouts
4. Pre-work and post-training reinforcement activities
5. Evaluation methodology to measure training effectiveness

DESIGN CONSIDERATIONS:
- Include mixed learning modalities (discussion, case studies, self-reflection, etc.)
- Incorporate real company scenarios and challenges
- Create psychological safety while encouraging authentic engagement
- Address potential resistance constructively
- Provide practical tools that can be implemented immediately
```

## Environmental Science & Sustainability

### Climate Change Impact Assessment

```
You are an environmental scientist conducting a climate change vulnerability assessment for a coastal city.

CITY PROFILE:
- Population: 250,000
- Geography: Coastal location with river delta, average elevation 15 feet above sea level
- Economy: Tourism, fishing industry, regional port, technology sector
- Infrastructure: 30% built before 1980, water treatment plant in low-lying area
- Demographics: 20% elderly population, 25% low-income neighborhoods in flood-prone areas

CLIMATE PROJECTIONS (2050):
- Sea level rise: 1.5-2.5 feet
- Storm intensity: 15-25% increase in major hurricane probability
- Precipitation: 20% increase in extreme rainfall events
- Temperature: 3-5°F increase in average temperatures, 10-15 more days above 95°F annually

TASK: Develop a comprehensive climate vulnerability assessment with adaptation recommendations.

ASSESSMENT COMPONENTS:
1. Exposure Analysis
   - Critical infrastructure vulnerability mapping
   - Population displacement risk assessment
   - Economic impact projections by sector
   - Natural resource and ecosystem threat analysis

2. Sensitivity Assessment
   - Social vulnerability mapping with equity focus
   - Critical service disruption analysis
   - Public health impact projections
   - Cascading failure scenarios for interconnected systems

3. Adaptive Capacity Evaluation
   - Existing resilience measures effectiveness
   - Governance structure assessment
   - Financial resource availability
   - Community cohesion and social capital inventory

4. Risk Prioritization
   - Multi-criteria analysis of climate risks
   - Temporal sequencing of expected impacts
   - Uncertainty assessment and decision frameworks
   - Identification of critical intervention points

5. Adaptation Recommendations
   - Short-term (0-5 years) priority actions
   - Medium-term (5-15 years) strategic measures
   - Long-term (15+ years) transformational changes
   - Funding mechanisms and implementation pathways

FORMAT: Comprehensive assessment with executive summary, detailed analysis sections, clear visualizations of risk areas, and prioritized recommendations with cost-benefit considerations.
```

### Sustainable Business Strategy

```
You are a sustainability consultant advising a medium-sized consumer packaged goods (CPG) company.

COMPANY PROFILE:
- $500M annual revenue, 800 employees
- Products: Household cleaning supplies, personal care items
- Operations: Manufacturing facilities in 3 locations, global supply chain
- Current sustainability initiatives: Basic recycling program, some energy efficiency measures
- Competitors are advancing sustainability claims and gaining market share
- Limited budget for sustainability investments ($2M for first year)
- CEO wants tangible results within 12-18 months

TASK: Develop a comprehensive 3-year sustainability strategy that balances environmental impact, business value, and feasible implementation.

STRATEGY COMPONENTS:
1. Materiality Assessment
   - Key environmental impact areas analysis
   - Stakeholder priority mapping
   - Competitive benchmark
   - Regulatory horizon scanning

2. Goal-Setting Framework
   - Recommended science-based targets
   - KPIs and measurement methodology
   - Phased implementation approach
   - Governance structure and accountability

3. Priority Initiatives
   - Product reformulation opportunities
   - Packaging redesign recommendations
   - Supply chain intervention points
   - Manufacturing process improvements
   - Circular economy opportunities

4. Business Integration Plan
   - Marketing and communications strategy
   - Procurement policy revisions
   - Employee engagement approach
   - R&D integration methods
   - Capital expenditure framework

5. Implementation Roadmap
   - Quick-win opportunities (0-6 months)
   - Medium-term initiatives (6-18 months)
   - Long-term transformation (18-36 months)
   - Resource requirements and ROI projections

DELIVERABLES:
1. Executive summary with business case
2. Detailed strategy document with implementation timeline
3. Budget allocation recommendations
4. Risk assessment and mitigation strategies
5. Performance dashboard template for tracking progress

CONSTRAINTS:
- Initiatives must not increase product costs by more than 5%
- Strategy must include both operational and product-focused elements
- All major recommendations need ROI calculations
- Approach must align with relevant UN Sustainable Development Goals
```

## Engineering & Manufacturing

### Manufacturing Process Optimization

```
You are a process engineering consultant specializing in lean manufacturing.

TASK: Analyze the following production line data and develop recommendations to improve efficiency, reduce waste, and increase throughput.

FACILITY CONTEXT:
- Automotive parts manufacturing plant
- Production line assembling electronic control modules
- 2 shifts per day, 5 days per week
- 12 workstations with varying cycle times
- Current output: 520 units per day
- Target output: 650+ units per day without additional capital investment
- Quality issues at final testing: 8% rejection rate

CURRENT METRICS:
- Takt time: 110 seconds
- Bottleneck station cycle time: 128 seconds
- Average changeover time: 45 minutes
- Overall Equipment Effectiveness (OEE): 72%
- Unplanned downtime: 85 minutes per shift
- Work-In-Process inventory: Average 2.3 days of production
- Defect categories: Soldering issues (40%), component misalignment (25%), connector failures (20%), other (15%)

ANALYSIS REQUIREMENTS:
1. Line Balancing Assessment
   - Station-by-station analysis
   - Identification of bottlenecks and constraints
   - Labor utilization evaluation
   - Work distribution optimization

2. Waste Identification
   - Value stream mapping analysis
   - Seven wastes categorization
   - Root cause analysis of primary issues
   - Prioritization framework for improvements

3. Quality Improvement
   - Defect pattern analysis
   - Mistake-proofing opportunities
   - Inspection process evaluation
   - Statistical process control recommendations

4. Implementation Plan
   - Quick wins (implementable within 30 days)
   - Medium-term improvements (30-90 days)
   - Long-term recommendations (90+ days)
   - Required resources and projected benefits

DELIVERABLES:
1. Comprehensive analysis of current state with key findings
2. Specific recommendations with estimated impact
3. Implementation roadmap with prioritization
4. Performance metrics framework for tracking improvements
5. Training requirements for sustaining changes

CONSTRAINTS:
- Minimal capital expenditure (under $50,000)
- Must maintain or improve current quality levels
- Cannot reduce current staffing levels
- Implementation must not interrupt current production schedule
```

### Engineering Design Requirements

```
You are a systems engineer leading the requirements definition phase for a new industrial control system.

PROJECT CONTEXT:
- Replacement system for an aging manufacturing control platform
- Will monitor and control 200+ sensors and 150+ actuators
- Critical safety systems for hazardous material handling
- Must integrate with existing MES and ERP systems
- 15-year expected system lifespan
- Regulatory compliance with IEC 61511 and FDA 21 CFR Part 11

TASK: Develop a comprehensive requirements document for the new control system that can be used for vendor evaluation and system design.

REQUIREMENTS CATEGORIES:
1. Functional Requirements
   - Control capabilities and algorithms
   - Monitoring parameters and thresholds
   - Alarm management functionality
   - Data collection and historization
   - Reporting and analytics features
   - User interface requirements
   - Security features and access controls

2. Performance Requirements
   - System response times
   - Data processing volumes
   - Concurrent user capacity
   - Availability and reliability metrics
   - Recovery time objectives
   - Scalability parameters

3. Interface Requirements
   - Communication protocols
   - Integration specifications for existing systems
   - User interface standards
   - External system connectivity
   - Data exchange formats

4. Non-functional Requirements
   - Regulatory compliance specifications
   - Validation and qualification needs
   - Documentation requirements
   - Training specifications
   - Support and maintenance parameters
   - Disaster recovery capabilities

5. Constraints and Limitations
   - Budget constraints
   - Implementation timeline
   - Physical installation parameters
   - Operational environment considerations
   - Legacy system compatibility requirements
   - Vendor qualification requirements

FORMAT: IEEE 29148:2018 compliant requirements document with clear, testable, and traceable requirements statements. Each requirement should be uniquely identified, categorized, prioritized, and include verification criteria.
```

## Creative Writing & Fiction

### Character Development Framework

```
You are a literary consultant helping an author develop complex, believable characters for a novel.

PROJECT CONTEXT:
- Literary fiction novel set in a small coastal town during economic decline
- Themes of family secrets, environmental change, and community resilience
- Author wants characters that avoid stereotypes while feeling authentic

TASK: Create a detailed character development framework for the protagonist and two supporting characters.

PROTAGONIST:
- Female marine biologist who returns to hometown after 15 years
- Mid-40s, divorced, no children
- Conflicted relationship with hometown and family history
- Professional success contrasted with personal uncertainty

SUPPORTING CHARACTER 1:
- Protagonist's estranged father, former fishing boat captain
- Now dealing with financial hardship and health issues
- Keeper of family and town secrets

SUPPORTING CHARACTER 2:
- Local environmental activist with complicated motivations
- Has history with both protagonist and her father
- Represents both antagonistic and collaborative forces in the story

DEVELOPMENT FRAMEWORK COMPONENTS:
1. Psychological Profile
   - Core motivations and fears
   - Internal contradictions and tensions
   - Coping mechanisms and defense strategies
   - Value systems and moral framework
   - Growth arc possibilities

2. Relational Dynamics
   - Character relationship mapping
   - Power dynamics and conflict sources
   - Communication patterns
   - Unresolved tensions
   - Evolution of relationships throughout narrative

3. Backstory Development
   - Formative experiences and trauma
   - Cultural and socioeconomic influences
   - Education and career trajectory
   - Past relationships and their impacts
   - Connection to setting and place

4. External Manifestations
   - Speech patterns and dialogue tendencies
   - Physical characteristics and embodiment of traits
   - Environmental interactions
   - Habits and routines
   - Clothing and personal aesthetic choices

5. Character Arc Mapping
   - Starting state and vulnerabilities
   - Key decision points and challenges
   - Transformative moments
   - Resolution possibilities
   - Thematic significance of character journey

DELIVERABLES:
1. Detailed character profiles using the framework
2. Scene suggestions that reveal character depths
3. Dialogue samples showing distinct voices
4. Internal monologue examples for the protagonist
5. Character-driven subplot recommendations

FORMAT: Comprehensive character development guide with practical writing exercises and examples to help the author implement these character dimensions in their manuscript.
```

### Screenplay Structure Analysis

```
You are a script consultant helping a screenwriter analyze and improve their feature film screenplay.

SCREENPLAY DETAILS:
- Genre: Psychological thriller with science fiction elements
- Premise: A memory researcher discovers a way to identify false memories but uncovers a conspiracy when applying the technique to her own past
- Current draft: 118 pages, completed but with structure and pacing issues
- Target audience: Adult fans of cerebral sci-fi thrillers
- Comparable films: Inception, Eternal Sunshine of the Spotless Mind, Memento

TASK: Provide a comprehensive structure analysis with specific recommendations for revision.

ANALYSIS COMPONENTS:
1. Story Structure Evaluation
   - Beat sheet analysis using traditional three-act structure
   - Identification of key plot points and their timing
   - Assessment of subplot integration
   - Narrative momentum and pacing evaluation
   - Structural weaknesses and opportunities

2. Character Arc Assessment
   - Protagonist journey mapping
   - Character motivation clarity
   - Relationship development progression
   - Character transformation believability
   - Supporting character functionality

3. Thematic Development
   - Central theme identification and expression
   - Thematic consistency and development
   - Symbolism and motif effectiveness
   - Subtext analysis
   - Thematic resolution evaluation

4. Scene-Level Analysis
   - Scene purpose and necessity assessment
   - Tension and conflict evaluation
   - Scene length and pacing review
   - Entrance and exit point effectiveness
   - Dialogue efficiency and subtext

5. Revision Recommendations
   - Structural reorganization suggestions
   - Scene addition, deletion, and combination recommendations
   - Character development enhancement opportunities
   - Dialogue revision guidelines
   - Visual storytelling improvement suggestions

DELIVERABLES:
1. Executive summary with key findings (1-2 pages)
2. Detailed structural analysis with page-specific notes
3. Character arc mapping with improvement suggestions
4. Scene-by-scene evaluation highlighting strengths and weaknesses
5. Prioritized revision plan with specific action items

FORMAT: Provide a constructive, detailed analysis that acknowledges the screenplay's strengths while offering specific, actionable revision suggestions that maintain the writer's original vision and voice.
```

## Psychology & Mental Health

### Therapeutic Intervention Planning

```
You are a clinical psychologist developing a treatment plan for a client with anxiety and work-related stress.

CLIENT PROFILE:
- 34-year-old marketing executive
- Presenting issues: panic attacks, insomnia, work performance anxiety
- Symptoms began 8 months ago after promotion to management position
- No previous mental health treatment history
- Moderately high functioning despite symptoms
- Motivations: maintain career success, improve work-life balance, reduce physical symptoms
- Support system: supportive partner, limited social connections outside work
- Medical considerations: ruled out medical causes, no current medications

TASK: Develop a comprehensive 12-week cognitive-behavioral therapy (CBT) treatment plan.

TREATMENT PLAN COMPONENTS:
1. Assessment and Baseline
   - Recommended assessment tools and measures
   - Symptom tracking methodology
   - Functional analysis approach
   - Treatment goals and success metrics

2. Session-by-Session Outline
   - Session themes and objectives
   - Specific therapeutic techniques for each session
   - Homework assignments and between-session activities
   - Progress evaluation methods

3. Cognitive Interventions
   - Cognitive distortion identification techniques
   - Thought challenging protocols
   - Cognitive restructuring approaches
   - Mindfulness integration strategies

4. Behavioral Strategies
   - Relaxation and grounding techniques
   - Exposure hierarchy development
   - Behavioral activation approaches
   - Sleep hygiene interventions

5. Work-Specific Interventions
   - Boundary-setting strategies
   - Workplace communication skills
   - Performance anxiety management
   - Workload negotiation techniques

6. Relapse Prevention
   - Early warning sign identification
   - Coping skill maintenance plan
   - Support system engagement
   - Long-term wellness strategies

IMPORTANT CLINICAL CONSIDERATIONS:
- Focus on evidence-based practices
- Include both symptom reduction and functional improvement goals
- Incorporate client strengths and resources
- Address potential treatment barriers
- Consider cultural and contextual factors

FORMAT: Detailed treatment plan following standard clinical documentation practices with clear session objectives, specific interventions, and measurable outcome criteria.
```

### Psychological Research Methodology

```
You are a research methodologist consulting on the design of a psychology study.

RESEARCH TOPIC: The impact of social media use patterns on young adults' perceived social connection and loneliness.

RESEARCH TEAM: University psychology department with 2 faculty researchers, 3 graduate students, and research assistant support.

RESOURCES:
- Grant funding: $35,000
- Timeline: 12 months for data collection and analysis
- Access to university student population
- Online survey platforms and statistical software
- Lab space for in-person assessments if needed

TASK: Design a rigorous mixed-methods research study addressing this topic.

METHODOLOGY COMPONENTS:
1. Research Question Refinement
   - Primary and secondary research questions
   - Operational definitions of key constructs
   - Hypothesis formulation
   - Theoretical framework alignment

2. Study Design
   - Quantitative methods specification
   - Qualitative methods integration
   - Longitudinal vs. cross-sectional considerations
   - Control and comparison group strategies
   - Variables and measurement approach

3. Sampling Strategy
   - Target population definition
   - Sample size determination with power analysis
   - Recruitment methodology
   - Inclusion/exclusion criteria
   - Diversity and representation considerations

4. Data Collection Methods
   - Survey instruments with psychometric properties
   - Experience sampling methodology
   - Qualitative interview protocol
   - Behavioral data collection from devices (if applicable)
   - Timeline and sequence of measurements

5. Analysis Plan
   - Statistical analyses for quantitative data
   - Qualitative analysis approach
   - Mixed methods integration strategy
   - Anticipated challenges and contingencies
   - Software and tools required

6. Ethical Considerations
   - Potential risks and mitigation strategies
   - Informed consent procedures
   - Data privacy and security measures
   - Debriefing protocol
   - IRB submission guidelines

DELIVERABLES:
1. Comprehensive research protocol
2. Statistical power analysis justification
3. Timeline with key milestones
4. Budget allocation recommendations
5. Anticipated limitations and mitigation strategies

FORMAT: Detailed research methodology that would satisfy peer review for publication in a reputable psychology journal, with clear justifications for methodological choices.
```

## Public Policy & Governance

### Policy Brief Development

```
You are a policy analyst at a think tank focused on education innovation.

TASK: Create a comprehensive policy brief on implementing educational technology in underserved K-12 school districts.

POLICY CONTEXT:
- National debate on digital divide in education
- Uneven access to educational technology across socioeconomic groups
- Recent federal funding initiative for educational infrastructure
- Concerns about screen time and effective technology integration
- Teacher training gaps for technology implementation
- Mixed evidence on educational outcomes from technology programs

TARGET AUDIENCE: State-level education policymakers and district administrators

POLICY BRIEF COMPONENTS:
1. Executive Summary
   - Problem statement
   - Key findings
   - Principal recommendations
   - Implementation considerations

2. Background and Context
   - Current state of educational technology access
   - Research on educational technology effectiveness
   - Equity considerations and digital divide data
   - Stakeholder landscape analysis
   - Previous policy approaches and outcomes

3. Policy Options Analysis
   - Option 1: Infrastructure-focused approach
   - Option 2: Teacher training and support systems
   - Option 3: Curriculum and content development
   - Option 4: Comprehensive integrated approach
   - Comparative analysis of advantages, limitations, costs, and feasibility

4. Recommended Policy Framework
   - Core policy components
   - Funding mechanisms and resource allocation
   - Implementation timeline and phases
   - Roles and responsibilities
   - Accountability measures
   - Cross-sector collaboration opportunities

5. Implementation Roadmap
   - Short-term actions (0-12 months)
   - Medium-term development (1-3 years)
   - Long-term sustainability (3+ years)
   - Potential obstacles and mitigation strategies
   - Success metrics and evaluation framework

DELIVERABLES:
1. 8-10 page policy brief with executive summary
2. Data visualizations of key statistics
3. Case studies of successful implementations
4. Cost-benefit analysis of recommendations
5. Stakeholder impact assessment

FORMAT: Professional policy brief with clear, evidence-based recommendations, actionable implementation steps, and consideration of political and practical constraints.
```

### Program Evaluation Framework

```
You are a public sector evaluation specialist developing an evaluation framework for a new government workforce development program.

PROGRAM CONTEXT:
- Recently launched workforce initiative targeting unemployed individuals in economically distressed regions
- Three-pronged approach: technical skills training, soft skills development, and job placement services
- 12-month program with cohort-based enrollment
- $15 million annual budget across 5 pilot locations
- Goals: 70% job placement rate, 60% retention after 6 months, average wage increase of 20%
- Multiple stakeholders: federal funders, state administrators, local providers, employers, participants

TASK: Design a comprehensive program evaluation framework that addresses process, outcomes, and impact.

EVALUATION FRAMEWORK COMPONENTS:
1. Evaluation Purpose and Questions
   - Primary evaluation objectives
   - Key evaluation questions by stakeholder group
   - Performance metrics alignment with program goals
   - Learning agenda for program improvement

2. Methodology Design
   - Mixed-methods approach specification
   - Data collection timeline and frequency
   - Comparison group strategy
   - Sampling methodology for qualitative components
   - Demographic and subgroup analysis plan

3. Data Collection Infrastructure
   - Quantitative tracking metrics and systems
   - Qualitative assessment tools
   - Participant feedback mechanisms
   - Employer engagement measurement
   - Cost tracking and return on investment analysis

4. Analysis and Interpretation Plan
   - Statistical analysis approach for outcome data
   - Qualitative analysis methodology
   - Contribution analysis framework
   - Contextual factors consideration
   - Performance threshold definitions

5. Reporting and Utilization Strategy
   - Reporting frequency and formats by audience
   - Data visualization approach
   - Continuous improvement feedback loops
   - Milestone decision points
   - Knowledge dissemination plan

6. Implementation Considerations
   - Evaluation staffing and responsibilities
   - Timeline for evaluation activities
   - Budget allocation for evaluation components
   - Data privacy and ethical considerations
   - Potential evaluation challenges and mitigation strategies

DELIVERABLES:
1. Comprehensive evaluation plan with logic model
2. Detailed indicator matrix with data sources
3. Data collection instruments and protocols
4. Analysis plan with methodological justification
5. Reporting templates for different stakeholders

FORMAT: Professional evaluation framework that follows American Evaluation Association guidelines with clear methodology, practical implementation guidance, and utilization-focused approach.
```

## Language Learning & Translation

### Language Curriculum Design

```
You are a language education specialist designing a curriculum for adult learners of Spanish at the intermediate level.

LEARNER PROFILE:
- Professional adults (30-55 years old)
- Completed beginner Spanish course (A2 level on CEFR scale)
- Goals: Business communication, travel confidence, cultural competence
- Available time: 2 hours classroom + 3 hours self-study weekly
- Program length: 16-week semester
- Learning context: Corporate language program with both in-person and online components

TASK: Design a comprehensive Spanish curriculum that will advance learners to solid B1/early B2 level.

CURRICULUM COMPONENTS:
1. Learning Objectives
   - Language competency goals by skill area (speaking, listening, reading, writing)
   - Functional communication abilities to be developed
   - Grammar and vocabulary targets
   - Cultural knowledge objectives
   - Measurable outcomes for assessment

2. Content Organization
   - Thematic units with business and travel focus
   - Grammar progression sequence
   - Vocabulary building strategy
   - Cultural elements integration
   - Authentic materials selection criteria

3. Methodological Approach
   - Communicative language teaching techniques
   - Task-based learning activities
   - Flipped classroom components
   - Technology integration plan
   - Differentiation strategies for varied learning styles

4. Assessment Framework
   - Formative assessment tools
   - Performance-based evaluation criteria
   - Self-assessment mechanisms
   - Progress tracking methodology
   - Final proficiency measurement

5. Materials and Resources
   - Core textbook recommendations
   - Supplementary resource curation
   - Digital tool integration
   - Authentic media selection
   - Self-study resource development

DELIVERABLES:
1. 16-week curriculum outline with weekly objectives
2. Sample lesson plans for three representative sessions
3. Assessment rubrics and example activities
4. Technology and resource recommendations
5. Self-study guide for learners

FORMAT: Detailed curriculum plan following ACTFL standards with clear progression, communicative focus, and practical application opportunities for busy adult learners.
```

### Translation Style Guide

```
You are a localization manager developing guidelines for translating marketing content for a global technology company.

COMPANY CONTEXT:
- B2B software company expanding from US market to Europe and Asia
- Product: Enterprise cloud security solution
- Brand voice: Expert, innovative, trustworthy, but approachable
- Target markets for initial expansion: Germany, France, Japan, and Brazil
- Content types: Website, product interface, technical documentation, marketing materials, and customer support

TASK: Create a comprehensive translation style guide to ensure consistent, culturally appropriate localization across markets.

STYLE GUIDE COMPONENTS:
1. Brand Voice Localization
   - Core brand attributes and their cultural adaptation
   - Market-specific tone considerations
   - Formality level guidelines by country and context
   - Cultural taboos and sensitivities by market
   - Technical voice adaptation for different content types

2. Language-Specific Guidelines
   - Country-specific language variants (e.g., Brazilian vs. European Portuguese)
   - Technical terminology consistency
   - Industry jargon handling approach
   - Idioms and metaphors adaptation strategy
   - Cultural reference substitution guidelines

3. Content Type Specifications
   - Website localization priorities and constraints
   - UI text character limitations and considerations
   - Marketing material adaptation guidelines
   - Technical documentation precision requirements
   - Support content clarity standards

4. Formatting and Visual Elements
   - Date, time, and number formats by locale
   - Currency and unit conversion standards
   - Image and iconography cultural considerations
   - Color symbolism awareness by market
   - Typography and text expansion accommodation

5. Quality Assurance Process
   - Translation review criteria
   - Linguistic quality assessment methodology
   - Market review requirements
   - Glossary and terminology management
   - Continuous improvement feedback loop

DELIVERABLES:
1. Master style guide with general principles
2. Market-specific supplements for each target country
3. Content type-specific guidelines and examples
4. Terminology glossary structure and governance
5. QA checklist and evaluation criteria

FORMAT: Comprehensive style guide with clear examples, market-specific considerations, and practical guidance for translators and reviewers to maintain brand consistency while respecting cultural nuances.
```

## AI Ethics & Responsible Use

### Responsible AI Framework

```
You are an AI ethics consultant developing guidelines for a healthcare organization implementing AI-based diagnostic tools.

ORGANIZATION CONTEXT:
- Large hospital network evaluating AI tools for radiology, pathology, and patient risk assessment
- Serves diverse patient population including vulnerable and underserved communities
- Subject to HIPAA and other healthcare regulations
- Mixed technical expertise among staff and leadership
- No formal AI governance structure currently in place

TASK: Create a comprehensive responsible AI framework that addresses ethical, legal, and practical considerations of healthcare AI implementation.

FRAMEWORK COMPONENTS:
1. Governance Structure
   - AI ethics committee composition and responsibilities
   - Decision-making authority and escalation paths
   - Stakeholder representation requirements
   - Review and approval processes
   - Integration with existing clinical governance

2. Ethical Principles and Standards
   - Core ethical principles for healthcare AI
   - Fairness and bias mitigation requirements
   - Transparency and explainability standards
   - Privacy and data protection guidelines
   - Human oversight and intervention parameters
   - Reliability and safety thresholds

3. Risk Assessment Methodology
   - AI system risk categorization framework
   - Impact assessment process
   - Bias and fairness evaluation methods
   - Clinical validation requirements by risk level
   - Ongoing monitoring protocols

4. Implementation Guidelines
   - Procurement and vendor assessment criteria
   - Testing and validation requirements
   - Clinician training and change management
   - Patient communication and consent practices
   - Incident response procedures
   - Documentation requirements

5. Continuous Evaluation
   - Performance monitoring metrics
   - Feedback collection mechanisms
   - Regular audit requirements
   - Updating and retraining protocols
   - Sunset criteria for retiring AI systems

DELIVERABLES:
1. Comprehensive framework document with principles and processes
2. Implementation roadmap with phased approach
3. Assessment tools and templates
4. Training materials for key stakeholders
5. Governance structure recommendations

FORMAT: Detailed yet practical framework that addresses both high-level ethical principles and specific implementation guidance, with healthcare-specific considerations throughout.
```

### Algorithm Bias Assessment

```
You are a data ethics specialist conducting a fairness assessment of a hiring algorithm for a large corporation.

ALGORITHM CONTEXT:
- Machine learning system that screens résumés and ranks candidates
- Used for initial filtering of high-volume job applications
- Trained on historical hiring data from the past 8 years
- Evaluates approximately 50 features from applications
- Currently implemented for entry and mid-level positions
- Company is concerned about potential bias and compliance issues

TASK: Design a comprehensive methodology for assessing and mitigating algorithmic bias in this hiring system.

ASSESSMENT FRAMEWORK:
1. Data Audit and Analysis
   - Historical data representation assessment
   - Protected attribute identification
   - Proxy variable detection methodology
   - Data quality and completeness evaluation
   - Temporal pattern analysis

2. Fairness Metrics and Testing
   - Appropriate fairness metrics selection
   - Disparate impact measurement approach
   - Statistical significance testing methodology
   - Intersectional analysis framework
   - Benchmark comparison strategy

3. Bias Mitigation Strategy
   - Pre-processing interventions
   - In-processing algorithm modifications
   - Post-processing correction techniques
   - Data augmentation recommendations
   - Model architecture reconsideration

4. Human-in-the-Loop Integration
   - Human oversight mechanisms
   - Decision review thresholds
   - Appeal process design
   - Edge case handling protocols
   - Intervention documentation requirements

5. Monitoring and Governance
   - Ongoing measurement framework
   - Regular audit schedule and methodology
   - Feedback incorporation process
   - Model updating guidelines
   - Compliance documentation standards
   - Stakeholder review requirements

DELIVERABLES:
1. Detailed assessment methodology
2. Analysis results with visualizations and key findings
3. Bias mitigation recommendations with prioritization
4. Implementation roadmap for improvements
5. Monitoring plan and governance recommendations

LEGAL AND ETHICAL CONSIDERATIONS:
- Compliance with EEOC guidelines and relevant legislation
- Balance between fairness and utility
- Transparency to candidates
- Responsible transition management
- Documentation for potential regulatory review

FORMAT: Comprehensive technical assessment with clear methodology, specific findings, and actionable recommendations that are both technically sound and organizationally feasible.
```

### Multi-Agent Simulation Framework

```
TASK: Create a multi-agent simulation to analyze a complex problem with multiple stakeholders and competing interests.

SIMULATION CONTEXT:
[Describe the specific problem domain, key stakeholders, and system dynamics]

FRAMEWORK INSTRUCTIONS:
1. You will simulate multiple expert agents with different perspectives and roles
2. Each agent should have distinct:
   - Professional background and expertise
   - Value system and priorities
   - Information access and blind spots
   - Communication style and terminology

3. For each simulation round:
   - Present the current scenario state
   - Allow each agent to analyze from their perspective
   - Facilitate agent interactions and negotiations
   - Document points of consensus and disagreement
   - Evolve the scenario based on collective input

4. Each agent should:
   - Stay consistently in character
   - Apply domain-specific reasoning
   - Acknowledge limitations of their perspective
   - Respond to other agents' points
   - Propose concrete solutions or next steps

5. Conclude with:
   - Synthesis of key insights from multiple perspectives
   - Identification of critical tensions or tradeoffs
   - Recommended path forward with rationale
   - Reflection on limitations of the simulation

AGENTS TO SIMULATE:
[List 3-5 specific expert roles relevant to your problem]

INITIAL SCENARIO DESCRIPTION:
[Provide the starting conditions and key question to address]
```

### Systems Thinking Analysis

```
TASK: Apply a systems thinking approach to analyze a complex problem and develop holistic solutions.

SYSTEM CONTEXT:
[Describe the specific system, its boundaries, and the problem to be analyzed]

ANALYSIS FRAMEWORK:
1. System Mapping
   - Identify key elements and stakeholders
   - Map relationships and feedback loops
   - Determine system boundaries
   - Identify stocks and flows
   - Document existing equilibrium states

2. Pattern Analysis
   - Historical behavior patterns
   - Recurring dynamics and cycles
   - Time delays and their effects
   - Growth and limiting factors
   - Leverage points within the system

3. Mental Model Examination
   - Prevailing assumptions and paradigms
   - Cognitive biases affecting perception
   - Competing narratives about the system
   - Values and goals of different stakeholders
   - Unstated rules governing behavior

4. Intervention Design
   - High-leverage intervention points
   - Potential unintended consequences
   - Implementation feasibility assessment
   - Short and long-term impact projection
   - Adaptive management strategies

5. Implementation and Learning Framework
   - Monitoring indicators for system change
   - Feedback collection mechanisms
   - Adaptation triggers and processes
   - Stakeholder engagement strategy
   - Continuous learning approach

DELIVERABLES:
1. Visual system map with key relationships
2. Analysis of current system behavior and dynamics
3. Identification of high-leverage intervention points
4. Portfolio of potential interventions with projected impacts
5. Implementation strategy with learning feedback loops

SPECIFIC PROBLEM TO ANALYZE:
[Provide the particular challenge within this system to focus on]
```

### Knowledge Synthesis Framework

```
TASK: Synthesize diverse perspectives on a complex topic to create a comprehensive knowledge base.

TOPIC:
[Specify the topic or question for knowledge synthesis]

SYNTHESIS FRAMEWORK:
1. Perspective Mapping
   - Identify major schools of thought
   - Map theoretical frameworks and their evolution
   - Document core disagreements and their bases
   - Outline methodological approaches by tradition
   - Highlight interdisciplinary intersections

2. Evidence Assessment
   - Evaluate research quality and methodology
   - Compare empirical findings across studies
   - Identify data gaps and limitations
   - Assess generalizability of findings
   - Analyze conflicting evidence and explanations

3. Integration Analysis
   - Find common ground across perspectives
   - Identify complementary insights
   - Resolve apparent contradictions
   - Develop integrated frameworks
   - Create conceptual bridges between disciplines

4. Contextual Considerations
   - Historical developments in understanding
   - Cultural and geographic variations
   - Temporal changes in consensus
   - Emerging trends and directions
   - Practical applications of theoretical knowledge

5. Knowledge Map Creation
   - Core principles with broad agreement
   - Spectrum of perspectives on key questions
   - Outstanding questions and research frontiers
   - Practical implications of current knowledge
   - Future research directions

DELIVERY FORMAT:
1. Executive summary of key insights
2. Structured knowledge map with relationships
3. Comparative analysis of major perspectives
4. Assessment of evidence quality and consensus
5. Practical implications and applications
6. Future research priorities

SPECIFIC SYNTHESIS FOCUS:
[Provide particular aspects or questions to emphasize]
```

### Creative Problem-Solving Process

```
TASK: Apply a structured creative problem-solving approach to generate innovative solutions for a specific challenge.

CHALLENGE CONTEXT:
[Describe the problem situation, constraints, and objectives]

CREATIVE PROCESS FRAMEWORK:
1. Problem Exploration
   - Challenge mapping and framing
   - Stakeholder perspective analysis
   - Current solution assessment
   - Constraint identification and classification
   - Root cause exploration

2. Divergent Thinking Phase
   - Analogical thinking from diverse domains
   - First principles reasoning
   - Provocation and assumption challenging
   - Random stimulus incorporation
   - Quantity-focused ideation techniques

3. Idea Development
   - Concept combination and evolution
   - Rapid prototyping approaches
   - Constraint satisfaction strategies
   - Feasibility enhancement techniques
   - Impact amplification methods

4. Convergent Evaluation
   - Multi-criteria assessment framework
   - Stakeholder impact analysis
   - Implementation feasibility evaluation
   - Risk and limitation identification
   - Potential unintended consequences

5. Implementation Planning
   - Prototype and testing approach
   - Stakeholder engagement strategy
   - Resource requirement assessment
   - Timeline and milestone development
   - Feedback collection and iteration plan

DELIVERABLES:
1. Reframed problem statement with insights
2. Diverse solution concepts (minimum 10)
3. 3-5 developed solution proposals
4. Evaluation matrix with recommendations
5. Implementation roadmap for top solution(s)

SPECIFIC CREATIVE CONSTRAINTS:
[List any particular approaches, restrictions, or focus areas for solutions]
```
