# Tag name: `?[tag]?`

**Tag type:** Special Tag

## Function

Marks an ATL tag or directive as optional. The model or application may decide whether the tag is useful for the current task.

## Usage

Wrap a standard tag with question marks on both sides:

```text
?[search:name]?
?[diagram:mermaid]?
```

Optional syntax is a recommendation, not a way to guarantee tool behavior or hide information.

## Example

**User prompt:**

> Who won the Nobel Prize in Physics in 1921? If available, `?[search:name]?` may verify the answer against an authoritative source.

**Example answer:**

> Albert Einstein received the 1921 Nobel Prize in Physics for his explanation of the photoelectric effect. The model may answer from existing knowledge if retrieval is unavailable.

Use `[search:name]` without the optional wrapper when retrieval is mandatory for the workflow.
