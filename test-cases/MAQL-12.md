# MAQL-12: Preserve a completed conversation after backgrounding and resuming the Android app

Suite: 04 - Mobile Usability and Connectivity

Final recorded result: **Passed** — [Run 11](../test-results/run-11.csv)

## Description

Verify that a completed prompt and assistant response remain intact and accessible after the app stays in the background for 30 seconds and is resumed.

## Preconditions

ENV-001 is available. Verify and record the actual environment and any deviations.

Open the original conversation containing the completed swimming pool summary. No response generation is in progress, and the message input field is empty.

Keep the network connection unchanged throughout the test.

## Postconditions

Preserve before-and-after evidence and record any errors or recovery actions. Leave the original conversation unchanged.

## Step 1

Action:

Open the original swimming pool conversation. Capture the completed response and verify it matches the baseline.

Input / baseline:

```text
A piscina do clube Jardim do Lago ficará fechada em 25 de novembro de 2026, das 8h às 12h, para manutenção; a academia continuará funcionando normalmente.
```

Expected result:

The original prompt and complete assistant response are accessible. The response matches the baseline.

## Step 2

Action:

Press the Android Home button to put the app in the background. Wait 30 seconds without closing the app, locking the screen, or changing connectivity.

Expected result:

The Android home screen is displayed, and the app remains in the background for 30 seconds.

## Step 3

Action:

Open Android Recent Apps and select ChatGPT to return to the app.

Expected result:

The app resumes the same conversation without requiring a new login or manual reopening of the conversation.

## Step 4

Action:

Scroll through the original prompt and response, compare the response with the baseline, and capture evidence.

Expected result:

1. The same conversation is displayed after resuming.

2. The original prompt and complete response remain accessible by scrolling.

3. The response text matches the baseline without missing, altered, or duplicated content.

4. No additional message or regenerated response appears.

5. The app responds to scrolling and tapping the message input field.

6. No crash, error dialog, or manual recovery action occurs.

A changed scroll position alone is acceptable if the complete conversation remains accessible. Automatic visual line wrapping is acceptable.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
