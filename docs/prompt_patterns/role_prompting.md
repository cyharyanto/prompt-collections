# Role-Based Prompting

This document explores how to effectively use role assignments in prompts to improve AI responses.

## What is Role-Based Prompting?

Role-based prompting involves asking the AI to assume a specific persona, role, or expertise when responding to your queries. This technique leverages the model's ability to emulate different voices, expertise levels, and perspectives.

## Effective Implementation

- Defining clear roles with specific expertise
- Providing contextual background for the role
- Setting appropriate constraints
- Combining roles with other prompting techniques

## Common Role Types

- Domain Expert (e.g., "You are a senior software architect with 20 years of experience")
- Process Guide (e.g., "You are a writing coach helping improve my essay")
- Perspective Holder (e.g., "You are a critic analyzing this proposal")
- Specialized Tool (e.g., "You are a data visualization expert")

## Example Implementation

```
You are an experienced UX researcher with expertise in qualitative methods and user interview techniques. You have conducted hundreds of user studies and have a strong understanding of how to elicit meaningful insights while avoiding biased questions.

I need your help creating an interview script for a study about [product/service]. The target participants are [participant description]. Our research questions include:

1. [Research question 1]
2. [Research question 2]
3. [Research question 3]

Please create an interview guide that:
- Starts with appropriate warm-up questions
- Uses open-ended questions to explore key areas
- Includes effective follow-up prompts
- Avoids leading questions or introducing bias
- Ends with a proper conclusion

For each question, explain your rationale from a UX research perspective.
```

## Common Pitfalls

- Overly vague role definitions
- Conflicting role requirements
- Unrealistic expertise expectations
- Failing to align the role with the task

> Note: This is a placeholder document that will be expanded with detailed content. 