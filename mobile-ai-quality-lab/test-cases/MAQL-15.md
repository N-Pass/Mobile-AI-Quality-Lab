# MAQL-15: Summarize only the requested section without mixing information

Suite: 02 - Language and Instructions

Final recorded result: **Passed** — [Run 14](../test-results/run-14.csv)

## Description

Verify that the assistant summarizes only Notice B and does not include facts that belong exclusively to Notice A.

Documentation update after the initial execution: added the submitted prompt and detailed evaluation criteria to the repository case. This update is not a new test execution.

## Preconditions

ENV-001 is available. Verify and record any environment deviations.

Use a new, empty conversation with Work / 6 Luna / High and an active internet connection.

## Step 1

Action:

Abra uma conversa nova e envie o prompt abaixo uma vez.

Input / baseline:

```text
Resuma somente o Aviso B em duas frases, em português do Brasil. Preserve o local, a atividade, a data, o horário, a forma de inscrição e a informação sobre materiais. Não inclua informações exclusivas do Aviso A nem acrescente fatos.

Aviso A:

O centro cultural fictício Estação Norte realizará uma oficina gratuita de pintura em 5 de dezembro de 2026, das 9h às 11h. As inscrições serão feitas pelo site. Serão oferecidas 30 vagas, e todos os materiais estarão incluídos.

Aviso B:

O centro cultural fictício Estação Sul realizará uma oficina de cerâmica em 8 de dezembro de 2026, das 14h às 17h. As inscrições serão feitas presencialmente na recepção. Cada participante deverá levar um avental; a argila e as ferramentas serão fornecidas pelo centro cultural. O aviso não informa o preço nem a quantidade de vagas.
```

Expected result:

Uma resposta completa é apresentada.

## Step 2

Action:

Compare a primeira resposta com os critérios abaixo.

Expected result:

1. The summary contains exactly two sentences in Brazilian Portuguese.

2. It identifies Estação Sul and the pottery workshop.

3. It preserves December 8, 2026, from 14:00 to 17:00.

4. It states that registration is in person at the reception.

5. It preserves that participants must bring an apron, while clay and tools are provided by the cultural center.

6. It includes no information exclusive to Notice A, such as Estação Norte, painting, December 5, online registration, free participation, or 30 places.

7. It introduces no unsupported facts, including a price or participant capacity for Notice B.

Equivalent wording is acceptable. Explicitly stating that the price and capacity are not provided is optional.

## Step 3

Action:

Capture o prompt e a resposta completa.

Expected result:

As evidências permitem comparar os dois avisos com o resumo.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
