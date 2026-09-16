\# Tag name: ?\[tag]?

\*\*Tag type:\*\* Special Tag



\### 📝 Function

Marks an embedded ATL tag or a specific directive as entirely optional. It grants the AI full autonomy to evaluate the context and decide whether executing the enclosed tag is necessary. If the AI determines that its internal capabilities or static knowledge are sufficient, it can gracefully bypass the directive.



\### ⚙️ Usage

Wrap any standard ATL tag with question marks `?` on both sides (e.g., `?\[search]?`, `?\[table]?`). Use this when you want to suggest a tool or formatting style without strictly forcing the model to allocate resources or tokens for it if it isn't required.



\### 🎯 Example

\*\*User Prompt:\*\*

> Who won the Nobel Prize in Physics in 1921? For this query, ?\[search]? is optional.



\*\*AI Output:\*\*

Albert Einstein won the 1921 Nobel Prize in Physics for his services to Theoretical Physics, and especially for his discovery of the law of the photoelectric effect. \*(Note: The AI successfully bypassed the live search directive because this historical fact is permanently verified within its static core dataset).\*



