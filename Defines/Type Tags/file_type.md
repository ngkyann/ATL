\# Tag name: \[file:type]

\*\*Tag type:\*\* Type Tag



\### 📝 Function

Instructs the AI to structure and format its entire output rawly inside a single code block matching the specified file extension or programming language syntax (e.g., `\[file:json]`, `\[file:csv]`, `\[file:html]`, `\[file:python]`). It allows users to easily copy, save, or directly export clean, syntactically correct code or data without markdown conversational text around it.



\### ⚙️ Usage

Replace `type` with your desired format or file extension. Use this tag when you need structured data payloads, source code scripts, or configuration files ready for deployment or software import.



\### 🎯 Example

\*\*User Prompt:\*\*

> `\[file:json]` Create a user profile template with name, age, and skills.



\*\*AI Output:\*\*

```json

{

&#x20; "user": {

&#x20;   "name": "John Doe",

&#x20;   "age": 30,

&#x20;   "skills": \["Python", "Prompt Engineering", "ATL"]

&#x20; }

}

```



