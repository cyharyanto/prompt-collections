# Understanding Our Working Assumptions

When we work with AI code assistants, we're operating under several important technical constraints and assumptions that shape how these systems interact with code. Understanding these assumptions helps us work more effectively with these tools and design better approaches for code analysis.

## Context Window Limitations

The context window of an AI model is like a spotlight illuminating a section of a large mural. No matter how powerful the model, it can only "see" what falls within this spotlight at any given moment. This fundamental limitation affects how we work with code in several important ways.

When we're dealing with a typical context window of 8K-32K tokens, we need to think carefully about what code we show the AI. A single large source file might consume the entire context window, leaving no room for the AI to receive additional instructions or provide detailed analysis. Even with larger context windows of 100K tokens or more, we still need to be strategic about context management.

Think of it this way: if you were helping someone understand a large codebase through a video call where they could only see a few files at a time, you'd need to be very thoughtful about which files you share and in what order. You'd want to show them the most relevant pieces that help them understand the specific problem at hand.

## Code Retrieval Mechanisms

The way we find and present relevant code to the AI is crucial, and different approaches have different strengths and limitations:

Vector search works like finding similar paintings in an art gallery based on their overall style and composition. It's good at finding code that looks similar, but might miss functionally related code that looks different. For example, it might find all instances of authentication middleware in your codebase, but miss the configuration files that control how that middleware behaves.

Knowledge graph approaches are more like having a map of how different parts of a museum connect to each other. They can help find related code based on dependencies and relationships, even when the code itself looks quite different. However, they require careful maintenance and might miss newer or undocumented relationships.

Keyword-based lookup is like having an index in a book – direct and precise, but potentially missing relevant code that uses different terminology. It might find all uses of "authenticateUser", but miss related code that uses "validateCredentials" instead.

Each of these approaches has its own bias:
- Vector search tends to favor superficial similarity
- Knowledge graphs can be incomplete or outdated
- Keyword search can miss semantic relationships

## Language Model Behaviors

Understanding how language models process and analyze code helps us work with their natural tendencies rather than against them:

Models excel at pattern recognition but can sometimes be too eager to apply familiar patterns. They might try to force-fit a common design pattern onto code that intentionally deviates from it. This is like someone who knows classical music trying to apply those rules to jazz – the patterns they know might not always be appropriate.

Models often exhibit a recency bias, giving more weight to code they've seen most recently in the context window. This is similar to how a person might focus more on the last few pages they've read in a long document. We need to structure our interactions to account for this, sometimes restating important earlier context.

Models can also show training distribution bias. If they've seen thousands of React components but only a few Svelte components in their training data, they might try to apply React patterns inappropriately to Svelte code. This is like someone who has spent years working with one framework trying to apply those practices in a different framework.

## Practical Implications

Understanding these assumptions leads to several practical strategies:

1. We need to be explicit about context boundaries and deliberately manage what code the AI can see. This might mean breaking down large analysis tasks into smaller, focused sessions with carefully chosen context.
2. We should combine different code retrieval approaches to get a more complete picture. For example, using vector search to find similar implementations, then using knowledge graphs to find related configurations and dependencies.
3. We must actively guide the model away from inappropriate pattern matching, especially when working with novel or unique code structures. This means being explicit about when common patterns don't apply and explaining why our implementation is different.

These assumptions aren't just theoretical concerns – they directly affect how we structure our interactions with AI code assistants and what results we can expect from them. By understanding these limitations, we can design better workflows and get more reliable results from our AI tools.
