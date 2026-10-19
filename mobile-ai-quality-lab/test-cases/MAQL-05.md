# MAQL-5: Summarize an English source text in Brazilian Portuguese

Suite: 02 - Language and Instructions

Final recorded result: **Passed** — [Run 04](../test-results/run-04.csv)

## Description

Verify that the assistant follows the requested output language when it differs from the source language, while preserving essential facts and the requested two-sentence format.

## Preconditions

ENV-001 is available. Verify and record the actual environment before execution.

Start a new conversation with no previous messages or attachments. Record the state of memory and custom instructions.

Use the exact prompt provided in the test steps.

## Postconditions

Preserve the exact submitted prompt and the complete first response. Record the assessment and attach execution evidence. Do not regenerate the response or send corrective follow-up messages during this execution.

## Step 1

Action:

Open a new conversation in the ChatGPT Android app and verify the planned environment.

Expected result:

A new conversation is ready. The actual environment and any deviations are recorded.

## Step 2

Action:

Paste the exact prompt from the Data field and send it once.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil, preservando as informações essenciais e sem acrescentar fatos.

Texto:

The fictional store Maple Supplies issued order 2085 to Jordan Lee for eight notebooks. The merchandise subtotal was USD 96.00. A discount of USD 16.00 reduced the merchandise amount to USD 80.00, and a delivery fee of USD 5.00 brought the final order total to USD 85.00. Jordan has already paid USD 30.00. The remaining balance is USD 55.00 and has not yet been paid. The store emailed Jordan a payment reminder but did not specify a payment deadline.
```

Expected result:

The complete prompt is submitted, including the English source text and the instruction requesting Brazilian Portuguese.

## Step 3

Action:

Wait for the complete first response and compare it against all acceptance criteria.

Expected result:

1. The response is written in Brazilian Portuguese. Proper names and the currency code USD may remain unchanged.

2. The response contains exactly two sentences, without an additional introduction or closing note.

3. The final order total is correctly identified as USD 85.00.

4. The amount already paid is correctly identified as USD 30.00.

5. The outstanding balance is correctly identified as USD 55.00 and remains unpaid.

6. The currency remains unambiguous, with no conversion to Brazilian reais.

7. Any additional details included match the source. No payment deadline or other unsupported fact is invented.

Equivalent wording and Brazilian number formatting are acceptable. Decimal separators do not count as sentence boundaries.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
