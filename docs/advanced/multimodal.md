# Multimodal Prompting

## System Capabilities
- **Processing scope**: Images, audio, video, structured data, and combinations
- **Core functions**: Object recognition, text extraction, relationship analysis, context integration
- **Performance factors**: Resolution, quality, context window allocation, modality balance

## Technique Matrix

| Technique | Application | Implementation |
|-----------|-------------|----------------|
| Cross-modal reasoning | Relationship analysis | `Analyze relationship between [object] in image and [context] in text` |
| Visual grounding | Object identification | `Locate and describe [entity] with specific attributes` |
| Sequential processing | Complex analysis | `First describe image → then analyze specific components → finally integrate with text` |
| Parallel input | Comparative analysis | `Compare visual elements with numerical data` |

## Application Domains
- **Document analysis**: Form extraction, layout understanding, data validation
- **Visual QA**: Image interpretation, contextual answers, reasoning chains
- **Multimodal synthesis**: Report generation, content transformation, insight extraction
- **Temporal analysis**: Video progression, audio-video alignment, event detection

## Prompt Pattern: Analytical Decomposition
```
Input: [image/audio/video] + [contextual text]

1. Observation layer: Identify core elements without interpretation
   * Visual: objects, text, spatial relationships, colors/patterns
   * Audio: speakers, sounds, music, transitions, quality
   * Video: scenes, movements, temporal patterns, key frames

2. Interpretation layer: Derive meaning from observations
   * Contextual significance of [specific element]
   * Relationship between [elements A] and [element B]
   * Patterns or anomalies in [specific area/section]

3. Integration layer: Connect with external knowledge/context
   * Compare observations with [domain knowledge/reference point]
   * Analyze implications for [specific purpose]
   * Synthesize findings into [required output format]

4. Output requirements: [format/structure/focus of response]
```

## Technical Constraints
- **Modality gaps**: Bridge semantic distance between visual and textual understanding
- **Context management**: Allocate tokens efficiently across modalities
- **Reference precision**: Establish clear referencing conventions between modalities
- **Bias mitigation**: Apply balancing techniques for interpretation fairness 