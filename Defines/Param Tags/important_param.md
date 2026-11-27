# Deprecated tag: `[important:param]`

**Status:** Deprecated and not included in the active ATL v0.1 specification.

The earlier description claimed that this tag could force an AI to preserve an exact constraint or prevent hallucination. That behavior is model-dependent and is not guaranteed by prompt syntax alone.

Use explicit plain-language instructions instead:

```text
This plan must contain exactly 7 groups, with exactly 6 students in each group.
```

For application-level workflows, validate critical constraints with code or automated tests rather than relying on `[important:param]`.

This file is retained only to explain the old tag's status and avoid silent removal.
