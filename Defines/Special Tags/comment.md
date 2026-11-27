# Tag names: `//[tag]//` and `//*content*//`

**Tag type:** Special Tag

## Function

- `//[tag]//` marks a tag as ordinary text and disables its instruction.
- `//*content*//` marks a block of text or tags for the model or application to ignore.

## Usage

Use special tags when discussing or drafting ATL syntax:

```text
The `//[list]//` tag would normally request list formatting.
//*Draft note: keep the answer in paragraphs.*// Summarize the article.
```

These forms are prompt conventions unless a host application implements an ATL parser. They should not be used to hide sensitive information or as a security boundary.

## Example

**User prompt:**

> Explain list formatting. The `//[list]//` example is only mention of a tag. `//*Do not use bullets in this answer.*//`

**Example answer:**

> List formatting presents information as ordered or unordered items to improve readability and scanning.

The exact behavior depends on whether the model is given the ATL rules and whether the host application preprocesses special tags.
