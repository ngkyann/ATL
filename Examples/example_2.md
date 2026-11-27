# Example: Mathematical Proof and Logic Reasoning

**Tags used:** `[step]`, `[language:en]`

## Scenario

Provide a clear proof that the square root of 2 is irrational without skipping logical steps.

## Prompt

> `[step].[language:en]` Prove that √2 is irrational. State each key assumption and conclusion.

## Example output

1. Assume, for contradiction, that √2 is rational.
2. Write √2 as a fraction a/b in lowest terms, where a and b are integers and b ≠ 0.
3. Square both sides: 2 = a²/b², so 2b² = a².
4. Since a² is even, a is even. Write a = 2k.
5. Substitute: 2b² = (2k)² = 4k², therefore b² = 2k².
6. Since b² is even, b is even.
7. Both a and b are even, contradicting the assumption that a/b is in lowest terms.
8. Therefore, √2 cannot be rational and is irrational.

## Notes

- `[step]` requests a sequential explanation.
- `[language:en]` requests English output.
- ATL does not expose or guarantee access to hidden model reasoning. The output should contain only the user-requested proof and intermediate conclusions.
