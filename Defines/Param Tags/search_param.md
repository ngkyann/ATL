\# Tag name: \[search:param]

\*\*Tag type:\*\* Param Tag

\### 📝 Function

Refines the AI's real-time web search behavior by passing specific filtering parameters. The syntax supports keys like `\[search:link]` to restrict searching to a specific URL/domain, or `\[search:name]` to focus the search strictly on a specific entity, brand, or individual's official online presence.

Requests that available web-search or retrieval tooling prioritize a domain or entity. Use `[search:link]` for a specific URL or domain and `[search:name]` for a person, organization, brand, or named subject.

The tag does not enable internet access or guarantee that a source will be found. Search must be provided by the host application, and the returned information should be checked against authoritative sources.

\### ⚙️ Usage

Use `\[search:link]` when you want to audit or scrape data from a specific website. Use `\[search:name]` when you want to isolate information regarding a precise entity and avoid mixed search noise from generic terms.

\### 🎯 Example

\*\*User Prompt:\*\*

> `\[search:wikipedia.org]` Find the discovery date of penicillin.

\*\*AI Output:\*\*

According to official records indexed on wikipedia.org, penicillin was discovered by Alexander Fleming in September 1928.
