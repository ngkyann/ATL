# AI Tag Language (ATL)

ATL v0.1 is a compact prompt-formatting convention for expressing output structure and task constraints. It is designed to make prompts easier to read and reuse, but it is not a standalone parser or runtime and does not guarantee identical behavior across AI models.

## Project structure

- `Versions/v0.x/ATL_v01.md` — Core specification.
- `Defines/RULES.md` — Syntax, chaining, and precedence rules.
- `Defines/Flag Tags/` — Output behavior tags.
- `Defines/Type Tags/` — Output format and structure tags.
- `Defines/Param Tags/` — Constraints and retrieval parameters.
- `Defines/Special Tags/` — Comments, skips, and optional tags.
- `Examples/` — Prompt and output examples.
- `Benchmark/` — Evaluation notes and test criteria.

## Quick start

Review `Versions/v0.x/ATL_v01.md`, copy the system instruction and active tag definitions that your application needs, and add it to the system or developer prompt. Keep the original task in plain language; ATL should supplement, not replace, clear instructions.

Example:

```text
[size:100words].[language:vi] Giải thích lực hấp dẫn.
```

The result is not guaranteed to be exactly 100 words. Applications should validate length, structure, and factual accuracy with tests.

## Scope

ATL can be used directly in prompts or implemented as an application-level convention. Internet search, file generation, diagram rendering, and other external actions require compatible tools; a tag alone cannot create those capabilities.

## Compatibility

Tag support varies by model and application. Test each tag in the target environment before using it in a workflow where formatting or factual correctness is critical.

## License

ATL is provided under the repository's custom license. Individual and non-commercial use is permitted subject to attribution. Commercial use or redistribution may require permission from the author; see `LICENSE`.
