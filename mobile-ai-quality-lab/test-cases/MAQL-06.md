# MAQL-6: Follow an exact three-bullet summary format in Brazilian Portuguese

Suite: 02 - Language and Instructions

Final recorded result: **Passed** — [Run 05](../test-results/run-05.csv)

## Description

Verify that the assistant summarizes a source text using exactly three bullet points in Brazilian Portuguese, without an introduction, conclusion, or nested bullets, while preserving essential facts.

## Preconditions

ENV-001 is available. Verify and record the actual environment and any deviations.

Start a new conversation with no previous messages or attachments. Record the state of memory and custom instructions.

## Postconditions

Preserve the exact submitted prompt and complete first response as evidence. Do not regenerate the response or send corrective follow-up messages during this execution.

## Step 1

Action:

Open a new conversation in the ChatGPT Android app and verify the planned environment.

Expected result:

A new conversation is ready, and the actual environment is recorded.

## Step 2

Action:

Paste the exact prompt from the Data field, send it once, and wait for the complete first response.

Input / baseline:

```text
Resuma o texto abaixo em português do Brasil, usando exatamente três tópicos com marcadores, sem subtópicos. Não inclua título, introdução ou conclusão. Preserve as informações essenciais e não acrescente fatos.

Texto:

A biblioteca fictícia Vila Clara realizará uma oficina gratuita de escrita criativa em 21 de novembro de 2026, das 14h às 16h, na sala 2. A atividade será destinada a pessoas com 16 anos ou mais e terá 20 vagas. As inscrições deverão ser feitas presencialmente na recepção da biblioteca até 18 de novembro de 2026 e poderão encerrar antes dessa data caso todas as vagas sejam preenchidas. Cada participante deverá levar um caderno e uma caneta. A biblioteca fornecerá os demais materiais, mas não emitirá certificado.
```

Expected result:

The complete prompt is submitted and the first response is available for assessment.

## Step 3

Action:

Compare the complete response against all acceptance criteria.

Expected result:

1. The response contains exactly three top-level bullet points, with no nested bullets.

2. There is no title, introduction, conclusion, or other text outside the three bullet points.

3. The response is written in Brazilian Portuguese.

4. It preserves the free writing workshop, November 21, 2026, the 14:00–16:00 time range, and room 2.

5. It preserves the minimum age of 16 and the capacity of 20 participants.

6. It states that registration is in person at the library reception, with a November 18, 2026 deadline that may close earlier if all places are filled.

7. It preserves the requirement to bring a notebook and pen, the provision of other materials by the library, and the absence of a certificate.

8. No unsupported facts or contradictions are introduced.

Equivalent wording and unambiguous date formats are acceptable. Any standard bullet symbol is acceptable. Visual line wrapping does not create additional bullet points.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
