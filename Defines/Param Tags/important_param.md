\# Tag name: \[important:param]

\*\*Tag type:\*\* Param Tag



\### 📝 Function

Forces the AI to lock its attention on a specific, critical piece of data or constraint passed within the parameter (e.g., `\[important:35\_students]`, `\[important:budget\_$500]`, `\[important:strict\_deadline\_friday]`). It dramatically increases the attention weight of this parameter, preventing the AI from forgetting it, hallucinating numbers, or diluting its significance during long context processing.



\### ⚙️ Usage

Insert the critical variable, condition, or fixed data directly inside the tag parameter. Use this tag when generating schedules, financial reports, or logistical plans where a single accurate number or condition determines the validity of the entire response.



\### 🎯 Example

\*\*User Prompt:\*\*

> `\[important:students]` Create a group activity plan where each group must have exactly 6 members.



\*\*AI Output:\*\*

Based on the absolute constraint of 42 students, here is your balanced group activity layout:

\- Total Groups: Exactly 7 groups.

\- Group Distribution: 6 members per group (7 x 6 = 42).

\- Allocation Plan: \[Detailed sequential team assignments follow...]



