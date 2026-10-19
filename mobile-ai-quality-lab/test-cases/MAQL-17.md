# MAQL-17: Preserve an exception to a general operating schedule

Suite: 01 - Summary Accuracy

Final recorded result: **Failed** — [Run 16](../test-results/run-16.csv)

## Description

Verify that the summary preserves a general opening schedule and a service-specific exception without applying either schedule to the wrong scope.

Documentation update after the initial execution: added the submitted prompt and detailed evaluation criteria to the repository case. This update is not a new test execution.

## Preconditions

ENV-001 is available. Verify and record any environment deviations.

Use a new, empty conversation with Work / 6 Luna / High and an active internet connection.

## Step 1

Action:

Abra uma conversa nova e envie o prompt abaixo uma vez.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil, preservando o horário geral, a exceção e quais serviços continuam disponíveis. Não acrescente fatos.

Texto:

A biblioteca fictícia Alameda funcionará em 10 de dezembro de 2026, das 8h às 18h. Nesse dia, o balcão de empréstimos e devoluções encerrará o atendimento às 12h para uma atualização do sistema. Após as 12h, não será possível emprestar nem devolver livros, mas as salas de leitura e os computadores continuarão disponíveis até as 18h. O balcão retomará o atendimento em 11 de dezembro de 2026, às 8h.
```

Expected result:

Uma resposta completa é apresentada.

## Step 2

Action:

Compare a primeira resposta com os critérios abaixo.

Expected result:

1. The summary contains exactly two sentences in Brazilian Portuguese.
2. It preserves the library's general opening schedule: December 10, 2026, from 08:00 to 18:00.
3. It states that the borrowing and returns desk closes at 12:00 for a system update.
4. It preserves that borrowing and returning books are unavailable after 12:00 that day.
5. It states that reading rooms and computers remain available until 18:00.
6. It preserves that the borrowing and returns desk resumes service on December 11, 2026, at 08:00.
7. It does not imply that the entire library closes at 12:00 or that all services remain available until 18:00.
8. No unsupported facts or contradictions are introduced.

Equivalent wording and unambiguous date/time formats are acceptable. These are acceptance criteria for this independent portfolio study.

## Step 3

Action:

Capture o prompt e a resposta completa.

Expected result:

The exact submitted prompt and complete first response are captured as evidence, allowing comparison of the general schedule, service-specific exception, and service resumption.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
