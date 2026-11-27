\# Tag name: \[size:param]

\*\*Tag type:\*\* Param Tag

\### 📝 Function

Requests a target length or volume based on the specified value and unit (e.g., `[size:100words]`, `[size:3paragraphs]`, or `[size:500characters]`). The model should aim to preserve the core message while staying near the requested limit; applications requiring exact limits should measure and validate the result.

\### ⚙️ Usage

Append the desired numerical limit along with its corresponding unit (words, paragraphs, lines, characters) directly inside the tag parameters. Use this tag when you need to fit text into strict layouts, character-limited fields, or quick-read formats.

\### 🎯 Example

\*\*User Prompt:\*\*

> `\[size:50words]` Explain the concept of gravity.

\*\*AI Output:\*\*

Gravity is an invisible force that pulls objects toward each other. It is what keeps your feet on the ground and causes apples to fall from trees. The more mass an object has, the stronger its gravitational pull, which is why the Earth keeps the Moon in orbit.
