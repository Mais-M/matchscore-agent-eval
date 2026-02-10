# MatchScore — LLM Agent for JD ↔ CV Matching (Custom GPT)

**Live Agent:** https://chatgpt.com/g/g-6973b0c982ec8191a540f05cd1d20737-matchscore

## Overview
MatchScore is an LLM-based agent that compares a Job Description to a CV and produces:
- a structured match score
- strengths & gaps
- actionable recommendations (what to improve / highlight)

This repo documents the agent specification, guardrails, and an evaluation framework.

## Why this project
The focus is **reliability + safety + evaluation** for AI agents:
- structured outputs (consistent format)
- reduced hallucinations (evidence-first approach, where applicable)
- bias-aware behavior (avoid protected attributes, where applicable)
- scenario-based testing and failure-mode analysis

## How to use (high level)
1. Provide a Job Description
2. Provide a CV (use anonymized/synthetic CVs only)
3. Review the structured output: score + gaps + recommendations

## Repo Structure
- `agent_spec/` — agent instructions, scoring rubric, output schema
- `eval/` — test cases + results template
- `examples/` — anonymized sample inputs/outputs
- `docs/` — threat model and limitations

## Evaluation (what we test)
See `eval/test_cases.md`. Key dimensions:
- **Consistency:** same input → stable score/output
- **Must-have vs Nice-to-have:** correct weighting
- **Hallucination control:** claims supported by input (where applicable)
- **Safety & fairness:** avoid sensitive/protected attributes
- **Prompt injection resistance:** ignore malicious instructions embedded in inputs

## Privacy / Data Handling
Do **not** upload real personal data (real CVs, emails, phone numbers, IDs).
Use anonymized or synthetic examples only.

## Notes / Limitations
See `docs/limitations.md` for known limitations and future improvements.
