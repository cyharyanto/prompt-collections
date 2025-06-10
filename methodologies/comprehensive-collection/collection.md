# Problem-Solving Methodology Templates

## 🔹 SURFACE-LEVEL METHODS

### 1. Five Whys Analysis Template

**Problem Statement**: [Define the problem you're investigating]

**Instructions**: For each "Why" below, provide a specific, factual answer. Avoid vague responses like "poor management" or "lack of resources." Focus on observable, actionable causes.

**Why 1:** Why did [problem] occur?  
Answer: 

**Why 2:** Why did [answer from Why 1] happen?  
Answer: 

**Why 3:** Why did [answer from Why 2] happen?  
Answer: 

**Why 4:** Why did [answer from Why 3] happen?  
Answer: 

**Why 5:** Why did [answer from Why 4] happen?  
Answer: 

**Root Cause Identified:**

**Actionable Solutions:**
1.
2.
3.

**Validation Questions:**
- Can we prevent the problem by addressing this root cause?
- Are there other contributing factors we haven't explored?
- What evidence supports our root cause hypothesis?

### 2. Fishbone/Ishikawa Diagram Template

**FISHBONE ANALYSIS PROMPT**

Problem/Effect: [State the problem at the "head" of the fish]

For each category below, brainstorm potential causes. Think systematically about each area:

**PEOPLE (Human Factors)**
- Skills/Training:
- Motivation:
- Communication:
- Workload:

**PROCESS (Methods/Procedures)**
- Standard procedures:
- Documentation:
- Workflow:
- Decision-making:

**MATERIALS (Inputs/Resources)**
- Quality of inputs:
- Availability:
- Specifications:
- Storage/handling:

**MACHINES (Equipment/Technology)**
- Equipment condition:
- Capacity:
- Maintenance:
- Technology limitations:

**ENVIRONMENT (Physical/Organizational)**
- Physical conditions:
- Organizational culture:
- External factors:
- Regulatory environment:

**MEASUREMENT (Data/Metrics)**
- Data accuracy:
- Measurement methods:
- Feedback systems:
- Performance indicators:

**SYNTHESIS:**
- Which causes appear in multiple categories?
- What are the top 3 most likely root causes?
- How do these causes interact with each other?

### 3. FMEA (Failure Mode and Effects Analysis) Template

**FMEA ANALYSIS PROMPT**

System/Process: [Define the system or process being analyzed]

For each component/step, complete the following analysis:

**Component/Step 1:** [Name]
- **Function:** What is this supposed to do?
- **Potential Failure Mode:** How could it fail?
- **Potential Effects:** What happens if it fails?
- **Severity (1-10):** How bad is the effect?
- **Potential Causes:** Why might it fail?
- **Occurrence (1-10):** How likely is this failure?
- **Current Controls:** What prevents/detects this failure?
- **Detection (1-10):** How well can we detect it?
- **RPN (Risk Priority Number):** Severity × Occurrence × Detection
- **Recommended Actions:** What should we do?

**Repeat for each component/step**

**PRIORITIZATION:**
- List all failure modes by RPN (highest first)
- Focus improvement efforts on top 20% of RPNs
- Develop action plans for high-risk items

**VALIDATION:**
- How will you verify improvements?
- What monitoring will you implement?

### 4. Pareto Analysis Template

**PARETO ANALYSIS PROMPT**

Problem Category: [Define what you're analyzing - defects, complaints, costs, etc.]

**Step 1: Data Collection**
List all categories and their frequency/impact:
1. [Category]: [Count/Value]
2. [Category]: [Count/Value]
3. [Category]: [Count/Value]
[Continue for all categories]

**Step 2: Ranking and Cumulative Analysis**
Rank categories from highest to lowest impact:
1. [Category]: [Value] - [% of total] - [Cumulative %]
2. [Category]: [Value] - [% of total] - [Cumulative %]
3. [Category]: [Value] - [% of total] - [Cumulative %]

**Step 3: 80/20 Identification**
- Which categories contribute to 80% of the problem?
- What percentage of categories cause 80% of issues?

**Step 4: Action Planning**
- Focus Areas (top 20% of categories):
- Resource Allocation Strategy:
- Expected Impact of addressing vital few:
- Monitoring approach for "useful many":

**Insights:**
- What patterns emerge from this analysis?
- Are there underlying causes connecting the vital few?

### 5. PDCA (Plan-Do-Check-Act) Template

**PDCA CYCLE PROMPT**

**PLAN Phase:**
- **Problem Definition:** What exactly needs improvement?
- **Current State Analysis:** What's happening now?
- **Goal Setting:** What do we want to achieve?
- **Root Cause Hypothesis:** What do we think is causing the problem?
- **Proposed Solution:** What will we try?
- **Success Metrics:** How will we measure success?
- **Implementation Plan:** Who, what, when, where?

**DO Phase:**
- **Implementation Log:** What was actually done?
- **Deviations from Plan:** What went differently than expected?
- **Data Collection:** What data was gathered?
- **Observations:** What did we notice during implementation?

**CHECK Phase:**
- **Results Analysis:** What were the outcomes?
- **Goal Achievement:** Did we meet our targets?
- **Unexpected Results:** What surprised us?
- **Learning:** What did we learn about the problem/solution?

**ACT Phase:**
- **Decision:** Adopt, adapt, or abandon the solution?
- **Standardization:** If successful, how will we make this standard?
- **Next Cycle Planning:** What should we improve next?
- **Knowledge Sharing:** How will we share learnings?

## 🔸 MID-LEVEL METHODS

### 6. Root Cause Analysis (RCA) Template

**COMPREHENSIVE ROOT CAUSE ANALYSIS PROMPT**

**Problem Definition Phase:**
- **Problem Statement:** [Specific, measurable description]
- **Impact:** What are the consequences?
- **Scope:** Where and when does this occur?
- **Stakeholders Affected:** Who is impacted?

**Data Collection Phase:**
- **Timeline:** When did the problem first appear?
- **Frequency:** How often does it occur?
- **Patterns:** Are there trends or cycles?
- **Evidence:** What data supports the problem existence?

**Causal Analysis Phase:**
Apply multiple techniques:

**Technique 1: Categorical Analysis**
- Immediate Causes (symptoms):
- Intermediate Causes (contributing factors):
- Root Causes (fundamental issues):

**Technique 2: Systems Thinking**
- Inputs that contribute:
- Process factors:
- Output variations:
- Feedback loops:

**Technique 3: Human Factors**
- Individual factors:
- Team/group factors:
- Organizational factors:
- Cultural factors:

**Solution Development:**
- **For Each Root Cause:**
  - Proposed solution:
  - Implementation difficulty:
  - Expected effectiveness:
  - Resource requirements:

**Validation:**
- How will you test if root causes are correct?
- What pilot approach will you use?

### 7. Systems Mapping/Causal Loop Diagrams Template

**SYSTEMS MAPPING PROMPT**

**System Definition:**
- **System Purpose:** What is this system designed to achieve?
- **System Boundaries:** What's included/excluded?
- **Key Stakeholders:** Who are the main actors?

**Element Identification:**
- **Variables:** List key variables that change over time
- **Actors:** List entities that make decisions
- **Resources:** List what flows through the system
- **Constraints:** List what limits the system

**Relationship Mapping:**
For each pair of elements, ask:
- Does A influence B? How?
- Is the influence positive (+) or negative (-)?
- Is there a delay between cause and effect?
- What is the strength of the relationship?

**Loop Identification:**
- **Reinforcing Loops (R):** What creates exponential growth/decline?
- **Balancing Loops (B):** What creates stability/resistance?
- **Dominant Loops:** Which loops currently drive system behavior?

**Leverage Points Analysis:**
Rate each potential intervention point (1-10 scale):
- **Parameters:** Changing numbers/subsidies/taxes
- **Material Flows:** Changing structure of information flows
- **Rules:** Changing rules of the system
- **Power Distribution:** Who gets to make the rules
- **Goals:** The purpose/function of the system
- **Paradigms:** Shared ideas and assumptions
- **Transcending Paradigms:** Not being attached to any worldview

**Insights:**
- What unintended consequences might emerge?
- Where are the highest leverage intervention points?
- What mental models need to change?

### 8. TRIZ Template

**TRIZ PROBLEM-SOLVING PROMPT**

**Step 1: Problem Formulation**
- **Technical System:** What system are we improving?
- **Primary Function:** What should the system do?
- **Harmful Function:** What unwanted effects occur?
- **Resources Available:** What can we use (time, space, materials, fields)?

**Step 2: Contradiction Identification**
- **Technical Contradiction:** When improving parameter A worsens parameter B
  - Improving Parameter: [What we want to improve]
  - Worsening Parameter: [What gets worse]
  
- **Physical Contradiction:** When system requires opposite states
  - Required State 1: [What system needs to be]
  - Required State 2: [What system also needs to be]
  - Separation Principle: [In time/space/condition]

**Step 3: TRIZ Principles Application**
Based on your contradiction, explore these inventive principles:

**For Technical Contradictions:**
- Segmentation: Divide into parts
- Asymmetry: Change from symmetric to asymmetric
- Merging/Consolidation: Combine similar objects
- Universality: Make multi-functional
- Nesting: Place inside another
- Weight Compensation: Compensate for weight
- Equipotentiality: Limit position changes needed
- Inversion: Invert the action
- Spheroidality: Use curves instead of straight lines
- Dynamics: Make adaptive/flexible
- Partial/Overdone Actions: Do more or less than needed
- Another Dimension: Use 3D space differently

**Step 4: Solution Concept Development**
- **Principle Applied:** Which TRIZ principle are you using?
- **Concept Description:** How does it work?
- **Implementation Approach:** How would you build this?
- **Resource Utilization:** What resources does it use?

**Step 5: Solution Evaluation**
- Does it resolve the contradiction?
- What new problems might emerge?
- How elegant/simple is the solution?

### 9. Theory of Constraints (TOC) Template

**THEORY OF CONSTRAINTS ANALYSIS PROMPT**

**Step 1: System Goal Definition**
- **System Purpose:** What is the goal of this system?
- **Success Metrics:** How do you measure goal achievement?
- **Current Performance:** Where are you now vs. goal?

**Step 2: Constraint Identification**
Map your process flow and identify:
- **Physical Constraints:** Equipment, facilities, materials
- **Market Constraints:** Customer demand, competition
- **Policy Constraints:** Rules, procedures, measurements
- **Paradigm Constraints:** Mental models, assumptions

**Current System Bottleneck:** [The constraint that most limits goal achievement]

**Step 3: Constraint Analysis**
**For the identified constraint:**
- **Capacity:** What is maximum throughput?
- **Current Utilization:** How much is actually used?
- **Waste/Inefficiency:** What reduces effective capacity?
- **Dependencies:** What feeds this constraint?
- **Impact:** How does this constraint limit system goal?

**Step 4: Exploit the Constraint**
How can you get maximum value from the constraint without spending money?
- Eliminate idle time:
- Improve quality at constraint:
- Ensure optimal scheduling:
- Remove administrative burdens:

**Step 5: Subordinate Everything Else**
How should non-constraints support the constraint?
- Upstream processes:
- Downstream processes:
- Support functions:
- Performance measurements:

**Step 6: Elevate the Constraint**
If exploitation isn't enough, how will you increase constraint capacity?
- Investment options:
- Technology solutions:
- Process redesign:
- Additional resources:

**Step 7: Avoid Inertia**
Once this constraint is broken:
- What will become the new constraint?
- How will you identify it quickly?
- What assumptions need updating?

### 10. Kepner-Tregoe Template

**KEPNER-TREGOE DECISION ANALYSIS PROMPT**

**Decision Statement:** [What decision needs to be made?]

**Step 1: Establish Decision Objectives**
**MUSTS (Non-negotiable requirements):**
1. [Objective] - [Measurement criteria]
2. [Objective] - [Measurement criteria]
3. [Objective] - [Measurement criteria]

**WANTS (Desirable but not essential):**
1. [Objective] - [Weight 1-10] - [Measurement criteria]
2. [Objective] - [Weight 1-10] - [Measurement criteria]
3. [Objective] - [Weight 1-10] - [Measurement criteria]

**Step 2: Generate Alternatives**
List all viable options:
1. [Alternative 1]
2. [Alternative 2]
3. [Alternative 3]
[Continue as needed]

**Step 3: Evaluate Alternatives**

**MUST Analysis (Go/No-Go):**
| Alternative | Must 1 | Must 2 | Must 3 | Overall |
|-------------|---------|---------|---------|----------|
| Alt 1       | Go/No-Go| Go/No-Go| Go/No-Go| Go/No-Go |
| Alt 2       | Go/No-Go| Go/No-Go| Go/No-Go| Go/No-Go |

**WANT Analysis (for alternatives that passed MUST):**
| Alternative | Want 1 (Score × Weight) | Want 2 (Score × Weight) | Want 3 (Score × Weight) | Total |
|-------------|-------------------------|-------------------------|-------------------------|-------|
| Alt 1       | [Score 1-10] × [Weight] | [Score 1-10] × [Weight] | [Score 1-10] × [Weight] | [Sum] |
| Alt 2       | [Score 1-10] × [Weight] | [Score 1-10] × [Weight] | [Score 1-10] × [Weight] | [Sum] |

**Step 4: Risk Assessment**
For top alternatives, identify potential problems:
- **Alternative:** [Name]
- **Potential Problems:** 
  - Problem 1: [Description] - Probability: [H/M/L] - Impact: [H/M/L]
  - Problem 2: [Description] - Probability: [H/M/L] - Impact: [H/M/L]
- **Risk Mitigation:** How can you prevent/minimize these problems?

**Step 5: Final Decision**
- **Recommended Alternative:** [Based on analysis]
- **Rationale:** [Why this is the best choice]
- **Implementation Plan:** [Next steps]
- **Contingency Plans:** [What if risks materialize]

## 🔻 DEEP STRUCTURE METHODS

### 11. Dialectical Method (Hegelian) Template

**HEGELIAN DIALECTICAL ANALYSIS PROMPT**

**Dialectical Situation:** [Describe the contradictory situation you're analyzing]

**THESIS PHASE:**
- **Position Statement:** What is the dominant view/approach/system?
- **Core Assumptions:** What beliefs underlie this position?
- **Strengths:** What does this position do well?
- **Internal Logic:** How does this position justify itself?
- **Historical Context:** Where did this position come from?

**ANTITHESIS PHASE:**
- **Counter-Position:** What opposes or contradicts the thesis?
- **Fundamental Disagreement:** Where exactly do thesis and antithesis conflict?
- **Antithesis Strengths:** What valid points does the opposition make?
- **Limitations of Thesis:** What problems does the antithesis reveal?
- **Deeper Contradiction:** What fundamental tension is exposed?

**DIALECTICAL TENSION ANALYSIS:**
- **Nature of Contradiction:** Is this a logical, practical, or existential contradiction?
- **Stakes:** What is at risk if the contradiction remains unresolved?
- **False Resolutions:** What fake solutions have been tried?
- **Deeper Truth:** What truth is trying to emerge through this conflict?

**SYNTHESIS PHASE:**
- **Higher Unity:** How can both thesis and antithesis be preserved yet transcended?
- **New Framework:** What new way of thinking emerges?
- **Transformation:** How are both original positions changed in the synthesis?
- **Practical Implications:** How would this synthesis work in practice?
- **New Contradictions:** What tensions might emerge from this synthesis?

**VALIDATION:**
- Does the synthesis genuinely resolve the original contradiction?
- Does it preserve the essential truths of both thesis and antithesis?
- Does it open new possibilities for action/understanding?
- Is it a mere compromise or a genuine transcendence?

**RECURSIVE APPLICATION:**
- How might this synthesis become a new thesis?
- What might oppose this new thesis?
- What further development is possible?

### 12. Meta-Dialectical Methodology Template

**META-DIALECTICAL METHODOLOGY: A PRACTICAL FRAMEWORK**

**Decision Statement:** [What complex decision/problem are you addressing?]
**Importance Level:** [Routine/Significant/Strategic/Existential]
**Participants:** [Human decision-makers and AI tools involved]

**PHASE 1: ESTABLISH INITIAL THESIS**
**Core Position:**
- **Primary Thesis:** [Clear statement of initial position/proposed solution]
- **Key Assumptions:** [What beliefs underlie this position?]
- **Core Motivations:** [Why does this position appeal to you?]
- **Essential Tensions:** [What competing values/priorities are at play?]

**Constraints (Non-negotiable boundaries):**
- **Must Have:** [Requirements that cannot be compromised]
- **Must Avoid:** [Outcomes that are unacceptable]
- **Resource Limits:** [Time, money, people, or other constraints]
- **Stakeholder Requirements:** [Needs of key parties that must be met]

**PHASE 2: APPLY DEVIL'S ADVOCATE CHALLENGE**
**AI-Assisted Critique Prompt:**
"Act as a thoughtful critic of this position: [THESIS]
Identify:
1. Three implicit assumptions that might not hold
2. Two edge cases where this approach could fail  
3. One fundamental tension this position doesn't resolve
4. Context where this solution might cause unintended consequences
Explain each critique clearly, focusing on the strongest objections."

**Human Analysis:**
- **Assumption Challenges:** [Which assumptions feel most vulnerable?]
- **Failure Scenarios:** [Where could this approach break down?]
- **Unresolved Tensions:** [What contradictions remain?]
- **Constraint Violations:** [Does the thesis violate any constraints?]
- **Blind Spots:** [What perspectives might you be missing?]

**PHASE 3: STEELMAN THE ORIGINAL THESIS**
**AI-Assisted Strengthening Prompt:**
"The position '[THESIS]' has been critiqued with: [CRITIQUES]
Strengthen the original position by:
1. Addressing these critiques directly
2. Identifying the core value/insight in the original position
3. Explaining conditions where this approach would be optimal
Make the strongest possible case without changing the fundamental position."

**Strengthened Position:**
- **Response to Critiques:** [How does the thesis address major criticisms?]
- **Core Value Preserved:** [What essential insight must be maintained?]
- **Optimal Conditions:** [When would this approach work best?]
- **Success Indicators:** [How would you know if this approach is working?]

**PHASE 4: DEVELOP SYNTHETIC RECONCILIATION**
**AI-Assisted Synthesis Prompt:**
"I'm working with two opposing positions:
Position A (Thesis): [THESIS]
Position B (Antithesis): [STRONGEST CRITIQUES]

Generate three potential reconciliations that:
1. Acknowledge valid concerns from both sides
2. Resolve the apparent contradiction
3. Offer a more comprehensive approach than either position alone
For each, identify what new distinction/perspective makes it possible."

**Synthesis Development:**
- **Integration Strategy:** [How do you combine the best of both positions?]
- **New Framework:** [What higher-order perspective emerges?]
- **Contradiction Resolution:** [How are oppositions transcended rather than compromised?]
- **Practical Implementation:** [How would this work in practice?]

**PHASE 5: VERIFY SYMBOLIC INTEGRITY**
**Consistency Check:**
- **Term Definitions:** [Do key terms maintain consistent meaning throughout?]
- **Logical Coherence:** [Does the synthesis avoid contradictions?]
- **Constraint Alignment:** [Does the solution respect all constraints?]
- **Value Preservation:** [Are essential values from all positions preserved?]

**PHASE 6: PROJECT ACROSS CONTEXTS**
**Context Testing:**
For each relevant context, evaluate:

**Context 1: [Specific Situation]**
- **How the solution performs:** [Strengths in this context]
- **Potential weaknesses:** [Where it might fail]
- **Required adaptations:** [How to address weaknesses]

**Context 2: [Different Situation]**
- **How the solution performs:** [Strengths in this context]  
- **Potential weaknesses:** [Where it might fail]
- **Required adaptations:** [How to address weaknesses]

**Context 3: [Edge Case Scenario]**
- **How the solution performs:** [Strengths in this context]
- **Potential weaknesses:** [Where it might fail]
- **Required adaptations:** [How to address weaknesses]

**PHASE 7: EVALUATE OR ITERATE**
**Termination Criteria Check:**
- **Positive Criteria:** [Does solution withstand critique across contexts?]
- **Pragmatic Criteria:** [Is further refinement cost-effective?]
- **Iteration Limit:** [Have you reached the predetermined limit for this decision type?]

**If Iterating:**
- **New Thesis:** [Use synthesis as starting point for next cycle]
- **Refined Focus:** [What specific aspects need more work?]
- **Learning Applied:** [What insights from this cycle inform the next?]

**FINAL DECISION DOCUMENTATION**
**Chosen Solution:** [Clear statement of final position]

**Implementation Plan:**
- **Phase 1:** [Immediate steps]
- **Phase 2:** [Medium-term actions]  
- **Phase 3:** [Long-term goals]
- **Contingencies:** [What if key assumptions prove wrong?]

**Success Criteria:**
- **Immediate (1-3 months):** [Early indicators]
- **Medium-term (3-12 months):** [Progress markers]
- **Long-term (1+ years):** [Ultimate outcomes]

**Review Schedule:**
- **Initial checkpoint:** [Date and criteria]
- **Full review:** [Date and criteria]
- **Course correction triggers:** [What would prompt reconsideration?]

**AI Collaboration Record:**
- **AI tools used:** [Which AI systems assisted]
- **AI contributions:** [Key insights from AI analysis]
- **Human decisions:** [Where human judgment was essential]
- **Integration approach:** [How AI and human input were combined]

**Reasoning Documentation:**
- **Key tensions navigated:** [What oppositions were resolved]
- **Assumptions validated/invalidated:** [What beliefs were tested]
- **Alternative paths considered:** [What other approaches were explored]
- **Future decision-makers:** [Context for those who inherit this decision]

### 13. Double Loop Learning (Argyris) Template

**DOUBLE LOOP LEARNING ANALYSIS PROMPT**

**Situation:** [Describe the problem/challenge you're analyzing]

**SINGLE LOOP ANALYSIS (Error Correction):**
**What Happened:**
- **Intended Result:** What were you trying to achieve?
- **Actual Result:** What actually happened?
- **Gap:** How big was the difference?
- **Error Correction:** How can you fix this specific problem?

**DOUBLE LOOP ANALYSIS (Questioning Assumptions):**

**Governing Variables (Underlying Assumptions):**
- **Assumption 1:** What did you assume about the situation?
  - Where did this assumption come from?
  - When is this assumption valid/invalid?
  - How does this assumption limit your actions?

- **Assumption 2:** What did you assume about other people?
  - What theory of human behavior were you using?
  - How might others see the situation differently?
  - What assumptions do others have about you?

- **Assumption 3:** What did you assume about causation?
  - What cause-effect relationships did you assume?
  - What other causal patterns might exist?
  - How might the system be creating the problem?

**Action Strategies Under Question:**
- **Current Strategy:** How do you typically approach this type of situation?
- **Strategy Origins:** Where did you learn this approach?
- **Strategy Limits:** In what contexts does this strategy fail?
- **Alternative Strategies:** What other approaches might work?

**Mental Models Examination:**
- **Your Mental Model:** How do you understand this domain?
- **Model Limitations:** What does your model obscure or ignore?
- **Alternative Models:** How might others frame this differently?
- **Model Evolution:** How has your understanding changed over time?

**DEFENSIVE ROUTINES IDENTIFICATION:**
**Personal Defenses:**
- What uncomfortable truths are you avoiding?
- How do you protect yourself from negative feedback?
- What questions do you not want to ask?
- How might you be contributing to the problem?

**Organizational Defenses:**
- What topics are "undiscussable" in your organization?
- How does the organization avoid uncomfortable truths?
- What structures prevent learning?
- How do power dynamics limit inquiry?

**TRIPLE LOOP EXPLORATION (Learning About Learning):**
- How do you know when you're learning?
- What prevents you from questioning your assumptions?
- How might you create better conditions for ongoing learning?
- What would help you notice your blind spots?

**NEW ACTION DESIGN:**
- **Revised Assumptions:** Based on this analysis, what new assumptions will guide you?
- **New Strategies:** What different approaches will you try?
- **Learning Experiments:** How will you test your new assumptions?
- **Feedback Systems:** How will you know if your new approach is working?

### 14. Critical Systems Heuristics (Ulrich) Template

**CRITICAL SYSTEMS HEURISTICS PROMPT**

**System Definition:** [What system are you examining?]

**BOUNDARY CRITIQUE QUESTIONS:**

**Sources of Motivation (WHY):**
1. **Beneficiaries:** Who ought to be the beneficiaries of the system?
   - Who is actually considered a beneficiary?
   - Who should be but isn't included?
   - Whose interests are being served?

2. **Purpose:** What ought to be the purpose of the system?
   - What is the system's actual purpose?
   - Who defines the purpose?
   - What other purposes might be valid?

3. **Measure of Success:** What ought to be the measure of success?
   - How is success actually measured?
   - Who determines these measures?
   - What alternative measures might be important?

**Sources of Control (WHO):**
4. **Decision Makers:** Who ought to be the decision makers?
   - Who actually makes the decisions?
   - Who is excluded from decision-making?
   - What gives decision makers their authority?

5. **Resources:** What resources ought to be controlled by the decision makers?
   - What resources do they actually control?
   - What resources are outside their control?
   - How does resource control affect the system?

6. **Conditions of Success:** What conditions of success ought to be under the control of decision makers?
   - What conditions are actually under their control?
   - What critical conditions are outside their control?
   - How does this affect system outcomes?

**Sources of Knowledge (WHAT):**
7. **Professional Expertise:** What expertise ought to be consulted?
   - What expertise is actually consulted?
   - What expertise is excluded or ignored?
   - How is expertise validated?

8. **Guarantors:** Who ought to belong to the guarantors of success?
   - Who actually guarantees the system will work?
   - What happens if the system fails?
   - Who bears the risks and costs?

9. **Secures Emancipation:** What secures the emancipation of the affected from the premises and promises of those involved?
   - How can affected parties influence the system?
   - What recourse do they have if harmed?
   - How can they exit or change the system?

**Sources of Legitimacy (HOW):**
10. **Worldview:** What worldview is determining?
    - What assumptions about reality underlie the system?
    - Whose worldview dominates?
    - What alternative worldviews exist?

11. **Moral Basis:** What secures the moral basis of the design?
    - What ethical framework guides the system?
    - Who determines what is moral/ethical?
    - What moral conflicts exist?

12. **Competence:** What secures the competence to implement the design?
    - Who is responsible for implementation?
    - What happens if implementation fails?
    - How is competence verified?

**BOUNDARY JUDGMENTS ANALYSIS:**
- **Inclusions:** What/who is included in the system boundary?
- **Exclusions:** What/who is excluded and why?
- **Boundary Effects:** How do boundary judgments affect outcomes?
- **Alternative Boundaries:** How might different boundaries change the system?

**EMANCIPATORY POTENTIAL:**
- **Power Imbalances:** Where do you see concentrations of power?
- **Marginalized Voices:** Who lacks voice in the current system?
- **Emancipatory Actions:** What would increase affected parties' influence?
- **System Transformation:** How might the system be redesigned for greater justice?

### 15. Cynefin Framework Template

**CYNEFIN FRAMEWORK ANALYSIS PROMPT**

**Situation Description:** [Describe the situation you're analyzing]

**DOMAIN ASSESSMENT:**
For your situation, evaluate which domain(s) apply:

**SIMPLE/OBVIOUS Domain Characteristics:**
- Are best practices clearly established?
- Is the relationship between cause and effect clear to everyone?
- Are there standard procedures that always work?
- Is expertise widely available?
- **Assessment:** Does this describe your situation? [Yes/No]

**COMPLICATED Domain Characteristics:**
- Are there good practices that experts know?
- Is the relationship between cause and effect clear but requires analysis?
- Do you need specialized expertise to understand it?
- Are there multiple right answers?
- **Assessment:** Does this describe your situation? [Yes/No]

**COMPLEX Domain Characteristics:**
- Do patterns emerge only in retrospect?
- Is the relationship between cause and effect only clear after the fact?
- Are there unknown unknowns?
- Do small changes sometimes have large effects?
- **Assessment:** Does this describe your situation? [Yes/No]

**CHAOTIC Domain Characteristics:**
- Is there no clear relationship between cause and effect?
- Is immediate action needed to establish order?
- Are search patterns ineffective?
- Is innovation required for survival?
- **Assessment:** Does this describe your situation? [Yes/No]

**DISORDER Domain Characteristics:**
- Is it unclear which of the other domains apply?
- Are people arguing about what type of situation this is?
- Are multiple approaches being tried simultaneously?
- **Assessment:** Does this describe your situation? [Yes/No]

**PRIMARY DOMAIN IDENTIFICATION:**
**Dominant Domain:** [Based on your assessment above]
**Mixed Domains:** [If elements of multiple domains exist]

**APPROACH DESIGN:**

**If SIMPLE/OBVIOUS:**
- **Sense:** What are the facts?
- **Categorize:** What category does this fit?
- **Respond:** What is the best practice response?
- **Monitor:** How will you ensure best practices are followed?

**If COMPLICATED:**
- **Sense:** What data do you need?
- **Analyze:** What expertise is required?
- **Respond:** What is the good practice approach?
- **Expert Consultation:** Who should be involved?

**If COMPLEX:**
- **Probe:** What safe-to-fail experiments can you run?
- **Sense:** What patterns are emerging?
- **Respond:** How can you amplify good patterns and dampen bad ones?
- **Emergent Practice:** How will you discover what works?

**If CHAOTIC:**
- **Act:** What immediate action will establish order?
- **Sense:** What is the impact of your action?
- **Respond:** How will you move toward a more stable domain?
- **Crisis Management:** What needs immediate attention?

**If DISORDER:**
- **Break Down:** How can you break this into smaller parts?
- **Gather Information:** What additional data would clarify the domain?
- **Expert Input:** Who can help assess the situation?
- **Multiple Approaches:** What parallel strategies might work?

**TRANSITION PLANNING:**
- **Current State:** Where are you now?
- **Desired State:** Where do you want to be?
- **Movement Strategy:** How will you transition between domains?
- **Warning Signs:** What indicates you're moving into a different domain?

**DYNAMIC CONSIDERATIONS:**
- **Complacency Risk:** How might success in simple domains create vulnerability?
- **Complexity Collapse:** What could cause a complicated situation to become chaotic?
- **Innovation Opportunity:** How might chaos create opportunities for breakthrough?
- **Learning Strategy:** How will you build capability for each domain?

### 16. Design Dialectics/Onto-Epistemic Mapping Template

**DESIGN DIALECTICS / ONTO-EPISTEMIC MAPPING PROMPT**

**Design Challenge:** [What system/artifact/process are you designing?]

**ONTOLOGICAL MAPPING (What exists?):**

**Being-Structure Analysis:**
- **Primary Entities:** What fundamental entities does your design assume exist?
- **Relationships:** How do these entities relate to each other?
- **Emergence:** What new entities emerge from these relationships?
- **Persistence:** What maintains identity over time?
- **Change:** What enables transformation?

**Temporal Ontology:**
- **Time Conception:** How does your design understand time? (linear, cyclical, multi-dimensional)
- **Duration:** What time scales are relevant?
- **Synchronicity:** What needs to happen simultaneously?
- **Historical Dependency:** How does past shape present possibilities?
- **Future Orientation:** How does anticipated future affect current design?

**Spatial Ontology:**
- **Space Conception:** How does your design understand space? (container, network, field)
- **Scale:** What spatial scales matter?
- **Boundaries:** What defines inside/outside?
- **Topology:** How are connections structured?
- **Place vs. Space:** How does location matter?

**EPISTEMIC MAPPING (How is knowledge constructed?):**

**Knowledge Sources:**
- **Empirical:** What can be observed/measured?
- **Rational:** What can be logically derived?
- **Intuitive:** What is known through direct insight?
- **Social:** What is known through interaction?
- **Embodied:** What is known through physical engagement?

**Validation Methods:**
- **Verification:** How do you check if something is true?
- **Falsification:** How do you test if something is false?
- **Consensus:** How do you build agreement?
- **Pragmatic:** How do you test if something works?
- **Aesthetic:** How do you recognize elegance/beauty?

**Knowledge Dynamics:**
- **Learning:** How does understanding develop?
- **Forgetting:** What gets lost and why?
- **Transfer:** How is knowledge shared?
- **Evolution:** How does knowledge change?
- **Limits:** What cannot be known?

**DIALECTICAL TENSIONS:**

**Onto-Epistemic Contradictions:**
- Where do your assumptions about reality conflict with how you gain knowledge?
- What can you know vs. what actually exists?
- How do observer and observed interact?
- What changes when you try to understand it?

**Design Paradoxes:**
- **Control vs. Emergence:** How much can/should be designed vs. allowed to emerge?
- **Stability vs. Change:** How do you design for persistence and transformation?
- **Individual vs. Collective:** How do you balance personal and social needs?
- **Local vs. Global:** How do you optimize across scales?
- **Efficiency vs. Resilience:** How do you balance optimization and adaptability?

**SYNTHETIC DESIGN PRINCIPLES:**

**Dialectical Resolution Strategies:**
- **Both/And:** How can you embrace contradictory requirements?
- **Dynamic Balance:** How can you oscillate between poles appropriately?
- **Meta-Level Integration:** How can you transcend the contradiction at a higher level?
- **Contextual Switching:** How can you adapt approach based on situation?
- **Recursive Application:** How can the system redesign itself?

**Implementation Framework:**
- **Structural Elements:** What unchanging features enable change?
- **Process Elements:** What ongoing activities maintain the system?
- **Interface Elements:** How does the system relate to its environment?
- **Meta-Elements:** How does the system monitor and modify itself?

**REFLEXIVE DESIGN:**
- **Self-Reference:** How does the design process reflect the design principles?
- **Observer Impact:** How does the designer change the designed?
- **Design Evolution:** How will the design change the designer?
- **Recursive Improvement:** How will the system improve its own design process?

**VALIDATION AND ITERATION:**
- **Coherence Check:** Do ontological and epistemological assumptions align?
- **Pragmatic Test:** Does the design work in practice?
- **Dialectical Test:** Does it successfully navigate contradictions?
- **Emergent Properties:** What unexpected qualities appear?
- **Next Iteration:** What contradictions does this design create?

---

## Academic Foundation

The **Meta-Dialectical Methodology** featured in this collection is derived from:

**Haryanto, C. Y., & Lomempow, E. (2025).** *Cognitive Silicon: An Architectural Blueprint for Post-Industrial Computing Systems*. arXiv preprint arXiv:2504.16622. [https://doi.org/10.48550/arXiv.2504.16622](https://doi.org/10.48550/arXiv.2504.16622)

The paper presents a dialectical co-design methodology that creates "structured friction to expose blind spots and trade-offs" in complex system design. This collection generalizes their approach across various problem-solving domains while maintaining the core principle of using tensions as productive forces rather than obstacles to overcome.

---

## AI Integration Strategies for Problem-Solving

### Strategic AI Integration Framework

**Human-AI Collaboration Principles:**
- **Human direction**: You define important tensions and values; AI explores implications
- **Cross-verification**: Use multiple AI systems or prompting approaches for critical insights  
- **Calibrated trust**: Place more weight on AI analyses of logical consistency than value judgments
- **Epistemic humility**: Recognize both human and AI limitations in uncertain domains
- **Final synthesis ownership**: While AI can generate options, humans should own the final synthesis
- **Documentation discipline**: Record both AI and human contributions to the reasoning process

### AI Integration Points by Methodology Type

| Process Stage | How AI Can Help | Human Role | Best Prompting Patterns |
|---------------|-----------------|------------|-------------------------|
| **Problem Definition** | Generate alternative framings, identify assumptions | Select relevant framings, define scope | "Reframe this problem from 3 different perspectives..." |
| **Data Gathering** | Surface relevant information, identify patterns | Validate sources, interpret significance | "What information would be most relevant for..." |
| **Analysis** | Systematically identify weaknesses, surface counter-examples | Guide critique toward meaningful areas | "Act as a thoughtful critic of..." |
| **Synthesis** | Generate reconciliations, identify patterns | Select valuable insights, maintain coherence | "Generate 3 potential reconciliations that..." |
| **Validation** | Simulate different contexts, identify edge cases | Define relevant contexts, interpret results | "Test this solution across these scenarios..." |

### Effective AI Prompting Patterns

**For Devil's Advocacy:**
```
Act as a thoughtful critic of the following position: [POSITION]
Identify:
1. Three implicit assumptions that might not hold
2. Two edge cases where this approach could fail
3. One fundamental tension this position doesn't resolve
Explain each critique clearly, focusing on the strongest objections.
```

**For Steelmanning:**
```
The following position has been critiqued: [POSITION]
Key critiques include: [CRITIQUES]
Your task is to strengthen the original position by:
1. Addressing these critiques directly
2. Identifying the core value or insight in the original position
3. Explaining under what conditions this approach would be optimal
Make the strongest possible case without changing the fundamental position.
```

**For Multi-Perspective Analysis:**
```
Analyze this situation from these stakeholder perspectives: [LIST]
For each perspective, identify:
1. Primary concerns and priorities
2. Likely support or opposition to the current approach  
3. What would make this decision better from their viewpoint
4. Potential unintended consequences they might experience
```

**For Pattern Recognition:**
```
Given this data/situation: [DATA]
Identify:
1. Three patterns that might not be immediately obvious
2. Potential relationships between seemingly unrelated factors
3. Historical parallels that might offer insights
4. Early warning signs for potential problems
```

**For Scenario Planning:**
```
For this decision: [DECISION]
Generate 3 scenarios:
1. Best case: What would success look like?
2. Worst case: What could go badly wrong?
3. Most likely: What will probably happen?
For each scenario, explain the key factors that would drive that outcome.
```

### AI-Enhanced Templates for Key Methodologies

**Enhanced Root Cause Analysis with AI:**
```
**AI-ENHANCED ROOT CAUSE ANALYSIS**

**Initial Problem Definition:** [Your problem statement]

**AI Pattern Recognition Prompt:**
"Analyze this problem: [PROBLEM]
1. What patterns in the data suggest potential root causes?
2. What similar problems have occurred in other domains?
3. What system dynamics might be creating this symptom?
4. What are 3 non-obvious potential causes?"

**Human Analysis:**
- Which AI suggestions align with your observations?
- What domain-specific factors might AI have missed?
- What stakeholder perspectives should be included?

**AI Devil's Advocate for Each Suspected Cause:**
"Challenge this suspected root cause: [CAUSE]
1. What evidence contradicts this explanation?
2. What alternative causes could produce the same symptoms?
3. What would we expect to see if this were NOT the root cause?"

**Synthesis and Validation:**
- Combine AI analysis with human insight
- Test hypotheses against available evidence
- Design experiments to validate root causes
```

---

## Usage Guidelines

### Template Selection Decision Tree

```
START: What type of problem are you solving?

├─ QUICK TACTICAL FIXES
│  ├─ Simple cause-effect relationships → 5 Whys
│  ├─ Need to prioritize multiple issues → Pareto Analysis  
│  ├─ Systematic improvement process → PDCA
│  └─ Multiple potential causes → Fishbone Diagram

├─ SYSTEM IMPROVEMENTS  
│  ├─ Technical/engineering problems → TRIZ
│  ├─ Process bottlenecks → Theory of Constraints
│  ├─ Risk assessment needed → FMEA
│  ├─ Complex causation → Root Cause Analysis
│  └─ System interactions → Systems Mapping

├─ STRATEGIC DECISIONS
│  ├─ Multiple options to evaluate → Kepner-Tregoe
│  ├─ Uncertain problem type → Cynefin Framework
│  ├─ Value conflicts present → Dialectical Method
│  └─ High complexity + ambiguity → Meta-Dialectical

└─ LEARNING & DEVELOPMENT
   ├─ Questioning assumptions → Double Loop Learning
   ├─ Social/political issues → Critical Systems Heuristics  
   └─ Design challenges → Design Dialectics
```

### Documentation Framework for All Methodologies

**Decision Journal Template (Adaptable to any methodology):**
```markdown
# Decision: [Title]
Date: [Date]
Decision Owner: [Name]
Methodology Used: [Which template/approach]
Importance Level: [Routine/Significant/Strategic/Existential]

## Context & Problem Definition
- **Situation:** [What prompted this analysis?]
- **Stakeholders:** [Who is affected?]
- **Constraints:** [Non-negotiable boundaries]
- **Success Criteria:** [How will you measure success?]

## Analysis Process
### Method Applied: [Specific methodology]
### Key Insights:
- **Discovery 1:** [What did you learn?]
- **Discovery 2:** [What surprised you?]
- **Discovery 3:** [What assumptions were challenged?]

### AI Assistance Used:
- **Tools:** [Which AI systems were used?]
- **Prompts:** [Key prompts that generated valuable insights]
- **AI Contributions:** [What did AI help you discover?]
- **Human Decisions:** [Where human judgment was essential?]

## Alternative Approaches Considered
- **Option 1:** [Brief description and why rejected/accepted]
- **Option 2:** [Brief description and why rejected/accepted]
- **Option 3:** [Brief description and why rejected/accepted]

## Final Decision
**Chosen Approach:** [Clear statement of decision]

**Rationale:** [Why this approach over alternatives?]

**Implementation Plan:**
- **Immediate (1-4 weeks):** [First steps]
- **Short-term (1-3 months):** [Early milestones]  
- **Medium-term (3-12 months):** [Progress markers]

**Risk Mitigation:**
- **Risk 1:** [Potential problem] → [Mitigation strategy]
- **Risk 2:** [Potential problem] → [Mitigation strategy]

**Review Schedule:**
- **Initial checkpoint:** [Date] - [What to evaluate]
- **Full review:** [Date] - [What to evaluate]
- **Success evaluation:** [Date] - [Final assessment criteria]

## Learning & Future Application
- **What worked well in this process?**
- **What would you do differently next time?**
- **How might this decision inform future similar situations?**
- **What new questions emerged from this analysis?**
```

### Termination Criteria for All Methodologies

**When to Stop the Analysis Process:**

**Positive Termination (Good to proceed):**
- Solution addresses the core problem effectively
- Key stakeholder concerns have been considered
- Implementation plan is clear and feasible
- Success criteria are defined and measurable
- Risks have been identified and mitigated

**Pragmatic Termination (Good enough):**
- Decision deadline has arrived
- Further analysis cost exceeds expected benefit
- Multiple iterations yield only minor improvements
- Sufficient confidence level reached for decision importance

**Negative Termination (Need to reframe):**
- Core constraints cannot be satisfied by any option
- Fundamental assumptions about the problem are incorrect
- Required resources are unavailable
- Stakeholder conflicts cannot be reasonably resolved

**Iteration Guidelines by Decision Importance:**
- **Routine:** 1-2 iterations, 1-4 hours total
- **Significant:** 2-3 iterations, 4-16 hours total  
- **Strategic:** 3-5 iterations, 1-5 days total
- **Existential:** 5+ iterations, 1+ weeks total

### Meta-Dialectical Implementation Example

**Scenario:** A product manager deciding whether to pursue a major product redesign.

**Phase 1 - Initial Thesis:**
"We should completely redesign our product interface to align with modern design principles and improve user experience."

**Phase 2 - AI-Assisted Devil's Advocacy:**
*Prompt:* "Act as a thoughtful critic of this position: 'We should completely redesign our product interface to align with modern design principles and improve user experience.' Identify: 1) Three implicit assumptions that might not hold, 2) Two edge cases where this approach could fail, 3) One fundamental tension this position doesn't resolve."

*AI Response highlights:*
- Assumption: Current users want new interface rather than mastery of existing one
- Edge case: Long-time power users might reject dramatic workflow changes  
- Tension: Balancing fresh design with familiar aspects that define product identity

**Phase 3 - Steelmanning:**
*Prompt:* "Help me strengthen my original position by addressing these criticisms. What's the strongest case for a redesign that accounts for user disruption and transition costs?"

*Strengthened position:* "A redesign addresses technical debt, improves accessibility compliance, and positions us competitively, while a phased approach with user cohort testing can minimize disruption."

**Phase 4 - AI-Assisted Synthesis:**
*Prompt:* "Generate three potential reconciliations between: A) Completely redesigning the product, B) The concerns about user disruption and transition costs."

*Selected synthesis:* "Implement a dual-interface strategy with opt-in beta program, allowing gradual transition while maintaining familiar workflows for power users who prefer them."

**Phase 5-7 - Verification and Implementation:**
Final decision includes phased rollout plan, success metrics for both interfaces, and clear criteria for eventually deprecating the legacy interface based on user adoption rates.

---

## Advanced Collaborative Techniques

### Multi-Human-AI Team Structures

**Role-Based Collaboration:**
- **Thesis Advocate:** Presents and defends the primary position (Human)
- **Devil's Advocate:** Systematically challenges assumptions (Human + AI)
- **Steelman:** Strengthens positions before critique (AI + Human validation)
- **Synthesizer:** Identifies reconciliations (Human + AI generation)
- **Context Tester:** Evaluates across different scenarios (AI + Human judgment)
- **Process Guardian:** Maintains analytical integrity (Human)
- **Documentation Lead:** Captures insights and evolution (Human + AI assistance)

**AI-Human Handoff Patterns:**
1. **Human frames → AI explores → Human decides**
2. **AI generates options → Human evaluates → AI tests selected option**
3. **Human-AI alternating devil's advocacy → Joint synthesis**
4. **Parallel AI analysis → Human integration → Collective validation**

### Cross-Methodology Integration

**Sequential Application:**
- Start with Cynefin to classify problem type
- Apply appropriate methodology based on classification
- Use Meta-Dialectical for final validation of complex decisions

**Parallel Application:**
- Apply multiple methodologies simultaneously
- Compare insights across approaches
- Synthesize findings into robust solution

**Nested Application:**
- Break complex problems into sub-problems
- Apply different methodologies to each sub-problem
- Use higher-order methodology to integrate solutions

### Quality Checks for Problem-Solving Analysis

**Before concluding any analysis, verify:**

**Completeness:**
- [ ] All relevant stakeholders considered
- [ ] Key assumptions explicitly identified  
- [ ] Alternative approaches explored
- [ ] Implementation feasibility assessed
- [ ] Success criteria defined

**Rigor:**
- [ ] Evidence supports conclusions
- [ ] Counterarguments addressed
- [ ] Edge cases considered
- [ ] Assumptions tested where possible
- [ ] Expert input sought when needed

**Clarity:**
- [ ] Decision rationale is clear
- [ ] Implementation steps are specific
- [ ] Success measures are quantifiable
- [ ] Communication plan exists
- [ ] Documentation is complete

**Future-Proofing:**
- [ ] Review dates scheduled
- [ ] Course-correction triggers identified
- [ ] Learning capture process planned
- [ ] Decision context documented for future reference

---

## Conclusion: From Templates to Practice

These comprehensive prompting templates represent a toolkit for systematic thinking across the spectrum of problem complexity. The key to effective application lies not in rigid adherence to any single methodology, but in developing the judgment to:

**Select Appropriately:** Choose methodologies that match problem complexity and available resources.

**Adapt Flexibly:** Modify templates based on specific context and constraints.

**Integrate Strategically:** Combine human insight with AI capabilities to enhance analysis quality.

**Document Systematically:** Capture reasoning and process for future learning and accountability.

**Iterate Intelligently:** Know when to continue refining and when to move to action.

The ultimate goal is developing a **meta-cognitive capacity** - the ability to think about thinking - that naturally selects and applies appropriate analytical frameworks based on the situation at hand.

### From Method to Mindset

With practice, these structured approaches become internalized patterns of thought that:
- Naturally seek multiple perspectives
- Systematically challenge assumptions  
- Navigate rather than eliminate tensions
- Integrate analysis with action
- Learn from both successes and failures

The most valuable outcome is not just better individual decisions, but the development of organizational and personal capacity for nuanced thinking in complex environments.

**Start Simple:** Begin with surface-level methods for routine decisions.
**Build Gradually:** Add complexity as you develop comfort with structured analysis.
**Integrate AI Thoughtfully:** Use AI to enhance human judgment, not replace it.
**Document Learning:** Track what works and what doesn't for continuous improvement.
**Share Knowledge:** Help others develop these capabilities through teaching and collaboration.

*Remember: The goal is not perfect analysis but better decisions. Sometimes a simple 5 Whys is exactly what's needed. Sometimes the situation demands meta-dialectical rigor. Wisdom lies in knowing the difference.*