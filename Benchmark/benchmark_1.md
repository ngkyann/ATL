# Benchmark Method: ATL Tag Compliance (v0.1)

This file describes how ATL prompts should be evaluated. It does not claim a benchmark result until tests, models, and results are recorded.

## Evaluation goals

Compare an ATL prompt with an equivalent natural-language prompt across the following metrics:

1. **Structural compliance** — valid JSON, CSV, Mermaid, or plain-text output where applicable.
2. **Instruction compliance** — presence or absence of explanations, lists, steps, and conversational filler.
3. **Factual correctness** — independent validation of task-specific claims.
4. **Input size** — prompt tokens before and after ATL conventions are added.
5. **Output size** — response tokens for equivalent tasks.
6. **Latency** — median and tail response time, if measured.

## Test conditions

Record the following for every benchmark run:

- Model name and version.
- Provider and API or application settings.
- System/developer prompt.
- Temperature and other relevant sampling settings.
- Number of repetitions.
- Search or retrieval availability.
- Test date and dataset version.

## Evaluation method

1. Create one prompt in natural language and one semantically equivalent ATL prompt.
2. Run both prompts repeatedly against the same model configuration.
3. Score each output with deterministic checks where possible.
4. Use human review for factual and semantic correctness.
5. Report failures individually rather than averaging away important edge cases.
6. Publish raw prompts and result samples when the license and privacy requirements permit.

## Example scorecard

| Metric                   | Natural-language prompt | ATL prompt | Notes                                     |
| ------------------------ | ----------------------: | ---------: | ----------------------------------------- |
| Valid JSON output        |                     N/A |        N/A | Replace with measured pass rate           |
| Direct-answer compliance |                     N/A |        N/A | Replace with measured pass rate           |
| Median token usage       |                     N/A |        N/A | Report input and output tokens separately |
| Median latency           |                     N/A |        N/A | Report environment and provider           |
| Factual correctness      |                     N/A |        N/A | Require independent verification          |

ATL may reduce repetition in prompts, but shorter input is not automatically cheaper or faster. Total cost and latency also depend on output length, provider overhead, model state, and retrieval tooling.
