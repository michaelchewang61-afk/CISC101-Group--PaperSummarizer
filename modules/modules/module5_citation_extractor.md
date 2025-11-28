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
