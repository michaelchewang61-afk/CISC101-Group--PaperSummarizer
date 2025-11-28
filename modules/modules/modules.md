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


# Module 4: Rendering & Refinement

## Inputs
- Validated section summaries.
- Overall paper text.

## Outputs
- Final structured output:
  - Paper Summary
  - Section-by-Section Table
  - Expert Summary
  - Lay Summary
  - Mini-Glossary
  - Checks & Warnings

## Internal Processing Rules
- Assemble summaries into consistent Markdown format.
- Create Expert Summary (technical, precise).
- Create Lay Summary (simplified, accessible).
- Generate Mini-Glossary with 5–10 key terms.
- Insert warnings at the end.

## Constraints
- Maintain formatting consistency.
- Respect word limits.
- No hallucinations.


# Module 5: Citation Extractor

## Inputs
- Full paper text.

## Outputs
- List of important references cited in the paper.

## Internal Processing Rules
- Scan text for citation markers (e.g., [Vaswani et al., 2017]).
- Extract references without altering or inventing them.
- Clean duplicates and normalize formatting.

## Constraints
- Do not fabricate citations.
- If no citations are found, output "No citations detected."


# Module 6: Key Contribution Summarizer

## Inputs
- Full paper text.

## Outputs
- Concise summary of main innovations and contributions.

## Internal Processing Rules
- Identify explicit claims of novelty (e.g., "We propose the Transformer…").
- Summarize contributions in ≤ 150 words.
- Maintain neutral tone.

## Constraints
- No invented contributions.
- Only summarize what is explicitly stated in the paper.



