
# Example: Data Extraction & Formatting
**Tags Used:** `[result]`, `[file:json]`, `[search]`

---

## Scenario
You want to get the financial population statistics of Vietnam in 2025 to paste into your database.

### ❌ Option 1: Before ATL (Standard Natural Language)
**User Prompt:**
> "Can you search the web and find the official population of Vietnam in 2025? Please give me just the numbers and structure it as a clean JSON object with keys like 'country', 'year', and 'population'. Do not write any greetings or explanations because I want to copy the raw data directly."

**The Problem:** 
AI often still outputs conversational fluff like *"Sure, here is the JSON data you requested..."* or fails to restrict the output strictly to a copyable raw block, forcing you to manually edit the text.

---

###  Option 2: After ATL (Using Prompt Engine Framework)
**User Prompt:**
> [search].[result].[file:json] Vietnam population 2025

**AI Output:**
```json
{
  "country": "Vietnam",
  "year": 2025,
  "population": 101400000
}
```

**Why it works:**
The chained pipeline `[search].[result].[file:json]` forces the AI engine to execute a live web search first, strip away 100% of introductory text, and wrap the data exactly inside a raw JSON block in one single turn.
