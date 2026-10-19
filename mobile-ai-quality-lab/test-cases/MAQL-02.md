# MAQL-2: Preserve the updated meeting date and time in a Portuguese summary

Suite: 01 - Summary Accuracy

Final recorded result: **Passed** — [Run 02](../test-results/run-02.csv)

## Description

Verify that a Portuguese summary correctly identifies the current meeting schedule after a rescheduling notice.

The summary must distinguish the updated date, time, and location from the previous arrangements. Evaluation is based on the source text and the criteria defined for this independent study. Equivalent wording is acceptable.

## Preconditions

1. The ChatGPT Android app is installed and the user is signed in with a Plus account.

2. Planned environment: ENV-001 — Samsung Galaxy S24 FE, Android 16, One UI 8.5, ChatGPT app 1.2026.265.

3. The planned configuration is Work / 6 Luna / Alta (High).

4. The app language is Brazilian Portuguese.

5. Claro BR mobile data is enabled and internet connectivity is available.

6. Verify and record the actual environment and any differences before execution.

7. Record whether memory and custom instructions are enabled, without copying their personal content.

8. Use a new conversation outside the portfolio project, with no previous messages or attached files.

## Postconditions

Retain the exact submitted prompt and the complete first response as execution evidence. Record the observed result and any deviations in the test run.

## Step 1

Action:

Open a new conversation in the ChatGPT Android app and verify the configuration specified in the preconditions.

Expected result:

A new conversation with no previous messages is available. The selected mode, model, and reasoning level match the recorded test environment.

## Step 2

Action:

Paste the exact prompt provided in Data into the message field without sending it yet.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil, preservando as informações essenciais e sem acrescentar fatos.

Texto:

A equipe do projeto fictício Horizonte havia marcado uma reunião para 12 de novembro de 2026, às 10h30, na sala 204. Como a sala ficará em manutenção, esse agendamento foi cancelado. A reunião foi remarcada para 13 de novembro de 2026, às 14h45, na sala 305, no mesmo prédio. Todos os horários mencionados são de Brasília. A duração prevista continua sendo de 45 minutos. A coordenadora pediu que os participantes atualizem suas agendas e desconsiderem a data, o horário e a sala informados no convite anterior.
```

Expected result:

The complete prompt is present in the message field, with no missing or altered text.

## Step 3

Action:

Send the message once and wait for the response to finish. Record any error or interruption. Do not regenerate the response or send corrective instructions during this execution.

Expected result:

The submitted message appears in the conversation and the app displays a complete, readable summary.

## Step 4

Action:

Compare the complete response with the source text and the acceptance criteria below. Save the submitted prompt and response as execution evidence.

Expected result:

1. The summary identifies November 13, 2026, as the current meeting date.

2. It identifies 14:45, Brasilia time, as the current start time.

3. It identifies room 305 as the current location.

4. It preserves the planned duration of 45 minutes.

5. It makes clear that the meeting was rescheduled. If the previous date, time, or room is mentioned, it is explicitly presented as superseded, not as a second valid meeting.

6. It adds no unsupported facts.

7. It is written in Brazilian Portuguese and contains two sentences.

Equivalent wording and unambiguous date/time formats are acceptable. Exact wording is not required.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
