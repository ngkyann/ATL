# AI Tag Language (ATL) — Specification v0.1

# Creator: ngkyann | License: see the repository `LICENSE`

## Purpose

ATL is a prompt-formatting convention for describing the desired output structure and constraints to an AI model. ATL tags are interpreted by the AI or by an application using an ATL prompt adapter; ATL does not include a built-in parser, runtime, or guaranteed model behavior.

## System instruction

> Parse ATL tags in a prompt according to the rules below. Apply supported tags to the requested task, ignore unsupported tags when possible, and do not print the tags unless the user asks for them.

## Syntax

- Flag tag: `[tag]`
- Parameter tag: `[key:value]`
- Special tag: `//[tag]//` or `?[tag]?`
- Chained tags: `[tag1].[tag2].[tag3]`

Use tags only for directives that the target model and application support. Plain text should remain the primary description of the task and factual requirements.

## Precedence

1. Block comments and tag skips are resolved first.
2. Explicit conflicts should be resolved by the tag closest to the end of the prompt.
3. Output constraints should not override the user's factual question or required safety and correctness constraints.

This precedence is a convention for prompt authors and applications. It is not an execution guarantee for a model that has not been given the corresponding instructions.

## Chaining

Dots separate related directives. The order is primarily useful for describing the intended sequence, but ATL does not require or provide a real processing pipeline.

Examples:

- `[result].[list]`: return only the direct answer and present it as a list.
- `[step].[file:python]`: organize instructions as steps, but return a Python code artifact where that is the intended output.

Avoid combinations with contradictory goals, such as `[result]` with `[explain]` or `[text]` with `[file:json]`.

## Active tags

### Flag tags

- `[list]`: Present the response as a bulleted or numbered list.
- `[result]`: Focus on the direct answer and omit unnecessary discussion.
- `[explain]`: Explain concepts and reasoning.
- `[step]`: Present the work as an ordered sequence.
- `[text]`: Avoid Markdown and code-block formatting.
- `[example]`: Use practical examples to explain the subject.

### Type tags

- `[file:type]`: Request a code block or text artifact for a format such as JSON, CSV, HTML, or Python.
- `[diagram:type]`: Request a diagram in Mermaid, PlantUML, ASCII, or another supported syntax.
- `[language:type]`: Request output in the specified language or locale.

### Parameter tags

- `[size:param]`: Request a word, paragraph, line, or character limit.
- `[role:param]`: Request a specific perspective or professional tone.
- `[search:link]` or `[search:name]`: Request that available search or retrieval tooling prioritize a domain or named entity.

Search tags do not create internet access. The host application must provide retrieval tooling and the model must be able to use it.

### Special tags

- `//[tag]//`: Treat the enclosed tag as ordinary text and do not execute it.
- `//*content*//`: Ignore the enclosed text and tags.
- `?[tag]?`: Describe the tag as optional; do not force an unavailable action.

## Conflict and fallback behavior

- A tag that conflicts with another tag should be handled explicitly by the user or application.
- Unsupported tags should remain inert rather than being invented by the model.
- Safety, legal, factual, and system constraints take priority over formatting tags.
- Output accuracy is not guaranteed solely because a tag was present.

## Compatibility

ATL behavior is model-dependent. Validate important prompts with representative tests across target models and keep a natural-language version as the fallback.
