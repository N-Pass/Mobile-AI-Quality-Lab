# MAQL-8: Preserve conflicting information without inventing a resolution

Suite: 03 - Input Handling

Final recorded result: **Passed** — [Run 07](../test-results/run-07.csv)

## Description

Verify that the assistant explicitly reports conflicting event dates in the source instead of selecting one as confirmed or inventing a resolution.

## Preconditions

ENV-001 is available. Verify and record the actual environment and any deviations.

Start a new conversation with no previous messages or attachments. Record the state of memory and custom instructions.

## Postconditions

Preserve the exact submitted prompt and complete first response. Do not regenerate the response or send corrective follow-up messages during this execution.

## Step 1

Action:

Open a new conversation in the ChatGPT Android app and verify the planned environment.

Expected result:

A new conversation is ready, and the actual environment is recorded.

## Step 2

Action:

Submit the exact prompt from the Data field once and wait for the complete first response.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil, preservando as informações essenciais e sem acrescentar fatos.

Texto:

O centro cultural fictício Pátio Azul divulgou dois comunicados sobre a mesma oficina de fotografia. Um comunicado informa que a oficina acontecerá em 7 de dezembro de 2026, às 15h, na sala 4. O outro informa que ela acontecerá em 9 de dezembro de 2026, também às 15h, na sala 4. Os comunicados não têm data de publicação e nenhum deles indica que substitui ou corrige o outro. A organização ainda não confirmou qual é a data correta. A participação será gratuita, com 15 vagas, e as inscrições ainda não foram abertas.
```

Expected result:

The complete prompt is submitted and the first response is available for assessment.

## Step 3

Action:

Compare the complete response against all acceptance criteria.

Expected result:

1. The response explicitly identifies a conflict between December 7 and December 9, 2026, for the same workshop.

2. Neither date is presented as confirmed, corrected, newer, or authoritative.

3. The response preserves that the organizer has not confirmed the correct date.

4. The response does not invent a rescheduling, cancellation, second session, or explanation for the discrepancy.

5. The shared time of 15:00 and room 4 are preserved.

6. Free participation, the capacity of 15 participants, and registration not yet being open are preserved.

7. The response contains exactly two sentences in Brazilian Portuguese.

8. No unsupported facts or contradictions are introduced.

Equivalent wording and unambiguous date formats are acceptable. Reporting the unresolved conflict is the expected behavior.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
