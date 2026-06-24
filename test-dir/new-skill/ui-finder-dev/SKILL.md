---
name: ui-finder-dev
description: To design and generate modular, accessible React.js components specifically tailored for Retrieval-Augmented Generation (RAG) workflows and complex data visualization when requesting front-end code for chatbots, document retrieval systems, or translating technical system architecture diagrams into functional UI components.
---

## ui-finder-dev

This skill assists in designing and generating modular, accessible React.js components that are specifically tailored for Retrieval-Augmented Generation (RAG) workflows and complex data visualization. It is triggered when front-end code is requested for applications such as chatbots, document retrieval systems, or when translating technical system architecture diagrams into functional UI components.

### Workflow Steps

1. **Identify Requirements**: Gather specifications for the desired UI component based on user needs and system architecture.
2. **Design Component Structure**: Define the component hierarchy and modular approach for reusability.
3. **Generate Code**: Create the React.js (JSX/TSX) code for the component, ensuring adherence to modern UI usability principles.
4. **Explain Usability Considerations**: Provide bullet points detailing state management, accessibility, and integration tips.
5. **Output Code**: Format the generated code into markdown, ready for integration into existing React architectures.

### Output Format

The output will be structured as markdown containing:

- A code block with the generated React (JSX/TSX) component.
- A bullet-point list explaining key aspects such as state management, usability considerations, and integration advice.

### Examples

**Example 1:**

*Input:* Generate a React component for a chatbot message display.

*Output:*

```jsx
import React from 'react';

const ChatMessage = ({ message, sender }) => {
    return (
        <div className={`chat-message ${sender}`}>
            <p>{message}</p>
        </div>
    );
};

export default ChatMessage;
```

- **State Management**: Use local state to manage the visibility of the message.
- **Usability**: Ensure the component is responsive and accessible, using ARIA roles where appropriate.

**Example 2:**

*Input:* Create a UI component for displaying document retrieval results.

*Output:*

```jsx
import React from 'react';

const DocumentList = ({ documents }) => {
    return (
        <ul className="document-list">
            {documents.map(doc => (
                <li key={doc.id}>
                    <a href={doc.url}>{doc.title}</a>
                </li>
            ))}
        </ul>
    );
};

export default DocumentList;
```

- **State Management**: Consider using a context provider for managing document state across the application.
- **Usability**: Ensure links are clearly styled and provide visual feedback on hover.

### Anti-Patterns

- Avoid creating monolithic components that are hard to reuse or maintain.
- Do not overlook accessibility features such as ARIA roles and keyboard navigation.
- Refrain from using outdated practices that hinder performance, such as unnecessary re-renders.

### Scope

This skill is aimed at software engineers and UI developers who are building AI-integrated applications. Future enhancements could include support for additional UI frameworks, improved templates for diverse applications, and integration with design systems for better consistency.