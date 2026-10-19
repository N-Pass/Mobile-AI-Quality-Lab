# MAQL-4: Request the missing source text instead of inventing a summary

Suite: 03 - Input Handling

Final recorded result: **Passed** — [Run 03](../test-results/run-03.csv)

## Description

Verify that the assistant recognizes a summarization request without source text and asks the user to provide the missing content.

The assistant must not invent source material, summarize unrelated context, or claim that a summary has been completed. These are evaluation criteria defined for this independent study.

## Preconditions

1. The user is signed in to the ChatGPT Android app with a Plus account.

2. Planned environment: ENV-001 — Samsung Galaxy S24 FE, Android 16, One UI 8.5, ChatGPT app 1.2026.265.

3. Planned configuration: Work / 6 Luna / Alta (High).

4. The app language is Brazilian Portuguese.

5. Claro BR mobile data is enabled and internet connectivity is available.

6. Verify and record the actual environment and any differences before execution.

7. Record whether memory and custom instructions are enabled, without copying their personal content.

8. Use a new conversation outside the portfolio project, with no previous messages, attached files, or selected source content.

## Postconditions

Retain the exact submitted prompt and the complete first response as execution evidence. Record the result without providing the missing text during this execution.

## Step 1

Action:

Open a new conversation and verify the configuration specified in the preconditions. Confirm that no source text or attachment has been provided.

Expected result:

A new conversation is available with no previous messages or attachments. The configuration matches the recorded test environment.

## Step 2

Action:

Paste the exact prompt provided in Data. Do not add any text after "Texto:" and do not attach files.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil, preservando as informações essenciais e sem acrescentar fatos.

Texto:
```

Expected result:

The message contains the summarization instruction followed by "Texto:", with no source content after it.

## Step 3

Action:

Send the message once and wait for the response to finish. Do not regenerate the response, provide source text, or send corrective instructions.

Expected result:

The message is submitted and the app displays a complete, readable response.

## Step 4

Action:

Compare the response with the acceptance criteria below and capture the prompt and complete response.

Expected result:

1. The assistant indicates that the source text is missing or clearly asks the user to provide the text to be summarized.

2. It does not invent source material or present a fabricated summary.

3. It does not summarize the instruction itself or unrelated prior information.

4. It does not claim that the requested summary has been completed.

5. The clarification is written in Brazilian Portuguese.

Equivalent wording is acceptable. The clarification does not need to contain two sentences: the two-sentence requirement applies to the requested summary, which cannot be produced without source text.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
