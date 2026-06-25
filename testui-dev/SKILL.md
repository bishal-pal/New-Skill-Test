---
name: test-ui
description: To design and generate modular, accessible React.js components specifically tailored for Retrieval-Augmented Generation (RAG) workflows and complex data visualization when requesting front-end code for chatbots, document retrieval systems, or translating technical system architecture diagrams into functional UI components.
---

## test-ui

This skill is designed to create reusable and accessible React.js components that facilitate the development of AI-integrated applications, focusing on Retrieval-Augmented Generation (RAG) workflows and complex data visualization. It provides developers with the necessary tools to translate design requirements into functional UI elements.

### Workflow Steps

1. **Identify Requirements**: Define the specific data and functionality needed for the UI component based on the project requirements.
2. **Select Component Type**: Choose the type of React component (functional or class-based) appropriate for the task.
3. **Generate Code**: Utilize the skill to generate the corresponding React.js component code in JSX or TSX format.
4. **State Management**: Implement state management solutions (like hooks or context) as needed to manage component state effectively.
5. **Accessibility Checks**: Ensure all components meet accessibility standards (e.g., ARIA roles, keyboard navigation).
6. **Testing**: Validate the component through unit tests to ensure functionality and integration within the broader application framework.
7. **Documentation**: Provide clear documentation on the component's usage, including props and state management details.

### Output Format

The output will be structured as follows:

```jsx
// React component code here
```
- **State Management Considerations**: Bullet points detailing how state is managed within the component.
- **Usability Considerations**: Bullet points outlining important usability features implemented.

### Examples

**Example 1: Chatbot UI Component**

Input:
```
Generate a chatbot UI component for user interaction.
```

Output:
```jsx
import React, { useState } from 'react';

const Chatbot = () => {
  const [messages, setMessages] = useState([]);

  const sendMessage = (message) => {
    // Logic to send message
  };

  return (
    <div>
      {/* Render chat messages */}
      <input type="text" onKeyPress={e => e.key === 'Enter' && sendMessage(e.target.value)} />
    </div>
  );
};
```
- **State Management**: Uses `useState` to manage chat messages.
- **Usability**: Supports Enter key for sending messages, ensuring smooth user interaction.

**Example 2: Document Retrieval Component**

Input:
```
Create a component to display document retrieval results.
```

Output:
```jsx
import React from 'react';

const DocumentResults = ({ results }) => (
  <ul>
    {results.map(result => (
      <li key={result.id}>{result.title}</li>
    ))}
  </ul>
);
```
- **State Management**: Accepts `results` as a prop to dynamically render document titles.
- **Usability**: Lists documents in an accessible format, ensuring screen readers can interpret the content.

### Anti-Patterns

- Avoid hardcoding values within components; always use props for flexibility.
- Do not neglect accessibility; ensure components are usable by everyone, including those using assistive technologies.
- Refrain from creating overly complex components that are difficult to maintain or integrate.

### Scope

This skill targets software engineers and UI developers working on AI-integrated applications. Future enhancements may include:
- Integration with design systems for consistent UI patterns.
- Support for additional frameworks beyond React (e.g., Vue, Angular).
- Advanced state management solutions tailored for complex applications.
- Improved documentation features for better developer onboarding.