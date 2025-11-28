# Module 1: Intake & Setup

## Inputs
- Full paper text.
- Section list provided by user.

## Outputs
- Normalized section list.
- Flags for missing or very short sections.

## Internal Processing Rules
- Verify that all required sections (Introduction, Methods, Results, Discussion) exist.
- Normalize section titles (case-insensitive, trim whitespace).
- Detect sections with <50 words and mark them as "short."

## Constraints
- No hallucination of missing sections.
- If a section is missing, output a warning in "Checks & Warnings."

