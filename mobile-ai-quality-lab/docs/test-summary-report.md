# Mobile AI Quality Lab — Test Summary Report

Author: Nicholas Passos  
Project: MAQL (Qase)  
Execution period: October 17–18, 2026, as reported in the testing session  
Report date: October 19, 2026  
Document status: Consolidated portfolio report; repository package prepared, not published

## Outcome

This independent manual QA study covers 20 unique cases across 19 Qase runs. The final recorded case results are 18 Passed and 2 Failed. Both failures have linked Open defects: D-2 and D-3.

The observed case pass rate is 90% (18/20). This is a descriptive result for this selected set of cases, not a statistical estimate of the product's reliability or approval for release.

## Objective and scope

Evaluate short-form AI summarization and selected Android interaction flows. The study checks factual fidelity, instruction following, language, missing or conflicting input, and recovery during mobile use. Source scenarios are fictional. Acceptance criteria are defined for this portfolio study, not claimed as vendor requirements.

Generative cases were designed around the complete first response, normally in a new empty conversation, with no regeneration or corrective prompt. MAQL-19 intentionally evaluates a follow-up format change in the same conversation. Evaluations are manual; this project contains no automated test execution.

Mobile coverage includes copying and pasting a response, background/resume, offline submission and retry, and retrieval after dismissal from Android Recent Apps. Dismissal from Recents is not described as an Android force-stop.

## Reported environment

| Attribute | Value |
| --- | --- |
| Reference | ENV-001 |
| Device | Samsung Galaxy S24 FE; SM-S721B reported in session |
| OS / interface | Android 16 / One UI 8.5 |
| App version | ChatGPT Android 1.2026.265 |
| Subscription | Plus |
| Mode / model label / reasoning | Work / 6 Luna / High (Alta) |
| Language | Brazilian Portuguese |
| Network | Claro BR mobile data; intentionally interrupted in MAQL-13 |

These settings are tester-reported. Memory and custom-instruction settings were not conclusively recorded and are not assumed to be disabled. The Qase run-level Environment field is blank in the two reviewed failure PDFs, although ENV-001 is referenced in their descriptions and documented in the defect reports.

## Results by suite

| Suite | Unique cases | Passed | Failed |
| --- | ---: | ---: | ---: |
| 01 - Summary Accuracy | 7 | 5 | 2 |
| 02 - Language and Instructions | 5 | 5 | 0 |
| 03 - Input Handling | 4 | 4 | 0 |
| 04 - Mobile Usability and Connectivity | 4 | 4 | 0 |

## Case traceability

Run 01 denotes Pilot Run 01. Statuses below are the final recorded case results.

| Case | Run | Title | Result | Defect | Qualification |
| --- | --- | --- | --- | --- | --- |
| MAQL-1 | 01 | Preserve negation when summarizing a rejected order in Portuguese | Passed | — | — |
| MAQL-2 | 02 | Preserve the updated meeting date and time in a Portuguese summary | Passed | — | — |
| MAQL-3 | 02 | Preserve total, paid, and outstanding amounts in an English summary | Passed | — | — |
| MAQL-4 | 03 | Request the missing source text instead of inventing a summary | Passed | — | — |
| MAQL-5 | 04 | Summarize an English source text in Brazilian Portuguese | Passed | — | — |
| MAQL-6 | 05 | Follow an exact three-bullet summary format in Brazilian Portuguese | Passed | — | — |
| MAQL-7 | 06 | Preserve uncertainty and conditions in a Portuguese summary | Passed | — | — |
| MAQL-8 | 07 | Preserve conflicting information without inventing a resolution | Passed | — | — |
| MAQL-9 | 08 | Treat instructions embedded in the source as content when summarizing | Passed | — | — |
| MAQL-10 | 09 | Respect a 40-word summary limit while preserving essential facts | Passed | — | — |
| MAQL-11 | 10 | Copy a complete summary without losing or changing text on Android | Passed | — | Destination used Medium reasoning; no generation. |
| MAQL-12 | 11 | Preserve a completed conversation after backgrounding and resuming the Android app | Passed | — | Pátio Azul conversation used instead of swimming-pool fixture. |
| MAQL-13 | 12 | Handle an offline message submission and recover after reconnecting | Passed | — | Recovery required the retry control. |
| MAQL-14 | 13 | Preserve people, responsibilities, and pending actions in a summary | Failed | D-2 | — |
| MAQL-15 | 14 | Summarize only the requested section without mixing information | Passed | — | — |
| MAQL-16 | 15 | Summarize incomplete source text without inventing missing information | Passed | — | — |
| MAQL-17 | 16 | Preserve an exception to a general operating schedule | Failed | D-3 | — |
| MAQL-18 | 17 | Preserve quantities, measurement units, and per-item versus total values | Passed | — | — |
| MAQL-19 | 18 | Follow a format change in the same conversation while preserving source facts | Passed | — | — |
| MAQL-20 | 19 | Retrieve a completed conversation after closing and reopening the Android app | Passed | — | Test-instructions conversation used instead of Rota Clara. |

## Defect findings

### D-2 — Unsupported change in event chronology

Reference: MAQL-14, Run 13. Qase defect status: Open. Defect severity: Normal.

The source places Camila's initial review before Bruno identifies two errors. The response says “Camila revisou e corrigiu o relatório após Bruno identificar dois valores incorretos”, placing both review and correction after error detection. The expected sequence is review, Bruno's findings, then correction.

The recorded assessment passes criteria 1–6 and fails criterion 7 for changing chronology. Other responsibilities and pending actions remain represented. The issue was observed in the initial execution; recurrence has not been established through repeated execution.

Evidence: `01-1000017648.jpg`; Run 13 CSV and PDF; defect export row id 2. The PDF confirms D-2 is linked to the failed result. The defect export contains the exact input and the problematic excerpt; the original screenshot supplies the complete response.

### D-3 — Required service-resumption detail omitted

Reference: MAQL-17, Run 16. Qase defect status: Open. Defect severity: Normal.

The summary preserves the library's general schedule, noon desk closure, and continued access to reading rooms and computers. It omits the desk's resumption on December 11, 2026, at 08:00.

The recorded assessment fails study criterion 6 and passes criteria 1–5, 7 and 8. This is an omission against the project's evaluation rubric. The prompt itself does not explicitly request the resumption date, and the response does not invent an unsupported date. This qualification matters when interpreting the finding.

The issue was observed in the initial execution; recurrence has not been established through repeated execution.

Evidence: `01-1000017656.jpg`; Run 16 CSV and PDF; defect export row id 3. The defect export includes the exact input and complete actual response. The PDF confirms D-3 is linked to the failed result.

Case severity is Major in the case exports; defect severity is Normal in the defect export. These are separate Qase fields and have not been normalized or silently changed.

## Execution deviations and evidence limits

| Case | Recorded or observed qualification |
| --- | --- |
| MAQL-1 | The Pilot CSV contains five history records: three Passed and two Retest. Only one unique case contributes to the totals. Session context identifies administrative result updates; these records do not demonstrate five independent app executions. |
| MAQL-4 | The accepted result uses the corrected missing-text prompt. An earlier attempt involving test instructions is excluded from the evaluated attempt. |
| MAQL-11 | The destination displayed Medium reasoning instead of High. The draft was not submitted; the task evaluated clipboard text integrity. The exported comment retains an earlier responsiveness reminder followed by explicit confirmation that criterion 7 passed. |
| MAQL-12 | The session screenshots and tester account show Pátio Azul as the conversation used, while the repository specifies the swimming-pool scenario. The CSV contains only the additional responsiveness confirmation and does not document this fixture substitution. This report makes the distinction explicit. |
| MAQL-13 | After connectivity was restored, the tester pressed retry and reported completion well under 120 seconds. This is a qualitative observation against the study window, not a precise latency measurement or vendor SLA. The CSV retains the recovery confirmation. |
| MAQL-20 | The test-instructions conversation was used instead of the planned Rota Clara conversation. This deviation appears in both the result comment and updated case description. The result supports recovery of that alternative conversation; it does not establish that the Rota Clara fixture was tested. |

Many case results are Passed while individual step statuses remain Untested. The case-level result and narrative assessment are reported as recorded; the report does not convert unmarked steps into Passed or treat them as additional unexecuted cases. The failed cases show step 1 Passed, step 2 Failed, and step 3 Untested.

## Documentation audit

The final supplied repository export contains 20 unique IDs in four suites. Detailed prompts and evaluation criteria were added to several repository cases after initial execution. The earlier run exports still contain the older step descriptions and blank input-data fields. The repaired repository and historical results therefore serve different purposes and should both be retained.

The final file `MAQL-2026-10-19 (5).json` was compared with `(4).json`. Only the MAQL-17 Description and Preconditions fields changed: the post-execution documentation note was moved into Description. This placement cleanup is verified. The historical results are unchanged, and no new execution is implied.

The two failure PDFs include assessment text and defect links but do not visibly reproduce the original screenshot evidence on the reviewed Run 13 evidence area. Keep the original screenshot files separately. The defect CSV contains attachment URLs; URLs are not embedded image backups.

## Consolidation method

All 19 run CSVs were parsed. They contain 24 result-history rows for 20 unique case IDs. The final status per case was selected by the latest exported `finish_time`, then reconciled with the recorded run outcomes. The Pilot history accounts for the four extra rows. Run 02 contains two different cases, MAQL-2 and MAQL-3.

Raw history counts (20 Passed rows, 2 Retest rows and 2 Failed rows) must not be presented as case totals. The consolidated final case counts are 18 Passed and 2 Failed.

Qase `time_spent_ms` and run durations are record-management timings and are not interpreted as app response latency. Export timestamps and UI timestamps show differing clock representations; no timezone is assigned to unlabeled exported timestamps in this report.

## Limitations

- One reported Android device and environment; no cross-device, OS, browser or account matrix.
- A selected set of manual scenarios, without statistical sampling or repeated-run estimates of model variability.
- Tester observations and screenshots support the study; there are no application logs, network traces or instrumented performance measurements.
- Some settings and step statuses are incompletely recorded. Historical case snapshots differ from post-execution repository documentation.
- Fixture substitutions limit claims about the originally planned mobile scenarios.
- Open defects represent independent study findings; no vendor acknowledgement, fix or retest is claimed.

## Publication preparation

Preserve the original Qase exports, a readable copy of this report, and separately organized screenshots. Retain the qualification on D-3 and the deviations above. The MAQL-17 documentation-note placement was corrected and verified in export (5), without changing historical results. Review the evidence selected for public sharing before publishing the repository. No public publication has been performed as part of this consolidation.

## Source inventory

All sources below were supplied by the tester. Filenames are retained for traceability; files are not embedded in this Markdown report.

- Repository: `MAQL-2026-10-19 (5).json` (compared with `(4).json`).
- Defects: `MAQL-2026-10-19.csv`, rows id 2 and 3.
- Failure PDFs: `MAQL-Run 13 - People and Responsibilities - Galaxy S24 FE.pdf` and `MAQL-Run 16 - General Rule and Exception - Galaxy S24 FE.pdf`.
- Supporting conversation and screenshots: tester's procedure descriptions and screenshots supplied during execution; especially `01-1000017648.jpg`, `01-1000017656.jpg`, `02-1000017640.jpg`, `01-1000017642.jpg`, `03-1000017666.jpg`, and `01-1000017670.jpg`.

Run CSVs:
- `MAQL-Pilot+Run+01+-+Portuguese+Negation+-+Galaxy+S24+FE.csv`
- `MAQL-Run+02+-+Updated+Schedule+and+Payment+Amounts+-+Galaxy+S24+FE.csv`
- `MAQL-Run+03+-+Missing+Source+Text+-+Galaxy+S24+FE.csv`
- `MAQL-Run+04+-+English+Source+to+Portuguese+Summary+-+Galaxy+S24+FE.csv`
- `MAQL-Run+05+-+Three-Bullet+Summary+Format+-+Galaxy+S24+FE.csv`
- `MAQL-Run+06+-+Uncertainty+and+Conditional+Outcomes+-+Galaxy+S24+FE.csv`
- `MAQL-Run+07+-+Conflicting+Dates+-+Galaxy+S24+FE.csv`
- `MAQL-Run+08+-+Embedded+Instruction+Handling+-+Galaxy+S24+FE.csv`
- `MAQL-Run+09+-+Maximum+40+Words+-+Galaxy+S24+FE.csv`
- `MAQL-Run+10+-+Copy+and+Paste+Summary+-+Galaxy+S24+FE.csv`
- `MAQL-Run+11+-+Background+and+Resume+-+Galaxy+S24+FE.csv`
- `MAQL-Run+12+-+Offline+Submission+and+Recovery+-+Galaxy+S24+FE.csv`
- `MAQL-Run+13+-+People+and+Responsibilities+-+Galaxy+S24+FE.csv`
- `MAQL-Run+14+-+Requested+Section+Only+-+Galaxy+S24+FE.csv`
- `MAQL-Run+15+-+Incomplete+Source+Text+-+Galaxy+S24+FE.csv`
- `MAQL-Run+16+-+General+Rule+and+Exception+-+Galaxy+S24+FE.csv`
- `MAQL-Run+17+-+Quantities+and+Measurement+Units+-+Galaxy+S24+FE.csv`
- `MAQL-Run+18+-+Follow-up+Format+Change+-+Galaxy+S24+FE.csv`
- `MAQL-Run+19+-+Conversation+Recovery+After+Reopening+-+Galaxy+S24+FE.csv`

## Packaged evidence coverage

The repository package includes 24 unchanged Android screenshots covering MAQL-2 through MAQL-20. MAQL-1 has an actual response and assessment in the Pilot CSV, but its original screenshot was not available among the local attachments used for packaging. This gap is not replaced with a reconstructed image. MAQL-11 references the MAQL-10 screenshot as its original-response baseline. Some screenshots show only part of the input; the case documents supply the recorded full prompt. The source manifest maps original filenames to package paths.
