<!-- Navigation Guide -->
<!-- Previous: [Chain of Thought](chain_of_thought.md) | Next: [Role Prompting](role_prompting.md) -->
<!-- Path: [Fundamentals](../fundamentals/) → Prompt Patterns → [Chain of Thought](chain_of_thought.md) → Few-Shot → [Role Prompting](role_prompting.md) -->
<!-- Related: [Context Management](../fundamentals/context_management.md) -->

# Few-Shot Prompt Engineering

## Core Mechanics
| Component | Function | Optimization Strategy |
|-----------|----------|----------------------|
| **Example selection** | Task pattern demonstration | Diversity sampling + edge case inclusion + variation coverage |
| **Example ordering** | Learning trajectory establishment | Complexity progression + recency weighting + similarity proximity |
| **Format consistency** | Pattern recognition facilitation | Structural templating + delimiter standardization + variable positioning |
| **Example count** | Inference guidance calibration | Task complexity matching + memory constraints + domain unfamiliarity |

## Implementation Framework

### Pattern Specification
```
# Structure Components
- Input/output delimiter: [consistent separation marker]
- Example boundary: [inter-example separator]
- Variable indicators: [consistent placeholder notation]
- Format signaling: [structural consistency elements]

# Core Template
[intro text: task description + expected behavior]

[delimiter_1]Input:[delimiter_2] [example_1_input]
[delimiter_1]Output:[delimiter_2] [example_1_output]

[delimiter_1]Input:[delimiter_2] [example_2_input]
[delimiter_1]Output:[delimiter_2] [example_2_output]

[additional examples as needed]

[delimiter_1]Input:[delimiter_2] [target_input]
[delimiter_1]Output:[delimiter_2]
```

### Example Selection Matrix
| Dimension | Selection Criteria | Implementation Example |
|-----------|-------------------|------------------------|
| **Coverage** | Task subtype representation | Classification examples covering all categories |
| **Difficulty** | Progressive complexity | Simple → moderate → complex examples |
| **Diversity** | Input variation spectrum | Different formats, lengths, edge cases |
| **Relevance** | Similarity to target task | Examples matching target domain and style |

## Application Patterns

### Classification Optimization
- **Example strategy**: 1-2 examples per class + boundary case examples
- **Format design**: Explicit class labels + reasoning explanation (optional)
- **Order structure**: Balanced class representation + grouping by class
- **Enhancement**: Confidence indicators + multi-criteria reasoning

### Style Transfer Engineering 
- **Example strategy**: High-low style contrast + progressive style shift
- **Format design**: Input-output pairs showing clear style transformation
- **Order structure**: Style dimension isolation + combined transformations
- **Enhancement**: Style element labeling + transformation rationale

### Format Transformation
- **Example strategy**: Structure preservation examples + content variation
- **Format design**: Clear input-output format markers + annotation comments
- **Order structure**: Increasingly complex transformations + consistent positioning
- **Enhancement**: Format rule explanation + transformation breakdown

## Performance Optimization

### Count Optimization
```
Task complexity → Example requirements
- Simple classification: 1-2 examples per class
- Moderate reasoning: 3-5 total examples
- Complex transformation: 5-8 examples
- Hybrid/multi-step: 4-6 examples with subtask breakdown
```

### Debugging Techniques
- **Pattern misalignment**: Add explicit format instructions + increase example similarity
- **Incomplete pattern adoption**: Add intermediate reasoning steps + highlight pattern markers
- **Inconsistent outputs**: Standardize output structure + add format constraints
- **Task misunderstanding**: Add task description before examples + include counter-examples 