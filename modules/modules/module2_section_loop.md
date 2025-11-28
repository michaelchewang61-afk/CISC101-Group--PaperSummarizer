# Module 2: Section Loop

## Inputs
- Normalized section list.
- Section text chunks.

## Outputs
- Concise summary (≤ 100 words) for each section.

## Internal Processing Rules
- Summarize each section individually.
- Apply strict word limit.
- Maintain neutral tone.
- Ensure summaries are faithful to the text.

## Constraints
- No invented content.
- If section text is empty, output "No content available" and flag in "Checks & Warnings."
