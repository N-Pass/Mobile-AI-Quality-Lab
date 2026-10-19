# Mobile AI Quality Lab

**Manual Android QA and AI response evaluation by Nicholas Passos.**

This portfolio study evaluates summarization in the ChatGPT Android app and selected mobile interaction flows on a Samsung Galaxy S24 FE. It demonstrates test design, manual execution, evidence collection, defect reporting and result traceability using Qase.

| Recorded outcome | Count |
| --- | ---: |
| Unique test cases | 20 |
| Qase test runs | 19 |
| Passed cases | 18 |
| Failed cases | 2 |
| Open defects | 2 |

The observed pass rate is **90% for these selected cases**. This is an independent study using fictional source texts and project-defined criteria, not a general reliability score or vendor certification.

## Start here

- [Test summary report](docs/test-summary-report.md): findings, scope and limitations.
- [Case index](test-cases/README.md): 20 readable cases and the Qase repository export.
- [Result index](test-results/README.md): final case results and original run history exports.
- [Defect D-2](defects/D-2.md): a summary changes the order of completed actions.
- [Defect D-3](defects/D-3.md): a study-required reopening date and time are omitted.
- [Evidence index](evidence/README.md): screenshots mapped to cases and known gaps.

## Coverage

| Suite | Focus | Cases |
| --- | --- | ---: |
| Summary Accuracy | Negation, dates, payment amounts, uncertainty, people and responsibilities, service exceptions, measurement units | 7 |
| Language and Instructions | Brazilian Portuguese output, bullet format, word limit, selected section, follow-up format change | 5 |
| Input Handling | Missing text, conflicting dates, embedded instructions, truncated input | 4 |
| Mobile Usability and Connectivity | Clipboard integrity, background/resume, offline recovery, conversation retrieval after reopening | 4 |

## How the work was performed

The tester operated the app on a physical Android device, captured the responses and mobile behavior, assessed them against the study rubric, and recorded results and defects in Qase. AI assistance supported scenario drafting, evaluation discussion and documentation preparation. Generative cases normally use the first response in a new conversation; the follow-up case intentionally continues the same conversation.

The reported environment is Galaxy S24 FE, Android 16 / One UI 8.5, ChatGPT Android 1.2026.265, Plus, Work / 6 Luna / High, Brazilian Portuguese and Claro BR mobile data. See [environment and method](docs/environment-and-method.md) for qualifications.

## Findings and qualifications

**D-2** concerns chronology: Camila's initial review is described as occurring after Bruno found errors. **D-3** concerns omission of the desk's reopening schedule against a project criterion; the submitted prompt did not explicitly request that detail. Both are Open findings observed once, with no claim of established recurrence or vendor confirmation.

The mobile tests have documented deviations: a clipboard destination used Medium reasoning without generating a response; background/resume used Pátio Azul instead of the swimming-pool fixture; reopening used the test-instructions conversation instead of Rota Clara. Passed results apply to the observed attempts within these limits.

## How to read the records

The case repository was completed after execution in places. Run CSVs preserve the older case snapshots and result history. Individual steps often remain marked Untested even where the case result and narrative assessment are complete. These facts are disclosed in the report rather than silently rewritten.

The Pilot CSV contains five status-history rows for one case. Do not sum raw CSV rows as executed-case totals. There are 20 unique cases across the full set of exports.

The package contains 24 original Android screenshots. MAQL-1's original screenshot is not included; its response and assessment are retained in the Pilot export. Some screenshots do not show the complete input; the documented prompts are available separately.

## Repository contents

| Path | Purpose |
| --- | --- |
| `docs/` | Summary report, environment, method and source mapping |
| `test-cases/` | Readable case specifications and final Qase JSON |
| `test-results/` | 19 original CSV exports, result index and two failure PDFs |
| `defects/` | Two readable defect reports and original defect CSV |
| `evidence/` | Original screenshots and case mappings |

No code or automated-test installation is required. Markdown files can be read directly on GitHub. Original Qase exports retain their supplied values; source filenames and SHA-256 checksums are recorded in [the source manifest](docs/source-manifest.json). Qase attachment URLs remain in the original defect CSV, while the readable reports use local evidence links.

Study execution: October 17–18, 2026. Documentation and packaging: October 19, 2026. Public publication is a separate step.
