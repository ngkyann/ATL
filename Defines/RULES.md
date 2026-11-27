# ATL Syntax and Execution Rules (v0.1)

This document defines the syntax and recommended interpretation rules for ATL prompts.

## 1. Tag types

- **Flag tag**: `[tag]` — requests an output behavior, such as `[list]`, `[result]`, or `[step]`.
- **Type tag**: `[key:type]` — requests an output format or structure, such as `[file:json]` or `[diagram:mermaid]`.
- **Parameter tag**: `[key:param]` — adds a constraint or parameter, such as `[size:100words]` or `[role:coder]`.
- **Special tag**: `//[tag]//`, `//*content*//`, or `?[tag]?` — changes how surrounding ATL syntax is interpreted.

## 2. Precedence

1. Resolve special tags first.
2. Interpret standard tags as a combined set of instructions.
3. If tags conflict, prefer the most explicit instruction, or the tag closest to the end of the prompt.
4. Always preserve factual accuracy, safety rules, and the user's primary question.

ATL does not force a model to implement these priorities unless the specification has been included in the prompt context or enforced by an application.

## 3. Chaining

The dot operator (`.`) groups multiple directives:

```text
[tag1].[tag2].[tag3]
```

A chain is a prompt convention, not a claim that a real processor exists. Its left-to-right order describes the author's intent; application implementations may need to parse the tags and apply each constraint explicitly.

### Examples

- `[result].[list]` — return the direct answer, formatted as a list.
- `[step].[file:python]` — present a procedural artifact in Python, with each stage identifiable.
- `[size:100words].[language:vi]` — aim for a 100-word response in Vietnamese.

## 4. Conflicting tags

Examples of conflicting combinations include:

- `[result]` and `[explain]`
- `[text]` and `[file:json]`
- `[list]` and `[file:python]`

Authors should avoid such combinations or document which tag is intended to take precedence. A target application may reject or normalize conflicts instead of guessing.

## 5. Unsupported tags

An unsupported tag should not be invented into a new capability. For example:

- `[search:param]` only requests retrieval if search tooling is available.
- `[file:type]` may only be used for formats supported by the target application.
- `[language:type]` is a language instruction, not a translation service guarantee.

The recommended fallback is to ignore unsupported tags and continue from the plain-language task.

## 6. Special syntax

- `//[tag]//` — treat the tag as ordinary text and disable it.
- `//*content*//` — ignore the enclosed text.
- `?[tag]?` — treat the tag as optional rather than mandatory.

Special syntax is evaluated by the prompt instructions or application parser. It should not be relied on for hiding sensitive information.
