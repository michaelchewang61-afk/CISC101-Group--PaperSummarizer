# Module 3: Guardrails

## Inputs
- Section summaries.
- Flags from Intake & Setup.

## Outputs
- Validated summaries.
- Error/warning messages.

## Internal Processing Rules
- Reject hallucinated or invented content.
- Enforce word limits.
- Handle long papers by chunking text into manageable sections.
- Flag missing/empty sections and <50-word sections.

## Constraints
- Never invent results or citations.
- Always surface warnings in the final output.
