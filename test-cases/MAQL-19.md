# MAQL-19: Follow a format change in the same conversation while preserving source facts

Suite: 02 - Language and Instructions

Final recorded result: **Passed** — [Run 18](../test-results/run-18.csv)

## Description

Verify that a follow-up request changes a two-sentence summary into exactly three bullet points while preserving the original facts and pending actions.

Documentation update after the initial execution: added both submitted prompts and the detailed follow-up evaluation criteria to the repository case. This update is not a new test execution.

## Preconditions

ENV-001 is available. Verify and record any environment deviations.

Start a new, empty conversation with Work / 6 Luna / High and an active internet connection. Send both prompts in that same conversation.

## Step 1

Action:

Envie o primeiro prompt e aguarde a resposta completa. Capture a tela.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil, preservando todas as informações essenciais e sem acrescentar fatos.

Texto:

O espaço fictício Casa do Cedro cancelou a oficina de encadernação marcada para 15 de dezembro de 2026 porque o instrutor ficou indisponível. Os 12 inscritos foram avisados por e-mail. Todos haviam pago a taxa de R$ 40,00 por pessoa. O reembolso integral será realizado até 18 de dezembro de 2026, mas ainda não foi processado. Não há uma nova data definida para a oficina.
```

Expected result:

Resumo em duas frases, em pt-BR, preservando os fatos do texto.

## Step 2

Action:

Na **mesma conversa**, envie o segundo prompt e aguarde a resposta completa.

Input / baseline:

```text
Agora apresente as informações do texto original em exatamente três tópicos com marcadores, sem título, introdução, conclusão ou subtópicos. No primeiro, informe a oficina, a data cancelada e o motivo; no segundo, informe os inscritos, o aviso e o valor pago por pessoa; no terceiro, informe o prazo e a situação do reembolso e a ausência de nova data. Mantenha o português do Brasil e não acrescente fatos.
```

Expected result:

A nova resposta tem exatamente três tópicos e mantém as informações solicitadas.

## Step 3

Action:

Capture a segunda resposta e compare com os critérios abaixo.

Expected result:

1. The follow-up response contains exactly three top-level bullet points, with no title, introduction, conclusion, or nested bullets.

2. The first bullet identifies the Casa do Cedro bookbinding workshop, its canceled date of December 15, 2026, and the instructor's unavailability as the reason.

3. The second bullet preserves the 12 registered participants, notification by email, and the amount of R$40.00 paid per person.

4. The third bullet preserves the full refund deadline of December 18, 2026, states that the refund has not yet been processed, and states that no new workshop date has been defined.

5. The response remains in Brazilian Portuguese and introduces no unsupported facts or contradictions.

6. The follow-up uses the original source information from the same conversation without requiring the source text to be submitted again.

Equivalent wording is acceptable. Preserve both submitted prompts and both complete responses as evidence.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
