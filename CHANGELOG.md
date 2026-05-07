# Changelog — Quantum Physics Guide

All notable changes to the system prompt are documented here.

## [v2.0.4] - 06/05/2026

### Why This Version?
- **The Trigger:** Shifted inference parameters from **Temperature 0.8 / Top-P 0.95** (v2.0.3) to **Temperature 0.3 / Top-P 0.90** to test if lower randomness would force stricter adherence to word limits.
- **The Discovery:** Lowering parameters made the model *more* rigid but *more* verbose (it became "polite" and added fluff). The original "≤ 60 words" rule was insufficient.
- **The Solution:** Abandoned abstract word-count limits. Instead, implemented **"Exactly 2 sentences"** constraints + **Few-Shot Examples** (Bad vs. Good) to enforce brevity *without* breaking safety logic.

### Fixed
- **Safety Vulnerability (DAN/Meta Injection):** Resolved critical failure where the model adopted "DAN" persona or revealed internal rules.
  - *Fix:* Reordered `HARD SAFETY` to the very top and added explicit "No Persona" constraints.
- **Conciseness Failure:** Resolved the issue where the model exceeded word limits despite lower temperature.
  - *Fix:* Replaced the ineffective "≤ 60 words" rule (from v2.0.3) with **"Exactly 2 sentences"** + **Few-Shot Examples**.

### Changed
- **Inference Strategy:** Confirmed that **Temperature 0.3** is optimal for *safety*, but **Prompt Engineering** (examples/structure) is required for *brevity*.
- **Output Format:** Enforced strict `[Definition] + [Analogy]` structure to ensure consistency for beginners.

### Removed
- **Abstract Word Count Limits:** Removed "Keep each reply STRICTLY ≤ 60 words" (from v2.0.3) as it was unreliable for 8B models.

### Added
- **Few-Shot Examples:** Added "Bad" vs. "Good" examples in `TEACHING STYLE` to explicitly demonstrate the target length and tone.

---

## [v2.0.3] - 26/03/2026
- Initial release of constrained prompt.
- Focused on safety and beginner-friendly tone.
- *Constraints:* Used "STRICTLY ≤ 60 words (2 short paragraphs MAX)".
- *Known Issue:* Model consistently exceeded word limits (verbose outputs) despite safety rules.
