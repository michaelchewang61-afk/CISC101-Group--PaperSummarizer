# Module 2: Section Loop

**Change Log (Set 3):**  
- Added `summary_level` ("short", "detailed").  
- Added conditional behavior for different summary modes.

## Inputs
- Normalized section list  
- Section text chunks  
- `summary_level` ("short" / "detailed")

## Outputs
- Per-section summary (format depends on summary_level)

## Rules
### If summary_level = "short":
- Produce 1–2 sentence compact summary.

### If summary_level = "detailed":

## Constraints
- No hallucinations  
- Maintain neutral tone
- Max 100 words per section.  
