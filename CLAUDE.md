# CLAUDE.md - Repository Maintenance Guide

## Repository Overview

This repository contains a comprehensive framework for prompt engineering across multiple domains. It's structured to provide both foundational knowledge and practical implementation guidance. This document will help you understand the repository organization and maintain consistency when making updates.

## Repository Structure

The repository is organized into several key directories:

- **docs/**: Core knowledge organized in progressive complexity
  - **fundamentals/**: Foundation concepts (mental models, limitations, context management)
  - **prompt_patterns/**: General techniques (chain of thought, few-shot, role prompting)
  - **domains/**: Field-specific applications (coding, writing, data analysis, education)
  - **advanced/**: Complex implementations (RAG, multimodal, system design)
- **examples/**: Practical implementations of concepts
- **templates/**: Reusable prompt structures
- **src/**: Functional code examples and maintenance documentation
  - **system_prompts/**: Ready-to-use system prompts
  - **maintenance_note.md**: High-density maintenance guidelines

Additionally, the repository root contains high-density reference files:
- **llms.txt**: Hyperdense repository navigation index optimized for LLM consumption

### Knowledge Hierarchy

The repository follows a progression from foundational to specialized knowledge:

1. **Fundamental concepts** provide the base understanding
2. **Prompt patterns** build on fundamentals with general techniques
3. **Domain applications** apply patterns to specific fields
4. **Advanced topics** integrate multiple concepts for complex systems

## Document Relationships

### Navigation System

Each document includes standardized navigation:

```
> **Navigation**: [Path to current document]
> 
> **Previous**: [Document that comes before] | **Next**: [Document that follows]
> 
> **Related**: [Conceptually related documents]
```

These navigation elements maintain the knowledge graph and should remain consistent when updating documents.

### Content Structure

Most documents follow this structure:

1. **Quick Summary**: Three-part summary with beginner explanation, practitioner view, and key takeaway
2. **Main Content**: Detailed explanation of concepts organized in sections
3. **Implementation Examples**: Practical applications of the concepts
4. **Tables and Matrices**: Comparative information in structured format

## Update Guidelines

### Update Types

The repository contains several types of information that require different update frequencies:

| Content Type | Update Frequency | Examples |
|--------------|------------------|----------|
| Fundamental concepts | Low (stable) | Mental models, reasoning patterns |
| Technical parameters | High (changes with models) | Context window sizes, token limits |
| Implementation techniques | Medium | Best practices, optimization approaches |
| Performance metrics | High | Efficiency statistics, improvement percentages |

### High-Density Reference Documents

Two special documents use a higher information density format than the rest of the repository:

- **/llms.txt**: A hyperdense repository index optimized for LLM consumption containing:
  - Complete repository structure and relationships
  - Condensed concept maps and implementation matrices
  - Technical parameters and optimization techniques
  - Quick-reference templates and navigation shortcuts
  
- **/src/maintenance_note.md**: Condensed maintenance guidelines with:
  - Update protocols and dependency mappings
  - Value persistence classifications
  - Obsolescence triggers and maintenance schedules

These high-density documents serve as efficient reference points for AI agents and should be maintained alongside regular documentation but preserve their condensed format.

### Update Process

When incorporating new information:

1. **First identify** which documents are affected by the new information
2. **Start with fundamentals** if core concepts need updating
3. **Update prompt patterns** to reflect new techniques or capabilities
4. **Revise domain applications** to incorporate updated patterns
5. **Check cross-references** to maintain link integrity

### Consistency Considerations

1. **Terminology**: Use consistent terms across all documents
2. **Navigation**: Ensure all links remain valid after updates
3. **Examples**: Update examples to reflect changed recommendations
4. **Performance claims**: Update metrics when new data is available

## Document Templates

### Standard Document Structure

```markdown
# Title

> **Navigation**: [Path links] | [Current location]
> 
> **Previous**: [Previous doc] | **Next**: [Next doc]
> 
> **Related**: [Conceptually related pages]

## Quick Summary
**For beginners**: [Simplified explanation]
**For practitioners**: [Advanced perspective]
**Key takeaway**: [Core insight]

---

# Main Content Title

## Section Heading
Content...

### Subsection
More specific content...
```

### Matrix Format

Many documents use matrices to compare approaches:

| Dimension | Properties | Implementation | Application |
|-----------|------------|----------------|-------------|
| **Category** | Key attributes | How to implement | When to use |

### Framework Presentation

Implementation frameworks typically follow this structure:

```
# Framework Name

1. Component Name
   - Element: [description]
   - Element: [description]

2. Component Name
   - Element: [description]
   - Element: [description]
```

## Verification Checklist

When updating the repository, verify:

1. **Navigation integrity**: All links point to valid documents
2. **Terminology consistency**: Terms mean the same thing across documents
3. **Knowledge dependencies**: Advanced concepts properly reference foundations
4. **Example alignment**: Examples match the patterns they demonstrate
5. **Format consistency**: Documents follow established templates
6. **Technical accuracy**: Parameters and metrics reflect current capabilities
7. **High-density synchronization**: Changes to regular documents are reflected in high-density references (llms.txt and maintenance_note.md)

## Technical Parameters

When updating technical parameters (which change frequently), pay attention to:

1. **Context window sizes**: Adjust recommendations for different window capacities
2. **Token efficiency**: Update compression techniques and their effectiveness
3. **Performance metrics**: Revise measured impacts of different techniques
4. **Model capabilities**: Update recommendations based on new capabilities

## Expansion Guidelines

When adding new content:

1. **Maintain the hierarchy**: Connect new content to existing knowledge
2. **Follow templates**: Use consistent formatting for new documents
3. **Update navigation**: Add appropriate links to and from new content
4. **Cross-reference**: Establish connections to related documents

## Common Update Scenarios

### Model Capability Changes

When model capabilities change:

1. Update context window parameters in `context_management.md`
2. Revise token efficiency techniques in relevant documents
3. Adjust performance metrics based on new capabilities
4. Update recommendations that depend on these capabilities

### New Prompt Techniques

When new prompt techniques emerge:

1. Determine if they're variants of existing patterns or entirely new
2. Update relevant documents or create new documents as appropriate
3. Add examples demonstrating the new techniques
4. Connect to existing knowledge through proper navigation

### Domain-Specific Updates

When updating domain-specific guidance:

1. Ensure alignment with current fundamental concepts
2. Update examples to reflect best practices
3. Revise performance claims based on new data
4. Maintain connection to general prompt patterns

## Maintaining Knowledge Integrity

The value of this repository comes from its consistent, interconnected knowledge. When making updates:

1. Consider how changes affect related documents
2. Update in a systematic way, starting with fundamentals
3. Maintain the appropriate level of detail and density
4. Preserve the connection between theory and practice

## Repository Tools

### Repository Summarization

When analyzing the repository structure or content:

1. Use the **repomix** tool to generate a comprehensive summary of the repository:
   ```
   repomix /path/to/repository > repomix-output.txt
   ```
2. The generated `repomix-output.txt` file contains a consolidated view of the repository structure and content
3. This file is ephemeral and should NOT be committed to the repository
4. After analysis is complete, you can safely delete this temporary file
