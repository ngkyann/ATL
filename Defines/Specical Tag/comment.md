# Tag name: //[tag]// & //*content*//
**Tag type:** Special Tag

### 📝 Function
Provides two distinct compiler-style commenting behaviors to control prompt execution:
1. `//[tag]//` (Tag Skip): Temporarily disables or skips the execution of a specific standalone ATL tag, treating it as dead text.
2. `//*content*//` (Block Comment): Completely hides and comments out any written content, text, or multiple tags wrapped inside. The AI will completely ignore this block during its generation process.

### ⚙️ Usage
- Use `//[tag]//` when you want to mention a tag as an inline text example without triggering its behavior.
- Use `//*your note or tags*//` when you want to leave developer notes, metadata, or draft sections that the AI engine must not process or respond to.

### 🎯 Example
**User Prompt:**
> What is the purpose of the list format? For example, your system supports the //[list]// tag. //*Developer note: This is an overview question, do not output a structured list right now.*//

**AI Output:**
The purpose of a list format is to present information clearly and sequentially using bullet points or numbers, making it highly scannable for readers. *(Note: The AI successfully skipped the execution of [list] and completely ignored the hidden developer note).*
