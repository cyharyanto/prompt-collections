# Multimodal Prompt Engineering Framework

## System Capabilities & Constraints
- **Processing scope**: Images, audio, video, structured data, and combinations
- **Core functions**: Object recognition, text extraction, relationship analysis, context integration
- **Performance factors**: Resolution, quality, context window allocation, modality balance
- **Limitations**: Cross-modal abstraction gaps, visual-linguistic alignment, context attribution

## Technique Matrix

| Technique | Application | Implementation |
|-----------|-------------|----------------|
| Cross-modal reasoning | Relationship analysis | `Analyze relationship between [object] in image and [context] in text` |
| Visual grounding | Object identification | `Locate and describe [entity] with specific attributes` |
| Sequential processing | Complex analysis | `First describe image → then analyze specific components → finally integrate with text` |
| Parallel input | Comparative analysis | `Compare visual elements with numerical data` |

## Implementation Library

### Visual-Textual Integration Patterns
```
# Pattern: Technical Diagram Analysis

1. Component Identification
   - "Identify all labeled components in this technical diagram"
   - "Locate and list all connection points between components A and B"
   - "Describe the hierarchical relationship between elements [x, y, z]"

2. Specification Integration
   - "Compare the measurements in the diagram with the specifications in the text"
   - "Verify whether component dimensions match the requirements in section 3.2"
   - "Identify any discrepancies between the visual representation and written specifications"

3. Procedural Interpretation
   - "Describe the process flow illustrated in this diagram based on the numbered steps"
   - "Explain how the visual cycle relates to the maintenance schedule in the documentation"
   - "Translate this visual troubleshooting guide into step-by-step textual instructions"

Implementation example:
"Analyze this circuit diagram and associated specifications table:
1. First identify all electronic components and their values
2. Then explain the signal flow from input to output 
3. Finally, verify that the component values match the specifications table
4. Note any potential issues or optimization opportunities based on both sources"
```

### Image-Based Reasoning Patterns
```
# Pattern: Visual Evidence Assessment

1. Observation Isolation
   - "Describe only what is directly visible in the image without inference"
   - "Identify specific visual elements that relate to [topic/question]"
   - "List the observable measurements/indicators shown in this visualization"

2. Evidence Linking
   - "Connect the visual elements to the claims made in the text"
   - "Identify which aspects of the image support or contradict hypothesis X"
   - "Match the data points in this graph with the conclusions in the report"

3. Confidence Calibration
   - "Rate your confidence in each observation on a scale of 1-5 and explain why"
   - "Distinguish between directly observable elements and inferred characteristics"
   - "Identify areas where the image quality or angle limits definitive conclusions"

Implementation example:
"Evaluate this product defect image against quality standards:
1. First, list all visible characteristics of the product surface
2. Compare these observations with the acceptable tolerances in the specification document
3. For each potential defect, rate your confidence level (1-5) and explain the basis for your assessment
4. Recommend whether this item passes quality control based on visual evidence"
```

### Multi-Image Comparative Analysis
```
# Pattern: Before/After Assessment

1. Individual Analysis
   - "Describe the key characteristics of image A, then separately describe image B"
   - "Identify the primary elements in each image independently"
   - "Catalog the measurable attributes present in each image"

2. Systematic Comparison
   - "Compare images A and B regarding aspects [x, y, z]"
   - "Identify all differences between the before and after images"
   - "Quantify the changes in [specific elements] between images"

3. Change Interpretation
   - "Explain the transformation process that likely occurred between states"
   - "Assess the effectiveness of the intervention based on the visual changes"
   - "Predict next steps based on the progression shown in these images"

Implementation example:
"Analyze these before/after building renovation images:
1. For each image, document architectural elements, condition indicators, and visible materials
2. Create a detailed comparison table identifying all changes in structure, materials, and aesthetic elements
3. Assess the quality and completeness of the renovation based on industry standards
4. Recommend any additional work that appears necessary based on the visual evidence"
```

### Text-in-Image Extraction & Analysis
```
# Pattern: Document Intelligence

1. Structured Extraction
   - "Extract all text from this document image in a structured format"
   - "Identify and transcribe all tabular data preserving row/column relationships"
   - "Locate and extract text specifically from sections [A, B, C]"

2. Format-Aware Processing
   - "Extract information preserving the document's hierarchical structure"
   - "Distinguish between headings, body text, annotations, and captions"
   - "Identify form fields and their corresponding values"

3. Content Integration
   - "Summarize the key information from both textual and visual elements"
   - "Extract numerical data and explain how it relates to the charts/graphs"
   - "Create a structured representation that preserves both content and layout context"

Implementation example:
"Process this invoice document:
1. Extract all text content preserving structural relationships
2. Create a structured JSON with fields for: invoice number, date, vendor, line items, subtotal, taxes, and total amount
3. Verify mathematical consistency between line items and totals
4. Flag any irregularities or missing information that would prevent processing"
```

## Application Domains

### Document Analysis Framework
```
# Document Analysis Implementation

1. Structure Recognition Layer
   - Document type classification: "Identify if this is an invoice, contract, form, or report"
   - Section delineation: "Identify the main sections and their hierarchical relationships"
   - Layout mapping: "Create a structural map showing text blocks, images, tables, and their spatial relationships"

2. Content Extraction Layer
   - Text transcription: "Extract all textual content with positional awareness"
   - Data identification: "Locate and extract key-value pairs, tables, and structured data"
   - Entity recognition: "Identify organizations, people, dates, amounts, and domain-specific entities"

3. Semantic Integration Layer
   - Cross-reference resolution: "Link related information across different sections"
   - Logical flow analysis: "Trace the document's logical progression and argumentative structure"
   - Contextual interpretation: "Integrate visual and textual elements to derive comprehensive meaning"

Implementation example:
"Analyze this research paper:
1. Map the document structure (abstract, introduction, methodology, results, discussion, references)
2. Extract key research questions, methodologies, findings, and conclusions
3. Identify all figures/tables and explain how they support the textual claims
4. Create a comprehensive summary integrating both textual arguments and visual evidence"
```

### Visual Question-Answering Framework
```
# Visual QA Implementation

1. Question Analysis Layer
   - Intent classification: "Determine if question seeks identification, description, relationship, or reasoning"
   - Focus identification: "Locate the specific visual elements relevant to the question"
   - Context integration: "Incorporate any textual context that frames the visual question"

2. Visual Evidence Layer
   - Targeted observation: "Examine visual elements directly related to the question"
   - Property extraction: "Identify relevant attributes (color, size, position, text, state)"
   - Relationship mapping: "Analyze spatial, functional, or conceptual relationships between elements"

3. Response Formulation Layer
   - Evidence compilation: "Gather all relevant visual and contextual evidence"
   - Reasoning application: "Apply appropriate reasoning patterns (comparative, causal, categorical)"
   - Confidence calibration: "Match certainty level to evidence quality and question specificity"

Implementation examples:

Basic identification: 
"What brand logo appears on this product packaging?"

Relationship analysis:
"How does the temperature trend in this graph relate to the events described in the caption?"

Reasoning with uncertainty:
"Based on the visible symptoms in this plant image and the growing conditions described, what is the most likely cause of the discoloration?"

Counterfactual assessment:
"If the component arrangement in this device were modified as described in the proposal, what potential issues might arise based on the current configuration?"
```

### Multimodal Data Analysis
```
# Multimodal Data Analysis Implementation

1. Cross-Format Integration Layer
   - Data alignment: "Match data points across visual and tabular representations"
   - Format translation: "Describe how the same information appears across different modalities"
   - Representation comparison: "Assess the effectiveness of different data visualization choices"

2. Pattern Extraction Layer
   - Trend identification: "Describe patterns visible in the graphical data"
   - Anomaly detection: "Identify outliers or unexpected patterns in the visualizations"
   - Correlation discovery: "Determine relationships between variables across different representations"

3. Insight Generation Layer
   - Finding prioritization: "Highlight the most significant patterns based on business context"
   - Cause-effect analysis: "Explain potential reasons for observed patterns or anomalies"
   - Recommendation development: "Suggest actions based on integrated data analysis"

Implementation example:
"Analyze this sales dashboard with multiple visualizations and supporting data tables:
1. Describe the key trends visible in each chart (regional sales, product performance, quarterly growth)
2. Identify any inconsistencies or surprising patterns across different visualizations
3. Explain how the tabular data supports or provides additional context to the visual representations
4. Recommend 3 specific actions based on the integrated analysis of all data sources"
```

### Visual Content Creation Guidance
```
# Visual Content Creation Implementation

1. Specification Interpretation Layer
   - Requirement analysis: "Extract key visual requirements from the design brief"
   - Style interpretation: "Identify specific style attributes requested (modern, corporate, minimalist)"
   - Constraint mapping: "List all technical and brand constraints that must be followed"

2. Element Recommendation Layer
   - Component suggestion: "Recommend layout elements based on communication goals"
   - Visual hierarchy guidance: "Suggest focal points and information prioritization"
   - Format optimization: "Advise on aspect ratios, sizes, and formats for intended use"

3. Feedback Implementation Layer
   - Comparative analysis: "Assess how well the visual meets specified requirements"
   - Improvement guidance: "Suggest specific modifications to better achieve stated goals"
   - Iteration framework: "Provide structured approach for progressive refinement"

Implementation example:
"Provide guidance for this draft infographic about climate change:
1. Analyze how effectively the current design communicates the key data points
2. Assess the visual hierarchy and suggest improvements for information flow
3. Recommend specific changes to color, typography, and layout to enhance clarity
4. Suggest additional visualization types that might better represent the time-series data"
```

## Technical Implementation

### Modality Balancing Framework
| Focus Ratio | Implementation Pattern | Application Context | Optimization Approach |
|-------------|------------------------|---------------------|------------------------|
| **Image-dominant (70:30)** | Image analysis with textual context | Object identification, visual assessment, environment analysis | Detailed visual description + targeted textual integration + specific question focus |
| **Balanced (50:50)** | Cross-modal relationship analysis | Document analysis, data visualization, instructional content | Parallel processing + explicit connection mapping + equivalent attention allocation |
| **Text-dominant (30:70)** | Text analysis with visual reference | Content creation, textual reasoning with visual evidence, report generation | Primary textual focus + visual evidence citation + selective image referencing |

### Resolution-Prompt Scaling Guidelines
| Image Complexity | Prompt Length | Detail Focus | Token Allocation |
|------------------|--------------|--------------|------------------|
| **Simple** (1-3 main elements) | Concise (2-3 sentences) | Holistic relationships | 70% analysis instruction, 30% output formatting |
| **Moderate** (4-10 elements) | Detailed (4-7 sentences) | Key component interactions | 50% component identification, 50% relationship analysis |
| **Complex** (10+ elements) | Comprehensive (8+ sentences) | Hierarchical examination | 40% structure mapping, 30% critical element focus, 30% integration |

### Cross-Modal Reference Techniques
```
# Reference Precision Framework

1. Spatial Referencing
   - Quadrant system: "In the upper-right quadrant of the image..."
   - Grid coordinates: "In cell B3 of the visual grid..."
   - Relative positioning: "To the left of the main subject..."

2. Element Identification
   - Unique attribute reference: "The red circular component with label A4..."
   - Type-instance pattern: "The largest of the three rectangular buttons..."
   - Contextual disambiguation: "The temperature gauge that connects to the pressure valve..."

3. Visual-Textual Bridging
   - Explicit connection: "Connect data point X in the graph with explanation Y in the text"
   - Bidirectional validation: "Verify whether the numerical values in the table match the heights in the bar chart"
   - Cross-modal annotation: "Create textual labels for unlabeled components based on the written description"

Implementation example:
"Analyze the relationship between components in this system diagram:
1. Refer to each component by its labeled ID (A1, B2, etc.)
2. When describing connections, specify both the connection type and direction (e.g., 'data flows from A1 to B3 via the blue connector')
3. For unlabeled elements, create consistent reference names based on position and function
4. When referencing measurements, specify both the visual indicator and the corresponding value in the specifications table"
```

### Multimodal Chain-of-Thought Techniques
```
# Sequential Reasoning Pattern

1. Observation Phase
   - Visual inventory: "I'll first catalog all visible elements in the image..."
   - Text extraction: "The image contains the following text elements..."
   - Structure mapping: "The document has a two-column layout with the following sections..."

2. Analysis Phase
   - Component relationships: "Based on the positioning, components A and B appear to be connected by..."
   - Cross-reference validation: "The values mentioned in paragraph 2 correspond to the measurements shown in figure 3..."
   - Pattern identification: "The repeating elements in the visual display suggest a cyclical process..."

3. Reasoning Phase
   - Evidence compilation: "Combining the textual description and visual elements, I can determine that..."
   - Inference justification: "The conclusion about functionality is supported by both the diagram layout and the technical specifications..."
   - Confidence assessment: "I can state with high confidence that... however, I'm less certain about... due to limited visual information"

Implementation example:
"Analyze this technical drawing and accompanying specifications:

Step 1: I'll first identify all labeled components in the drawing (A1-power supply, B2-controller, C3-sensor array...).

Step 2: Now I'll examine how these components are connected (A1 connects to B2 via a power line, B2 connects to C3 via a data bus...).

Step 3: Comparing the component specifications in the text with the visual representation, I notice the sensor array (C3) is rated for 24V operation, but the power supply (A1) output is specified as 12V in the documentation.

Step 4: Based on this analysis, there appears to be a discrepancy between the power requirements and supply that would prevent proper operation."
```

## Bias Mitigation & Fairness Frameworks

### Representational Balance Assessment
```
# Visual Fairness Evaluation Framework

1. Demographic Representation
   - Presence analysis: "Identify the diversity of people represented in these images"
   - Role examination: "Analyze the positions, activities, and prominence of different groups"
   - Stereotype assessment: "Evaluate whether portrayals reinforce or challenge common stereotypes"

2. Cultural Context Awareness
   - Symbol recognition: "Identify culturally specific elements and their significance"
   - Interpretation variation: "Consider how different cultural perspectives might interpret these visuals"
   - Contextual sensitivity: "Note whether the visual requires cultural background for proper understanding"

3. Technical Fairness Factors
   - Quality consistency: "Assess whether all subjects are represented with similar image quality"
   - Processing equity: "Evaluate whether the model analyzes all subjects with similar accuracy"
   - Description balance: "Ensure descriptions maintain consistent detail and tone across subjects"

Implementation example:
"Analyze this marketing campaign imagery for representational fairness:
1. Document the diversity of people shown across dimensions of age, gender, ethnicity, and ability
2. Examine role distribution, positioning, and prominence across different groups
3. Assess whether certain groups are depicted with different quality, lighting, or compositional emphasis
4. Recommend specific adjustments to improve representational balance while maintaining campaign objectives"
```

### Confidence Calibration Framework
```
# Uncertainty Communication Framework

1. Visual Certainty Assessment
   - Quality-based confidence: "The image resolution limits confidence in identifying small details"
   - Occlusion awareness: "Partial visibility of the component reduces certainty about its complete state"
   - Perspective limitations: "The viewing angle prevents conclusive assessment of the rear connections"

2. Textual-Visual Alignment
   - Corroboration strength: "The text strongly confirms what is visible in the image"
   - Contradiction handling: "There's an apparent discrepancy between the visual evidence and textual description"
   - Complementary information: "The text provides context not inferrable from the image alone"

3. Explicit Uncertainty Markup
   - Confidence labeling: "High confidence: clearly visible text; Medium confidence: partially obscured elements; Low confidence: implied connections"
   - Alternative possibilities: "The component could be either version A or B based on visible characteristics"
   - Information gaps: "The connection between components X and Y is not visible in the provided images"

Implementation example:
"Analyze this medical imaging series with corresponding patient data:

High confidence observations:
- Clearly visible mass in the upper right quadrant (marked with arrow in image 2)
- Dimensions approximately 2.3cm x 1.8cm based on scale reference

Medium confidence assessments:
- Tissue type appears consistent with diagnosis in medical record, though image contrast limits certainty
- Boundary definition suggests [specific characteristic] but higher resolution would confirm

Low confidence/cannot determine:
- Unable to assess potential involvement of deeper structures due to this imaging modality
- Cannot verify the timeline progression claimed in the notes based solely on these images"
```

## Advanced Techniques

### Multimodal RAG Implementation
```
# Retrieval-Augmented Multimodal Analysis

1. Query Formulation Layer
   - Visual question decomposition: "Break complex visual query into analyzable components"
   - Cross-modal retrieval framing: "Formulate search queries that bridge visual and textual domains"
   - Specification precision: "Define exact visual elements requiring knowledge augmentation"

2. Knowledge Integration Layer
   - Visual-textual alignment: "Map retrieved information to specific regions or elements in the image"
   - Confidence differentiation: "Distinguish between directly observed vs. knowledge-enhanced conclusions"
   - Source attribution: "Maintain clear boundaries between visual evidence and supplementary knowledge"

3. Enhanced Response Layer
   - Contextualized analysis: "Enrich visual observations with domain-specific knowledge"
   - Educational scaffolding: "Provide explanatory framework for interpreting visual information"
   - Verification support: "Offer additional verification methods or references for critical assessments"

Implementation example:
"Analyze this historical architectural photograph with knowledge augmentation:

1. First describe only what is directly observable in the image (architectural style, visible features, apparent time period)

2. Based on these observations, retrieve relevant information about:
   - The specific architectural style and its defining characteristics
   - Typical construction methods and materials of this period
   - Historical context that might explain design choices

3. Integrate this knowledge by:
   - Identifying specific architectural elements with their technical names
   - Explaining likely construction techniques used for visible features
   - Providing historical context that enhances understanding
   - Clearly distinguishing direct observations from knowledge-based inferences"
```

### Multimodal Cognitive Task Analysis
```
# Complex Visual Problem-Solving Framework

1. Task Decomposition Layer
   - Visual subtask identification: "Break down the visual analysis into discrete cognitive operations"
   - Sequential processing map: "Define the optimal order for analyzing multimodal information"
   - Attention focusing guide: "Direct attention to critical visual elements in specific sequence"

2. Reasoning Structure Layer
   - Evidence collection framework: "Gather relevant data points from both visual and textual sources"
   - Inference construction: "Build logically connected analyses based on multimodal evidence"
   - Alternative evaluation: "Consider multiple interpretations of ambiguous visual information"

3. Solution Path Layer
   - Progressive conclusion building: "Develop conclusions through explicit reasoning steps"
   - Verification methodology: "Apply specific tests to validate visual-textual interpretations"
   - Boundary condition awareness: "Identify when visual evidence is insufficient for reliable conclusions"

Implementation example:
"Analyze this engineering failure case using structured visual reasoning:

1. Observation stage:
   - Document all visible damage patterns and affected components
   - Note spatial relationships between damaged and intact areas
   - Extract measurements and deformation patterns where possible

2. Evidence analysis:
   - Categorize observations into primary damage and secondary effects
   - Identify temporal sequence indicators (which failures preceded others)
   - Match visible patterns with known failure modes in these materials

3. Causal reasoning:
   - Evaluate multiple hypotheses that could explain the observed damage pattern
   - Test each hypothesis against all available visual and contextual evidence
   - Eliminate inconsistent explanations and rank remaining possibilities by probability

4. Conclusion development:
   - Articulate the most likely failure sequence with specific supporting evidence
   - Indicate confidence level for each component of the analysis
   - Specify what additional information would be required to increase certainty"
```

### Cross-Modal Translation Framework
```
# Modality Transformation Techniques

1. Visual-to-Textual Translation
   - Structured description: "Convert diagram into hierarchical textual representation"
   - Process narration: "Transform flowchart into sequential procedural steps"
   - Spatial verbalization: "Translate physical layout into relationship descriptions"

2. Textual-to-Visual Guidance
   - Structure suggestion: "Recommend visualization type for this textual data"
   - Element organization: "Propose spatial arrangement to represent described relationships"
   - Visual hierarchy: "Suggest emphasis techniques to maintain the textual priorities"

3. Cross-Modal Verification
   - Consistency checking: "Verify alignment between textual claims and visual evidence"
   - Information preservation: "Ensure all critical data points persist across modalities"
   - Cognitive equity: "Balance information accessibility across visual and verbal learning preferences"

Implementation example:
"Transform this technical diagram into comprehensive textual documentation:

1. Component inventory:
   - Create a hierarchical list of all system components with their relationships
   - Translate visual attributes (size, color, position) into explicit importance and role descriptors
   - Convert connection types (lines, arrows) into explicit relationship statements

2. Process description:
   - Transform the visual flow into sequential steps with clear order and conditions
   - Convert branch points into explicit decision criteria
   - Translate parallel paths into concurrent process descriptions

3. Reference system:
   - Create a consistent naming convention for all components
   - Develop a cross-reference system between diagram elements and textual sections
   - Include metadata about spatial relationships that may carry implicit meaning

Format the documentation to serve both as a standalone text and as a companion reference to the original diagram."
```

## Application Integration Patterns

### Development Workflow Integration
```
# Multimodal Software Development Workflow

1. Requirements Analysis Phase
   - Visual-textual specification analysis: "Extract functional requirements from mockups + text docs"
   - UI/UX interpretation: "Translate design visuals into technical implementation requirements"
   - Constraint identification: "Determine technical limitations from system diagrams + specifications"

2. Implementation Guidance Phase
   - Pattern recognition: "Identify UI component patterns that match design visuals"
   - Visual-to-code translation: "Generate implementation code based on design screenshots"
   - Layout structuring: "Convert visual hierarchies into appropriate HTML/CSS structures"

3. Testing & Validation Phase
   - Visual regression detection: "Compare before/after screenshots to identify unintended changes"
   - Accessibility assessment: "Evaluate UI against accessibility standards using visual evidence"
   - Cross-platform verification: "Analyze screenshots across devices for responsive design issues"

Implementation example:
"Implement this product detail page based on the provided mockup and specifications:

1. First I'll analyze the visual components in the mockup:
   - Hero product image with gallery thumbnails
   - Product title, price, and availability indicator
   - Option selectors (size, color, quantity)
   - Add-to-cart and wishlist buttons
   - Product description tabs with expandable sections

2. Now I'll generate the React component structure:
   - Container component with responsive grid layout
   - Image gallery component with main/thumbnail functionality
   - Product metadata section with pricing and availability
   - Options selection component with validation
   - Action button group with primary/secondary styling
   - Expandable tabs component for description content

3. Implementation considerations based on specifications:
   - Ensure gallery component handles variable image ratios
   - Implement skeleton loading state for product data
   - Add inventory check before enabling add-to-cart
   - Ensure all interactive elements have proper focus states
   - Apply the design system typography and color tokens"
```

### Education & Training Integration
```
# Multimodal Learning Experience Framework

1. Conceptual Explanation Phase
   - Visual concept mapping: "Illustrate relationships between key concepts"
   - Comparative visualization: "Show visual examples of correct vs. incorrect approaches"
   - Process visualization: "Transform sequential steps into visual workflow"

2. Application Demonstration Phase
   - Annotated examples: "Provide labeled visual examples with explanation text"
   - Step-by-step breakdown: "Show progressive stages with explanatory captions"
   - Conditional pathways: "Visualize decision trees with outcome illustrations"

3. Comprehension Validation Phase
   - Visual problem-solving: "Present scenario images for analysis application"
   - Concept identification: "Request identification of principles in new examples"
   - Implementation guidance: "Ask for recommendations based on visual scenarios"

Implementation example:
"Create a lesson on database indexing performance using multimodal techniques:

1. Concept introduction:
   - Visual comparison showing query execution with and without indexes
   - Animated diagram of how B-tree index structures organize data
   - Side-by-side execution plan visualization showing performance difference

2. Application examples:
   - Screenshots of database tables with appropriate/inappropriate index designs
   - Annotated query examples highlighting where indexes are utilized
   - Performance graphs showing impact of different indexing strategies

3. Interactive elements:
   - Database schema images with prompts to identify optimal indexing opportunities
   - Query execution plans with questions about performance bottlenecks
   - Case study screenshots of real-world database performance issues to diagnose

4. Assessment activities:
   - Present a complex database schema image and ask for indexing recommendations
   - Show query performance statistics and request optimization suggestions
   - Provide before/after scenarios to evaluate indexing impact"
```

### Data Science Workflow Integration
```
# Multimodal Data Analysis Framework

1. Exploratory Analysis Phase
   - Visual pattern identification: "Describe notable patterns in these data visualizations"
   - Anomaly detection: "Identify outliers or unusual patterns in these plots"
   - Correlation discovery: "Analyze relationships between variables across these charts"

2. Insight Development Phase
   - Hypothesis generation: "Suggest possible explanations for the patterns in these visuals"
   - Cross-visualization synthesis: "Integrate insights from multiple charts into cohesive findings"
   - Contextual interpretation: "Explain these data patterns in the context of the business problem"

3. Communication Guidance Phase
   - Visualization recommendation: "Suggest the most effective visualization types for these insights"
   - Narrative structuring: "Develop a data story using these visualizations as evidence"
   - Audience adaptation: "Modify these technical visualizations for executive presentation"

Implementation example:
"Analyze this e-commerce dashboard dataset with visualization:

1. Initial exploration:
   - Describe the key trends visible in the sales time series visualization
   - Identify notable patterns in the customer segment distribution chart
   - Analyze the geographic heat map for regional performance variations
   - Examine the product category comparison for relative performance

2. Integrated analysis:
   - Connect the seasonal patterns in the time series with promotional events marked in the calendar view
   - Correlate customer segment performance with marketing channel effectiveness
   - Analyze how product category performance varies across different regions
   - Identify relationships between customer retention visualization and sales growth

3. Insight development:
   - Formulate hypotheses about the causes of observed performance variations
   - Prioritize findings based on business impact suggested by the visualization
   - Recommend additional analyses to investigate unexpected patterns
   - Suggest visualization improvements to better highlight key insights

4. Action recommendations:
   - Propose specific business actions based on the integrated visual analysis
   - Identify target segments, regions, or products for intervention
   - Suggest A/B testing opportunities based on observed patterns
   - Outline a measurement framework to track the impact of recommendations"
``` 