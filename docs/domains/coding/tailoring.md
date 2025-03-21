# Adapting to Different AI Models

> **Navigation**: [Fundamentals](../../fundamentals/) | [Prompt Patterns](../../prompt_patterns/) | `Domains` → Coding → Tailoring
> 
> **Previous**: [Methodology](methodology.md) | **Next**: [Code Analysis](code_analysis.md)
> 
> **Related**: [Mental Models](../../fundamentals/mental_models.md), [Assumptions](../../fundamentals/assumptions.md)

## Quick Summary
**For beginners**: This document shows you how to adapt your approach based on the AI model you're using, whether it's a smaller or larger model with different capabilities.

**For practitioners**: A framework for optimizing interactions with different model sizes, architectures, and specializations, with specific strategies for adapting to context windows and model capabilities.

**Key takeaway**: Different AI models require different prompting strategies. This guide helps you tailor your approach for maximum effectiveness based on model size, context window, and specialized capabilities.

---

# Adapting Your Approach for Different AI Models

When working with AI code assistants, we need to understand that different models have different capabilities and limitations, much like how different programming languages excel at different types of tasks. Just as you might approach a problem differently in Python versus C++, you need to adapt your approach based on the AI model you're working with.

## Understanding Model Characteristics

Let's explore how different aspects of AI models affect how we work with them, starting with the most fundamental characteristic: context window size.

### The Impact of Context Windows

Think of a context window like a workspace where you and the AI can examine code together. Different models have different workspace sizes, which affects how you need to organize your collaboration.

Working with Small Context Windows (4K-8K tokens):
```python
# When working with small context windows, you might need to break down
# even a moderate-sized class into multiple conversations

# First conversation - class structure
class UserService:
    def __init__(self, repository, auth_provider):
        self.repository = repository
        self.auth_provider = auth_provider

# Second conversation - authentication methods
    def authenticate_user(self, credentials):
        # Implementation details
        pass
    
    def validate_token(self, token):
        # Implementation details
        pass

# Third conversation - user management methods
    def create_user(self, user_data):
        # Implementation details
        pass
    
    def update_user(self, user_id, data):
        # Implementation details
        pass
```

When working with small context windows, we need to:
1. Break down analysis into focused, single-purpose conversations
2. Carefully manage what context we include
3. Explicitly connect insights from different conversations

Working with Large Context Windows (32K-100K+ tokens):
```python
# With larger context windows, we can include more related code
# and supporting information in a single conversation

class UserService:
    """Complete user management service implementation"""
    # Full implementation...

class UserRepository:
    """Data access layer for user management"""
    # Full implementation...

class AuthProvider:
    """Authentication provider implementation"""
    # Full implementation...

# Configuration
USER_SERVICE_CONFIG = {
    "token_expiry": 3600,
    "max_login_attempts": 3
}

# Tests
class TestUserService:
    """Test suite for user service"""
    # Full test implementation...
```

With larger context windows, we can:
1. Analyze multiple related components together
2. Include tests and configuration
3. Provide more comprehensive context

### Model Size and Capabilities

Different sized models require different approaches to interaction. Let's explore how to adapt our communication style based on model size.

Working with Smaller Models (7B-13B parameters):
```python
# When working with smaller models, be more explicit about patterns
# and break down complex concepts into simpler parts

# Instead of asking for generic analysis:
def process_transaction(transaction_data):
    # Implementation...

# Break down your questions:
# 1. "How does this function validate the input data?"
# 2. "What error handling patterns does it use?"
# 3. "How does it ensure transaction atomicity?"
```

Working with Larger Models (70B+ parameters):
```python
# Larger models can handle more complex analysis and inference
# but still benefit from clear communication

class PaymentProcessor:
    def __init__(self, payment_gateway, fraud_detector, logger):
        self.payment_gateway = payment_gateway
        self.fraud_detector = fraud_detector
        self.logger = logger
    
    def process_payment(self, payment_details):
        """
        Processes a payment with fraud detection and comprehensive logging.
        Implements retry logic for gateway timeouts and handles partial
        failures with compensating transactions.
        """
        # Implementation...

# You can ask more complex questions:
# "How does this implementation handle the interaction between 
#  fraud detection and payment processing, particularly around
#  timing and failure scenarios?"
```

## Adapting Communication Patterns

Just as you might explain a concept differently to a junior versus a senior developer, you need to adjust how you communicate with different AI models.

### For Smaller Models

Structure your queries to build understanding progressively:

```python
# Start with basic structure
"Let's look at the class definition and method signatures first"

class DataProcessor:
    def __init__(self, source, destination):
        self.source = source
        self.destination = destination
    
    def process_data(self, data):
        pass

# Then examine specific aspects
"Now let's look at how the process_data method validates its input"

# Finally connect the pieces
"How does this validation connect to the source and destination configuration?"
```

### For Larger Models

You can take a more holistic approach:

```python
# You can present more complex scenarios and ask for comprehensive analysis

class DataProcessor:
    def __init__(self, source, destination, validator):
        self.source = source
        self.destination = destination
        self.validator = validator
        
    def process_data(self, data):
        """Complex data processing with validation and error handling"""
        validated_data = self.validator.validate(data)
        processed = self.transform_data(validated_data)
        self.destination.store(processed)
    
    def transform_data(self, data):
        """Applies business rules and transformations"""
        # Implementation...

# You can ask about broader implications:
"How does this implementation handle the interaction between validation,
transformation, and storage, particularly around error scenarios?"
```

## Fine-Tuning Considerations

When working with fine-tuned models, we need to understand their specialization and adjust accordingly.

### Domain-Specific Models

For models specialized in certain domains:

```python
# A security-focused model might excel at analyzing code like this:
class AuthenticationManager:
    def validate_credentials(self, credentials):
        """
        Validates user credentials with proper security measures.
        Implements rate limiting, password complexity checks,
        and brute force protection.
        """
        # Implementation...

# You can dive directly into security-specific aspects:
"What security considerations does this implementation address?"
```

### General Models

For general-purpose models:

```python
# Provide more context about domain-specific requirements
class AuthenticationManager:
    # Explain domain requirements in comments
    """
    Authentication manager for financial services application.
    Must comply with SOX requirements for financial systems:
    - Multi-factor authentication required
    - Audit logging for all attempts
    - Complex password requirements
    """
    def validate_credentials(self, credentials):
        # Implementation...
```

## Continuous Adaptation

As AI models evolve, our interaction patterns should evolve too. Keep track of what works well:

```python
# Document effective patterns
"""
Interaction Pattern Log:

Model: Large Context (100K tokens)
Effective: Providing full class hierarchy with tests
Result: Better understanding of interaction patterns

Model: Small Context (8K tokens)
Effective: Breaking analysis into focused methods
Result: More precise, targeted insights
"""
```

Remember that regardless of model capability:
1. Clear communication always helps
2. Explicit context is better than implicit
3. Progressive building of understanding works well
4. Verification of understanding remains important

By thoughtfully adapting our approach based on model characteristics, we can work more effectively with AI code assistants of all sizes and capabilities.
