# Multi-Section Summarizer

This repository defines a modular system for summarizing the research paper *“Attention Is All You Need.”*

## Workflow
1. **System Prompt** — defines rules, inputs, outputs, and boundaries.
2. **Module 1: Intake & Setup** — normalize sections and detect missing/short ones.
3. **Module 2: Section Loop** — summarize each section.
4. **Module 3: Guardrails** — enforce constraints and prevent hallucinations.
5. **Module 4: Rendering & Refinement** — assemble final structured output.
6. **Module 5: Citation Extractor** — collect references.
7. **Module 6: Key Contribution Summarizer** — highlight main innovations.

## Outputs
- Paper Summary (≤ 400 words).
- Section-by-Section Table (≤ 100 words each).
- Expert Summary + Lay Summary.
- Mini-Glossary.
- Checks & Warnings.

## Constraints
- No hallucinations.
- Strict word limits.
- Neutral tone.
