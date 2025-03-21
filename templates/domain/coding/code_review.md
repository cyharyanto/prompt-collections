# Code Review Template

## Template Structure
```
# Code Review Request

## CONTEXT
- Application type: [type/domain]
- Functionality: [specific functionality]
- Purpose: [core purpose/goal]
- Tech stack: [languages/frameworks/libraries]

## REVIEW FOCUS
[priority_1]: [specific aspects] 
[priority_2]: [specific aspects]
[priority_3]: [specific aspects]

## SPECIFIC CONCERNS
- [concern_1]: [detail/question]
- [concern_2]: [detail/question]

## CODE
```[language]
[code_block]
```

## REQUESTED DELIVERABLE
- Format: [assessment structure]
- Emphasis: [primary focus areas]
- Action items: [how to present recommendations]
```

## Usage Guidelines

1. **Context specification**
   - Provide sufficient technical environment information
   - Include architectural constraints and dependencies
   - Note performance/security requirements if applicable

2. **Focus prioritization**
   - List 2-4 review dimensions in priority order
   - Use standard categories: security, performance, readability, maintainability
   - Include specific subcategories when relevant

3. **Code preparation**
   - Remove irrelevant sections with `// ... omitted ...` placeholders
   - Include sufficient surrounding context for functions/methods
   - Ensure all referenced dependencies are mentioned

4. **Review structuring**
   - Request severity classification for issues
   - Specify desired format (list vs. prose vs. annotated)
   - Request actionable refactoring suggestions

## Example Implementation

```
# Code Review Request

## CONTEXT
- Application: React SPA with JWT authentication
- Functionality: User authentication module
- Purpose: Manage login/session validation/logout
- Tech stack: React 17, Hooks, Axios, localStorage

## REVIEW FOCUS
Security: token handling, auth validation, secure storage
Performance: unnecessary re-renders, memory management
Error handling: edge cases, user feedback, recovery

## SPECIFIC CONCERNS
- Token storage: Are there security risks with current localStorage approach?
- useEffect dependency: Is our dependency array correct for session validation?
- Race conditions: Any potential issues with async auth operations?

## CODE
```javascript
import React, { useState, useEffect } from 'react';
import axios from 'axios';

const AuthManager = () => {
  const [token, setToken] = useState(localStorage.getItem('authToken'));
  const [user, setUser] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);
  
  const login = async (credentials) => {
    try {
      setLoading(true);
      const response = await axios.post('/api/login', credentials);
      const { token, user } = response.data;
      localStorage.setItem('authToken', token);
      setToken(token);
      setUser(user);
      return true;
    } catch (err) {
      setError(err.response?.data?.message || 'Login failed');
      return false;
    } finally {
      setLoading(false);
    }
  };
  
  const logout = () => {
    localStorage.removeItem('authToken');
    setToken(null);
    setUser(null);
  };
  
  const validateSession = async () => {
    if (!token) {
      setLoading(false);
      return;
    }
    
    try {
      const response = await axios.get('/api/validate', {
        headers: { Authorization: `Bearer ${token}` }
      });
      setUser(response.data.user);
    } catch (err) {
      logout();
      setError('Session expired');
    } finally {
      setLoading(false);
    }
  };
  
  useEffect(() => {
    validateSession();
  }, []);
  
  return { user, token, loading, error, login, logout };
};

export default AuthManager;
```

## REQUESTED DELIVERABLE
- Priority-ordered issue list with severity indicators (High/Medium/Low)
- Code samples for recommended fixes
- Security best practices for auth implementation
``` 