---
name: ui-devkit
description: To design and generate modular, accessible React.js components specifically tailored for Retrieval-Augmented Generation (RAG) workflows and complex data visualization when requesting front-end code for chatbots, document retrieval systems, or translating technical system architecture diagrams into functional UI components.
---

## ui-devkit

This skill is designed to aid software engineers and UI developers in creating modular and accessible React.js components. It focuses on supporting Retrieval-Augmented Generation (RAG) workflows and complex data visualization by providing structured code and usability insights.

### Workflow Steps

1. **Identify Requirements**: Determine the specific use case for the UI component (e.g., chatbot interface, document retrieval).
2. **Select Component Type**: Choose the type of React component needed (e.g., class-based, functional with hooks).
3. **Generate Code**: Use the skill to produce the React component code based on the requirements.
4. **Review Accessibility**: Ensure the generated component meets accessibility standards (e.g., ARIA roles, keyboard navigation).
5. **Implement State Management**: Outline state management strategies (e.g., using Context API, Redux).
6. **Usability Considerations**: Provide bullet points on how to enhance the user experience with the generated component.
7. **Test and Validate**: Test the generated components in real-world scenarios to validate functionality and performance.

### Output Format

The output will be in Markdown format containing structured React (JSX/TSX) code blocks. Each output will additionally include bullet points explaining key aspects of state management and usability considerations.

Example output format:

```jsx
import React from 'react';

const MyComponent = () => {
    // State management with hooks
    const [data, setData] = React.useState([]);

    return (
        <div>
            {/* Component UI goes here */}
        </div>
    );
};

// Usability Considerations:
// - Ensure the component is keyboard navigable
// - Provide clear error messages
```

### Examples

**Example 1: Chatbot Interface Component**

**Input:**
Generate a chatbot interface component.

**Output:**
```jsx
import React from 'react';

const ChatbotInterface = () => {
    const [messages, setMessages] = React.useState([]);

    const handleSendMessage = (message) => {
        // Logic to send a message
    };

    return (
        <div className="chatbot">
            <div className="messages">
                {messages.map((msg, index) => <div key={index}>{msg}</div>)}
            </div>
            <input type="text" onKeyPress={handleSendMessage} />
        </div>
    );
};

// Usability Considerations:
// - Ensure messages are displayed in chronological order
// - Provide a loading state while waiting for responses
```

**Example 2: Document Retrieval System Component**

**Input:**
Create a document retrieval system component.

**Output:**
```jsx
import React from 'react';

const DocumentFetcher = () => {
    const [documents, setDocuments] = React.useState([]);

    const fetchDocuments = async () => {
        // Fetch logic goes here
    };

    return (
        <div>
            <button onClick={fetchDocuments}>Fetch Documents</button>
            <ul>
                {documents.map((doc, index) => <li key={index}>{doc.title}</li>)}
            </ul>
        </div>
    );
};

// Usability Considerations:
// - Provide feedback during document retrieval
// - Ensure documents are easily selectable
```

### Anti-Patterns

- Do not generate components with hardcoded values that prevent reuse.
- Avoid components that do not adhere to accessibility guidelines.
- Do not neglect the performance implications of rendering large datasets without optimization.
- Avoid complex state management patterns that are not necessary for the component's functionality.

### Scope

This skill targets software engineers and UI developers building AI-integrated applications. Future enhancements may include support for additional frameworks, integration with design systems, and expanded accessibility features. Emphasis will be placed on keeping up with evolving UI usability standards and ensuring efficient rendering for dynamic data streams while maintaining easy integration into existing React architectures.