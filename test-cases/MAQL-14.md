# MAQL-14: Preserve people, responsibilities, and pending actions in a summary

Suite: 01 - Summary Accuracy

Final recorded result: **Failed** — [Run 13](../test-results/run-13.csv)

## Description

Verify that the summary correctly associates each person with their actions and preserves the distinction between completed and pending work.

Documentation update after the initial execution: added the submitted prompt and detailed evaluation criteria to the repository case. This update is not a new test execution.

## Preconditions

ENV-001 is available. Verify and record any environment deviations.

Use a new, empty conversation with Work / 6 Luna / High and an active internet connection.

## Step 1

Action:

Abra uma conversa nova e envie o prompt abaixo uma única vez.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil, preservando quem realizou cada ação e o que ainda está pendente. Não acrescente fatos.

Texto:

Na equipe fictícia do projeto Farol, Camila revisou o relatório e o enviou a Bruno. Bruno identificou dois valores incorretos e devolveu o documento a Camila, que corrigiu os dois valores. Depois, Camila enviou a versão corrigida a Renata, responsável pela aprovação final. Renata ainda não analisou essa versão. Bruno ficará responsável por enviar o relatório ao cliente somente após a aprovação de Renata. Até o momento, o cliente não recebeu o relatório.
```

Expected result:

O aplicativo aceita a mensagem e apresenta uma resposta completa.

## Step 2

Action:

Compare a primeira resposta com os critérios abaixo.

Expected result:

1. The summary contains exactly two sentences in Brazilian Portuguese.
2. Camila is correctly identified as the person who reviewed and corrected the report.
3. Bruno is correctly identified as the person who found two incorrect values.
4. Renata is responsible for final approval and has not yet reviewed the corrected version.
5. Bruno will send the report to the client only after Renata's approval.
6. The client has not yet received the report.
7. No responsibilities are swapped and no unsupported facts or changes to the sequence of actions are introduced.

Equivalent wording is acceptable. Evaluate the complete first response without regeneration or corrective prompts.

## Step 3

Action:

Capture o prompt e a resposta completa.

Expected result:

The exact submitted prompt and complete first response are captured as evidence and can be compared with the acceptance criteria.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
