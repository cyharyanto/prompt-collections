# Prompt Evaluation Framework

## Evaluation Dimensions
| Dimension | Definition | Measurement Approach |
|-----------|------------|---------------------|
| **Accuracy** | Factual correctness, logical soundness | Fact verification, reasoning validation, gold-standard comparison |
| **Relevance** | Query-response alignment, topic adherence | Intent matching, distraction quantification, information density |
| **Completeness** | Comprehensive coverage of requested elements | Component presence check, scope fulfillment, depth analysis |
| **Format Compliance** | Adherence to specified structure/constraints | Schema validation, pattern matching, constraint satisfaction |
| **Consistency** | Internal coherence, cross-response stability | Contradiction detection, variance analysis, belief persistence |
| **Efficiency** | Token economy, information-to-noise ratio | Token utilization metrics, compression ratio, content density |

## Domain-Specific Evaluation Matrices

### Code Generation Matrix
| Criterion | Priority Weight | Evaluation Method | Failure Modes |
|-----------|----------------|-------------------|---------------|
| Syntax validity | Critical | AST parsing, compilation testing | Invalid tokens, scope errors, type mismatches |
| Functional correctness | High | Test case execution, edge case testing | Logic errors, boundary condition failures, incorrect outputs |
| Performance characteristics | Medium | Profiling, complexity analysis, benchmarking | Inefficient algorithms, memory leaks, unnecessary operations |
| Security considerations | High | Vulnerability scanning, threat modeling | Injection vulnerabilities, authentication weaknesses, data exposure |
| Standard adherence | Medium | Style checking, pattern validation | Convention violations, antipatterns, readability issues |

### Content Creation Matrix
| Criterion | Priority Weight | Evaluation Method | Failure Modes |
|-----------|----------------|-------------------|---------------|
| Tone/style matching | High | Linguistic feature analysis, target comparison | Register misalignment, inconsistent voice, inappropriate formality |
| Factual accuracy | Critical | Source verification, expert validation | Fabrications, outdated information, misrepresented data |
| Structural compliance | Medium | Template matching, section verification | Missing components, organizational flaws, flow disruption |
| Audience appropriateness | High | Readability metrics, domain terminology analysis | Comprehension barriers, irrelevant content, motivational mismatch |
| Originality | Medium | Plagiarism detection, novelty measurement | Content duplication, generic phrasing, predictable patterns |

### Data Analysis Matrix
| Criterion | Priority Weight | Evaluation Method | Failure Modes |
|-----------|----------------|-------------------|---------------|
| Analytical correctness | Critical | Statistical validation, methodology review | Calculation errors, inappropriate methods, invalid assumptions |
| Insight relevance | High | Business impact assessment, decision influence | Triviality, misaligned priorities, obvious observations |
| Methodological soundness | High | Process validation, technical appropriateness | Invalid techniques, improper data handling, inappropriate tools |
| Explanation clarity | Medium | Comprehension testing, technical accuracy check | Jargon overuse, logical gaps, conceptual confusion |
| Visualization appropriateness | Medium | Information design assessment, perception testing | Misleading representations, ineffective encodings, cognitive overload |

## Implementation Roadmap

### Phase 1: Metrics Framework
- Dimension-specific quantification methods
- Composite scoring algorithms
- Benchmark dataset creation
- Baseline performance establishment

### Phase 2: Automated Evaluation Tools
- Syntax validation scripts
- Content analysis libraries
- Multi-dimensional comparison utilities
- Failure mode detection systems

### Phase 3: Continuous Improvement Infrastructure
- Feedback collection mechanisms
- A/B prompt testing framework
- Version control integration
- Performance tracking dashboard 