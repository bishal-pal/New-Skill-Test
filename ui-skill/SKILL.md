---
name: ui-devkit
description: To design and generate modular, accessible React.js components specifically tailored for Retrieval-Augmented Generation (RAG) workflows and complex data visualization when requesting front-end code for chatbots, document retrieval systems, or translating technical system architecture diagrams into functional UI components.
---

## ui-devkit

The ui-devkit skill is designed to facilitate the creation of modular, accessible React.js components that are optimized for use in Retrieval-Augmented Generation (RAG) workflows and for complex data visualization tasks. This skill aids software engineers and UI developers in generating front-end code that enhances user interaction with AI-integrated applications.

### Workflow Steps

1. **Define Requirements**: Specify the type of component required (e.g., chatbot interface, document retrieval UI, etc.).
2. **Input Context**: Provide any relevant context regarding data sources or existing UI elements.
3. **Component Design**: Select the component style (e.g., dropdown, modal, table) based on the use case.
4. **Generate Code**: The skill generates structured JSX/TSX code for the specified component.
5. **State Management**: Include considerations for managing component state and integration into the overall application.
6. **Usability Review**: Ensure the generated component adheres to modern UI usability principles.
7. **Integration Guidance**: Offer tips for integrating the generated code into existing React architectures.

### Output Format

The output will be a Markdown document containing:

- Structured React (JSX/TSX) code blocks.
- Bullet points explaining key aspects such as state management and usability considerations.

Example of output format:

```jsx
// Example Component
const MyComponent = () => {
  const [data, setData] = useState([]);

  useEffect(() => {
    // Fetch data logic
  }, []);

  return (
    <div>
      {/* Render logic */}
    </div>
  );
};

// Usability Considerations
- Ensure accessibility standards are met (e.g., ARIA roles).
- Optimize rendering for performance with memoization where applicable.
```

### Examples

**Example 1: Chatbot Interface**

**Input:**
- Component Type: Chatbot Interface
- Context: Needs to display messages dynamically

**Output:**
```jsx
const Chatbot = () => {
  const [messages, setMessages] = useState([]);

  return (
    <div className="chatbot">
      {messages.map((msg, index) => (
        <div key={index} className="message">{msg}</div>
      ))}
    </div>
  );
};

// Usability Considerations
- Implement keyboard navigation for accessibility.
- Ensure messages update without full re-renders.
```

**Example 2: Document Retrieval UI**

**Input:**
- Component Type: Document Retrieval UI
- Context: Requires search functionality with results display

**Output:**
```jsx
const DocumentSearch = () => {
  const [query, setQuery] = useState('');
  const [results, setResults] = useState([]);

  const handleSearch = () => {
    // Search logic
  };

  return (
    <div>
      <input value={query} onChange={(e) => setQuery(e.target.value)} />
      <button onClick={handleSearch}>Search</button>
      <ul>
        {results.map((doc) => (
          <li key={doc.id}>{doc.title}</li>
        ))}
      </ul>
    </div>
  );
};

// Usability Considerations
- Provide loading indicators during data fetch.
- Ensure results are filterable and sortable.
```

### Anti-Patterns

- Generating monolithic components that do not adhere to modular design principles.
- Overcomplicating state management without clear documentation.
- Ignoring accessibility standards and usability guidelines.
- Failing to consider performance optimizations for dynamic data.

### Scope

The scope of the ui-devkit includes:

- Current focus on generating React components for AI-integrated applications.
- Future enhancements may include the ability to generate full application layouts and integration with popular UI libraries.
- Target audience includes software engineers and UI developers seeking efficient and effective solutions for modern application challenges.
- Extra content will encompass best practices in UI design and performance optimization techniques for dynamic data visualization.