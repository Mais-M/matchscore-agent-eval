# Limitations — MatchScore

## Known limitations
- **Input quality dependency:** Results depend on JD/CV clarity and completeness.
- **Evidence matching is imperfect:** The agent may miss evidence if phrasing differs or the CV is unstructured.
- **Scoring subjectivity:** Even with a rubric, scoring may vary across runs or model versions.
- **Domain specificity:** Performance may drop for highly specialized roles without explicit JD requirements.
- **No guarantee of fairness:** Guardrails reduce risk, but do not fully eliminate bias without deeper evaluations.

## Future improvements
- Add a richer evaluation set across industries and seniority levels.
- Automate evaluation runs and compute consistency metrics.
- Add stronger defenses against indirect prompt injection (e.g., from retrieved documents).
- Explore lightweight signals for suspicious behavior (e.g., variance, refusal patterns).
