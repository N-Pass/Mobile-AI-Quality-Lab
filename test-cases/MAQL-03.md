# MAQL-3: Preserve total, paid, and outstanding amounts in an English summary

Suite: 01 - Summary Accuracy

Final recorded result: **Passed** — [Run 02](../test-results/run-02.csv)

## Description

Verify that an English summary accurately distinguishes the final order total, the amount already paid, and the outstanding balance.

The summary must preserve the currency and partial-payment status without inventing a completed payment. All amounts are explicitly provided in the source text; no calculation is required.

Documentation update after the initial execution: added the planned preconditions and evidence-retention instructions that were missing from the repository case. This update is not a new test execution and does not confirm any previously unrecorded environment settings.

## Preconditions

1. The ChatGPT Android app is installed and the user is signed in with a Plus account.

2. Planned environment: ENV-001 — Samsung Galaxy S24 FE, Android 16, One UI 8.5, ChatGPT app version 1.2026.265.

3. The planned configuration is Work / 6 Luna / Alta (High).

4. Keep the app interface language set to Brazilian Portuguese. The prompt requests a response in American English.

5. Claro BR mobile data is enabled and internet connectivity is available.

6. Verify and record the actual environment and any deviations before execution.

7. Record whether memory and custom instructions are enabled, without copying their personal content.

8. Use a new conversation outside the portfolio project, with no previous messages or attachments.

## Postconditions

Retain the exact submitted prompt and the complete first response as execution evidence. Record the observed result and any environment deviations in the test run.

## Step 1

Action:

Open a new conversation in the ChatGPT Android app and verify the configuration specified in the preconditions. Keep the app interface language set to Brazilian Portuguese.

Expected result:

A new conversation with no previous messages is available. The configuration matches the recorded test environment, and the app interface remains in Brazilian Portuguese.

## Step 2

Action:

Paste the exact prompt provided in Data into the message field without sending it yet.

Input / baseline:

```text
Summarize the following text in two sentences in American English, preserving the essential information without adding facts.

Text:

The fictional store Maple Supplies issued order 2085 to Jordan Lee for eight notebooks. The merchandise subtotal was USD 96.00. A discount of USD 16.00 reduced the merchandise amount to USD 80.00, and a delivery fee of USD 5.00 brought the final order total to USD 85.00. Jordan has already paid USD 30.00. The remaining balance is USD 55.00 and has not yet been paid. The store emailed Jordan a payment reminder but did not specify a payment deadline.
```

Expected result:

The complete English prompt is present in the message field, with no missing or altered text.

## Step 3

Action:

Send the message once and wait for the response to finish. Record any error or interruption. Do not regenerate the response or send corrective instructions during this execution.

Expected result:

The submitted message appears in the conversation and the app displays a complete, readable summary.

## Step 4

Action:

Compare the complete response with the source text and the acceptance criteria below. Save the submitted prompt and response as execution evidence.

Expected result:

1. The summary identifies USD 85.00 as the final order total.
2. It identifies USD 30.00 as the amount already paid.
3. It identifies USD 55.00 as the outstanding, unpaid balance.
4. The currency is unambiguously identified as US dollars.
5. It does not imply that the order has been fully paid or confuse the subtotal with the final total.
6. Any additional amounts, quantities, names, or identifiers included match the source text.
7. It adds no unsupported facts, including a payment deadline.
8. It is written in American English and contains two sentences.

Equivalent wording and numeric formatting are acceptable. For example, USD 85 and US$85.00 represent the same amount. Exact wording is not required.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
