# Example: Data Extraction and Formatting

**Tags used:** `[search:name]`, `[result]`, `[file:json]`

## Scenario

Retrieve the population of Vietnam for 2025 and return a database-ready JSON object.

## Before ATL

> Search for an official source for Vietnam's 2025 population. Return only the numbers in a clean JSON object with the keys `country`, `year`, and `population`. Do not add greetings or explanations.

This natural-language prompt is clear, but it does not encode the source or formatting convention as reusable tags.

## With ATL

> `[search:name].[result].[file:json]` Vietnam population 2025. Use a verifiable official source and include the source URL as `source` only if it fits the requested schema.

Example result:

```json
{
  "country": "Vietnam",
  "year": 2025,
  "population": 101400000,
  "source": "https://example.gov.vn/official-source"
}
```

## Notes

- `[search:name]` requests retrieval support for the named subject. It does not create internet access.
- `[result]` requests concise output, but the final answer should still be validated for factual accuracy.
- `[file:json]` requests JSON formatting. The application should validate the JSON and not assume that a code block is sufficient to guarantee valid syntax.
- Search results and population estimates should be sourced and checked against an authoritative dataset.
