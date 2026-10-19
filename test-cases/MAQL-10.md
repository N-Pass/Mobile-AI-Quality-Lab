# MAQL-10: Respect a 40-word summary limit while preserving essential facts

Suite: 02 - Language and Instructions

Final recorded result: **Passed** — [Run 09](../test-results/run-09.csv)

## Description

Verify that the assistant produces a Brazilian Portuguese summary of no more than 40 words while preserving the essential service interruption details.

## Preconditions

ENV-001 is available. Verify and record the actual environment and any deviations.

Start a new conversation with no previous messages or attachments. Record the state of memory and custom instructions.

## Postconditions

Preserve the exact submitted prompt and complete first response. Record the word count and assessment. Do not regenerate the response or send corrective follow-up messages during this execution.

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
Resuma o texto abaixo em português do Brasil, usando no máximo 40 palavras, em um único parágrafo, sem título. Preserve a data, o intervalo de horário, o serviço afetado e o serviço que continuará funcionando. Não acrescente fatos.

Para este pedido, conte como palavra cada elemento separado por espaços; números e horários também contam.

Texto:

O clube fictício Jardim do Lago informou que a piscina ficará fechada em 25 de novembro de 2026, das 8h às 12h, para manutenção do sistema de filtragem. Durante esse período, não será permitida a entrada de usuários na área da piscina. A academia continuará funcionando normalmente. O aviso foi colocado na recepção e enviado por e-mail aos associados. A administração orientou os usuários a planejarem suas atividades considerando a interdição temporária.
```

Expected result:

The complete prompt is submitted and the first response is available for assessment.

## Step 3

Action:

Count the words in the complete response and compare it against all acceptance criteria.

Expected result:

1. The complete response contains no more than 40 words.
2. The response is a single paragraph without a title.
3. The response is written in Brazilian Portuguese.
4. It preserves November 25, 2026 as the date of the closure.
5. It preserves the closure interval from 08:00 to 12:00.
6. The swimming pool is clearly identified as closed during that interval.
7. The gym is correctly described as continuing to operate normally.
8. No unsupported facts or contradictions are introduced.

Counting rule: trim leading and trailing whitespace, then count each non-empty element separated by whitespace as one word. Numbers and times count as words; attached punctuation does not add words. Count all text in the response.

Exactly 40 words is acceptable. Equivalent wording and unambiguous date formats are acceptable. Details not required above may be omitted.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
