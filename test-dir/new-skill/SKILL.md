---
name: ui-devkit
description: To design and generate modular, accessible React.js components specifically tailored for Retrieval-Augmented Generation (RAG) workflows and complex data visualization when requesting front-end code for chatbots, document retrieval systems, or translating technical system architecture diagrams into functional UI components.
---

## ui-devkit

This skill allows users to design and generate modular, accessible React.js components optimized for Retrieval-Augmented Generation (RAG) workflows and complex data visualizations. It is specifically useful for developers working on front-end code for chatbots, document retrieval systems, and translating technical system architecture diagrams into functional UI components.

### Workflow Steps

1. Identify the specific requirements for the UI component based on the intended use case (e.g., chatbot, document retrieval).
2. Define the data structure that the component will consume, ensuring it aligns with RAG workflows.
3. Generate the React component using JSX/TSX, adhering to modular design principles.
4. Include accessibility features to enhance usability for all users.
5. Document state management strategies and usability considerations in bullet points.
6. Review and test the component for performance and integration within existing architectures.

### Output Format

The output will be structured as follows:

- A code block containing the generated React (JSX/TSX) component.
- Bullet points detailing:
  - State management strategies
  - Usability considerations

Example output format:

```jsx
// React Component Code
const MyComponent = () => {
  // Component logic
  return <div>My Component</div>;
};

// State Management
- Use React hooks for state management.
- Ensure data fetching is efficient to minimize re-renders.

// Usability
- Ensure keyboard navigation is possible.
- Provide appropriate ARIA roles for accessibility.
```

### Examples

**Example 1:**

**Input:** Design a chatbot interface component.

**Output:**
```jsx
const ChatbotInterface = ({ messages, onSend }) => {
  // State to handle message input
  const [input, setInput] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    onSend(input);
    setInput('');
  };

  return (
    <div>
      <div className="messages">
        {messages.map((msg, index) => (
          <div key={index}>{msg}</div>
        ))}
      </div>
      <form onSubmit={handleSubmit}>
        <input
          type="text"
          value={input}
          onChange={(e) => setInput(e.target.value)}
          aria-label="Type your message"
        />
        <button type="submit">Send</button>
      </form>
    </div>
  );
};

// State Management
- Use useState for managing input state.
- Messages are passed as props for easy integration with parent component.

// Usability
- Provide real-time feedback on input.
- Ensure components are keyboard accessible.
```

**Example 2:**

**Input:** Create a data visualization component for document retrieval.

**Output:**
```jsx
const DocumentChart = ({ data }) => {
  // Logic to process and visualize data
  return <Chart data={data} />;
};

// State Management
- Use useEffect to fetch data when the component mounts.
- Handle loading and error states.

// Usability
- Provide tooltips for data points.
- Ensure the chart is responsive to screen size.
```

### Anti-Patterns

- Avoid hardcoding styles or component structures; favor props and stylesheets.
- Do not neglect accessibility features; ensure all components are usable by individuals with disabilities.
- Refrain from creating monolithic components; always strive for modularity and reusability.

### Scope

This skill is aimed at software engineers and UI developers focused on building AI-integrated applications. Future enhancements may include:

- Adding support for additional frameworks beyond React.js.
- Incorporating user feedback mechanisms for continuous improvement of generated components.
- Expanding the library of pre-built UI components for common use cases in AI applications.