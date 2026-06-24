---
name: ui-devkit
description: To design and generate modular, accessible React.js components specifically tailored for Retrieval-Augmented Generation (RAG) workflows and complex data visualization when requesting front-end code for chatbots, document retrieval systems, or translating technical system architecture diagrams into functional UI components.
---

## ui-devkit

The ui-devkit skill is designed to facilitate the creation of modular and accessible React.js components that are specifically suited for Retrieval-Augmented Generation (RAG) workflows and complex data visualizations. This skill is triggered when there is a need for front-end code to support chatbots, document retrieval systems, or when translating technical system architecture diagrams into functional UI components.

### Workflow Steps

1. **Identify the Component Type**: Determine the type of UI component needed (e.g., chat interface, data table, etc.).
2. **Define Data Requirements**: Specify the data structures and types that the component will handle.
3. **Generate Component Code**: Create the React component code in JSX/TSX format based on the defined requirements.
4. **Include State Management**: Incorporate state management considerations, using hooks or context as needed.
5. **Add Accessibility Features**: Ensure the component adheres to accessibility standards (e.g., ARIA attributes).
6. **Document Usability Considerations**: Provide bullet-point explanations for usability features and best practices.
7. **Return the Final Output**: Format the output in Markdown, ensuring code blocks and explanations are clear.

### Output Format

The output will be structured in Markdown format, containing:
- A code block with the generated React (JSX/TSX) code.
- Bullet points explaining state management and usability considerations.

Example Output:
```markdown
// React Component Code
const MyComponent = () => {
    const [data, setData] = useState([]);

    // Fetch data logic here

    return (
        <div aria-live="polite">
            {/* Render data */}
        </div>
    );
};

// Usability Considerations:
// - Implements loading state management for better user experience.
// - Ensures keyboard navigability for accessibility.
```

### Examples

**Example 1: Chatbot Interface Component**
- **Input**: Create a chat interface component for a chatbot.
- **Output**:
```markdown
// Chatbot Interface Component Code
const Chatbot = () => {
    const [messages, setMessages] = useState([]);

    const sendMessage = (msg) => {
        // Logic to send message
    };

    return (
        <div>
            {messages.map((msg, index) => (
                <div key={index}>{msg}</div>
            ))}
            {/* Input field and send button here */}
        </div>
    );
};

// Usability Considerations:
// - Allows users to send messages using the Enter key.
// - Displays typing indicators for an interactive experience.
```

**Example 2: Data Table Component**
- **Input**: Generate a data table for displaying document metadata.
- **Output**:
```markdown
// Data Table Component Code
const DataTable = ({ data }) => {
    return (
        <table>
            <thead>
                <tr>
                    <th>Title</th>
                    <th>Author</th>
                </tr>
            </thead>
            <tbody>
                {data.map((item) => (
                    <tr key={item.id}>
                        <td>{item.title}</td>
                        <td>{item.author}</td>
                    </tr>
                ))}
            </tbody>
        </table>
    );
};

// Usability Considerations:
// - Supports sorting by column headers.
// - Provides a summary of total items displayed.
```

### Anti-Patterns

- Avoid generating non-modular components that cannot be reused.
- Do not neglect accessibility features in the component design.
- Avoid hardcoding styles; use styled components or CSS modules instead.
- Do not produce overly complex components that are difficult to maintain.

### Scope

The scope of the ui-devkit skill is focused on providing reusable, accessible React components for software engineers and UI developers working on AI-integrated applications. Future enhancements may include:
- Adding support for additional front-end frameworks.
- Incorporating theming and styling options for better customization.
- Expanding the library of components to cover more use cases in AI and data visualization.