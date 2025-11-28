# Module 3: Guardrails

**Change Log (Set 3):**  
- Added `evidence_mode = "strict"`  
- Added standardized warning messages for missing/empty/very-short sections.

## Inputs
- Section summaries  
- Flags from Module 1  
- `evidence_mode` ("strict")

## Outputs
- Validated summaries  
- Warnings list

### Evidence Mode (“strict”)
- Only include claims/results explicitly in text.  
- If information is insufficient, output:  
  “The source text does not provide enough detail to summarize this section in strict evidence mode.”

### Standard Warning Messages
- Missing section → “Section skipped: no source text was provided.”  
- Empty section → “Section skipped: source text is empty.”  
- Very short (<50 words) → add: “Warning: section text is very short; summary may be incomplete.”

## Constraints
- No invented citations/results  

