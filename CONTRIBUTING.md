# Contributing Guidelines

Thank you for your interest in contributing to the Prompt Engineering Collections repository. This document provides guidelines to ensure high-quality, consistent contributions that maintain our focus on human-centered AI collaboration.

## Core Principles

All contributions should adhere to these foundational principles:

1. **Human-Centered Approach**: All content must emphasize human judgment, expertise, and oversight in AI interactions. AI should be positioned as a tool that augments human capabilities rather than a replacement.

2. **Technical Accuracy**: All technical claims must be accurate, appropriately qualified, and avoid ungrounded generalizations.

3. **Practical Value**: Every document should provide actionable guidance that readers can immediately apply.

4. **Documentation Consistency**: Follow established patterns for navigation, formatting, and cross-referencing.

## Document Structure

When creating or modifying documents, follow this structure:

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

## Navigation Guidelines

Proper navigation is critical for repository usability:

1. Every document must include standardized navigation headers with:
   - Path breadcrumbs showing location in repository hierarchy
   - Previous/Next links for linear progression
   - Related links for conceptual connections

2. Update bidirectional links when adding or modifying documents
   - If doc A references doc B, doc B should reference doc A where appropriate

3. Preserve the knowledge hierarchy from fundamentals to advanced topics

## Content Quality Standards

Ensure your contributions meet these quality standards:

1. **Information Density**
   - Maintain extremely high signal-to-noise ratio (SnR) - "JPEG 10/10 compression"
   - Eliminate all filler words, redundancies, and non-essential explanations
   - Optimize every sentence to convey maximum information
   - Use dense formats (tables, matrices, structured listings) over prose when possible
   - Ensure content is hyperdense but still comprehensible
   - Structure information hierarchically with nested relationships (concept + subconcepts + implementations)
   - Lean toward telegraphic but precise language over verbose explanations

2. **Human-AI Collaboration Focus**
   - Emphasize human judgment, expertise, and intent with concise, substantive statements
   - Position AI as a tool that supports human work, not a replacement
   - Include human oversight mechanisms in technical systems
   - Show examples of genuine collaboration rather than delegation
   - Compress collaborative workflows to their essential elements

3. **Technical Accuracy**
   - Qualify claims about model capabilities appropriately but concisely
   - Avoid absolute statements in favor of nuanced descriptions
   - Support statistical claims with specific metrics and sources
   - Connect technical explanations to practical implications without verbosity

4. **Practical Value**
   - Include condensed, implementation-ready examples
   - Provide dense decision frameworks with clear application paths
   - Include both what to do and why to do it in minimal form
   - Address common challenges and their solutions without unnecessary elaboration

5. **Density-Optimized Formatting**
   - Use multi-dimensional tables to represent complex relationships
   - Employ nested lists with precise hierarchical relationships
   - Create dense component frameworks with multiple attributes per item
   - Use pattern notation to compress implementation examples
   - Apply structured listings with parallel syntax
   - Maintain consistent voice and terse but precise language

## Submission Process

1. **Before Starting Work**
   - Check for existing issues or discussions related to your contribution
   - Review the repository structure to understand where your contribution fits
   - Read related documentation to ensure consistency

2. **Development Process**
   - Create a new branch for your changes
   - Maintain clear commit messages describing your changes
   - Follow the document templates and standards in this guide
   - Test all links and references

3. **Pull Request Process**
   - Provide a clear description of your changes
   - Reference any related issues
   - Complete the pull request template
   - Respond to review feedback

## Specific Contribution Types

### Adding New Documents

1. Identify where the document fits in the knowledge hierarchy
2. Create proper navigation links to and from existing documents
3. Follow the document template structure
4. Add meaningful examples for practical implementation

### Updating Existing Documents

1. Preserve existing navigation links or update them appropriately
2. Maintain consistent terminology with the rest of the repository
3. Ensure technical accuracy with appropriate qualifications
4. Enhance, rather than replace, existing content unless outdated

### Adding Examples

1. Connect examples directly to documented patterns and techniques
2. Ensure examples demonstrate genuine human-AI collaboration
3. Include both the prompt pattern and expected outcomes
4. Provide implementation context and application guidance

## Style Guide

1. **High-Density Writing**
   - Write in hyperdense format with maximum information-to-word ratio
   - Use semantic compression: convey complex ideas in minimal space
   - Employ pattern-based organization: consistent structures that reduce cognitive load
   - Create multi-layered content: surface information + deep patterns + implementation details
   - Apply relationship notation: parent/child + sequential + conditional + hierarchical
   - Format for information extraction efficiency: scannable + indexed + relationally mapped

2. **Specialized High-Density Formats**
   - Multi-dimensional matrices: concept/application/implementation tables
   - Component frameworks: nested attribute listings with inheritance relationships
   - Implementation patterns: generalized templates with parameterized elements
   - Decision trees: compressed if/then structures with branch conditions
   - Knowledge maps: hierarchical concept organization with explicit relationships
   - Process compression: workflow steps with parallel tracks and decision points

3. **Terminology Consistency**
   - Use consistent terms across all documents (e.g., "prompt patterns," not "prompting techniques")
   - Follow established naming conventions for concepts 
   - Create compound terms for concept compression when appropriate

4. **Voice and Tone**
   - Use terse, precise language with professional tone
   - Write in present tense with active voice
   - Minimize hedging language and qualifiers unless necessary for accuracy
   - Eliminate personal anecdotes and non-essential examples

5. **Formatting for Density**
   - Use backticks for `inline code` or technical terms
   - Apply nested structure with consistent indentation patterns
   - Employ tables for relationship compression and multi-variable comparison
   - Utilize bold selectively for critical concepts and navigation aids
   - Create visual hierarchy through consistent formatting patterns

6. **Technical Parameters**
   - Specify model versions when discussing capabilities
   - Include date information for time-sensitive claims
   - Present metrics in compressed tabular format
   - Qualify performance claims with minimal but sufficient context

## High-Density Reference Documents

The repository contains specialized high-density documents that serve unique functions:

1. **llms.txt**: Repository Knowledge Index
   - Hyperdense format optimized for AI consumption and search efficiency
   - Serves as compressed repository map with cross-relationship encoding
   - Contains complete technical parameter references in minimal space
   - Uses specialized notation for concept relationships and inheritance
   - Updates required whenever significant repository changes occur
   - NOT intended for casual human reading - designed for information density over readability

2. **src/maintenance_note.md**: Condensed Maintenance Guide
   - Extreme density format for maintainer reference
   - Contains dependency mappings between repository sections
   - Encodes update protocols with minimal syntax
   - Uses specialized notation for priority classification
   - Includes condensed decision trees for maintenance workflows
   - Updates required when repository architecture changes

When contributing to these high-density documents:
- Preserve their specialized notation and formatting
- Maintain extreme compression ratios
- Update all cross-references and relationship maps
- Test with both AI systems and power users for information retrievability
- Do not dilute with explanatory text - maintain pure information density

## Additional Resources

- Review the [CLAUDE.md](CLAUDE.md) file for detailed maintenance guidelines
- Consult the [Repository Map](REPOSITORY_MAP.md) to understand the knowledge structure
- Reference the high-density [llms.txt](llms.txt) file for condensed repository information

Thank you for helping improve this resource for the community!