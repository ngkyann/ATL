\# Tag name: \[diagram:type]

\*\*Tag type:\*\* Type Tag



\### 📝 Function

Instructs the AI to render or output its entire response as a visual diagram, flowchart, or architectural map using a specific text-based syntax (e.g., `\[diagram:mermaid]`, `\[diagram:plantuml]`, `\[diagram:ascii]`). This forces the AI to visually structure workflows, relational data, or system components rather than using standard paragraphs.



\### ⚙️ Usage

Replace `type` with your preferred diagramming format or tool syntax. Use this tag when you need to visualize system architectures, database schemas, business workflows, or organizational trees.



\### 🎯 Example

\*\*User Prompt:\*\*

> `\[diagram:mermaid]` Show the flow of a user logging into a website.



\*\*AI Output:\*\*

```mermaid

graph TD

&#x20;   A\[User Enters Credentials] --> B{Valid?}

&#x20;   B -- Yes --> C\[Access Granted / Dashboard]

&#x20;   B -- No --> D\[Show Error Message]

&#x20;   D --> A

```



