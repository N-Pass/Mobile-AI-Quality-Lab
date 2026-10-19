# MAQL-16: Summarize incomplete source text without inventing missing information

Suite: 03 - Input Handling

Final recorded result: **Passed** — [Run 15](../test-results/run-15.csv)

## Description

Verify that the assistant preserves available facts and explicitly identifies missing information when the source ends mid-sentence.

Documentation update after the initial execution: added the submitted prompt and detailed evaluation criteria to the repository case. This update is not a new test execution.

## Preconditions

ENV-001 is available. Verify and record any environment deviations.

Use a new, empty conversation with Work / 6 Luna / High and an active internet connection.

## Step 1

Action:

Abra uma conversa nova e envie o prompt abaixo, mantendo o final incompleto.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil. Preserve as informações disponíveis e indique qualquer informação incompleta, sem tentar adivinhar o trecho ausente.

Texto:

A loja fictícia Ponte Nova recebeu o pedido 4186 de Lucas Mendes para duas cadeiras. O pagamento foi confirmado, mas o pedido ainda não foi enviado. A equipe informou que a entrega está prevista para o dia 14 de
```

Expected result:

O aplicativo aceita a mensagem e apresenta uma resposta.

## Step 2

Action:

Compare a primeira resposta com os critérios abaixo.

Expected result:

1. The summary contains exactly two sentences in Brazilian Portuguese.
2. It preserves Ponte Nova, order 4186, Lucas Mendes, and the quantity of two chairs.
3. Payment is correctly described as confirmed.
4. The order is clearly described as not yet shipped.
5. The response explicitly indicates that the delivery date or the source passage containing it is incomplete.
6. It does not invent the missing month, year, or any continuation of the interrupted text. Mentioning day 14 is acceptable when the date is clearly qualified as incomplete.
7. No unsupported facts or contradictions are introduced.

Equivalent wording is acceptable. Evaluate the complete first response without regeneration or corrective prompts.

## Step 3

Action:

Capture o prompt e a resposta completa.

Expected result:

The exact submitted prompt and complete first response are captured as evidence, showing the incomplete source passage and how the assistant handled it.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
