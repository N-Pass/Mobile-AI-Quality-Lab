# MAQL-11: Copy a complete summary without losing or changing text on Android

Suite: 04 - Mobile Usability and Connectivity

Final recorded result: **Passed** — [Run 10](../test-results/run-10.csv)

## Description

Verify that copying an assistant response and pasting it into a message draft preserves the complete text, including accented characters, numbers, and punctuation.

Documentation update after the initial execution: replaced the duplicated action in the test data with the original response used as the clipboard comparison baseline. This update is not a new test execution.

## Preconditions

ENV-001 is available. Verify and record the actual environment and any deviations.

The conversation containing the completed swimming pool summary is available. The response must match the baseline text in the test data.

No response generation is in progress.

## Postconditions

Preserve screenshots of the original response and pasted draft. Discard the draft after recording the result. Do not send the pasted text.

## Step 1

Action:

Open the conversation containing the swimming pool summary and compare the original response with the baseline text.

Input / baseline:

```text
A piscina do clube Jardim do Lago ficará fechada em 25 de novembro de 2026, das 8h às 12h, para manutenção; a academia continuará funcionando normalmente.
```

Expected result:

The complete original response is available and matches the baseline text.

## Step 2

Action:

Tap the copy icon directly below the assistant response.

Expected result:

The copy action is available and can be activated without an error.

## Step 3

Action:

Open a new conversation, press and hold the message input field, and select Paste. Do not send the message.

Expected result:

The copied response appears in the message input field as an editable draft.

## Step 4

Action:

Compare the complete pasted draft with the baseline text and capture evidence.

Expected result:

1. The entire response is pasted, from the initial "A piscina" to the final "normalmente."
2. No words are missing, duplicated, reordered, or added.
3. Accented characters are preserved, including "ficará", "às", "manutenção" and "continuará".
4. The date and times are preserved exactly as displayed in the original response.
5. Punctuation is preserved, including commas, the semicolon, and the final period.
6. No prompt text or interface labels are included.
7. The app remains responsive during copying and pasting.

Automatic visual line wrapping is acceptable and is not a text change. Ignore leading or trailing whitespace when comparing.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
