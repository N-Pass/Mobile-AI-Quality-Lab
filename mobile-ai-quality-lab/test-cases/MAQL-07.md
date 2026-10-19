# MAQL-7: Preserve uncertainty and conditions in a Portuguese summary

Suite: 01 - Summary Accuracy

Final recorded result: **Passed** — [Run 06](../test-results/run-06.csv)

## Description

Verify that the assistant preserves tentative dates, pending approval, and conditional outcomes without presenting them as confirmed facts.

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

A empresa fictícia Brisa está avaliando lançar um aplicativo de organização pessoal em dezembro de 2026, mas essa previsão ainda não foi confirmada. O lançamento depende da conclusão dos testes de segurança e da aprovação do orçamento, que continua em análise. Se os testes identificarem falhas críticas, o lançamento será adiado, mas nenhuma nova data foi definida. A equipe está considerando oferecer uma versão gratuita, porém essa decisão também não foi aprovada. Até o momento, não há inscrições abertas para usuários.
```

Expected result:

The complete prompt is submitted and the first response is available for assessment.

## Step 3

Action:

Compare the complete response against all acceptance criteria.

Expected result:

1. December 2026 is presented as a tentative launch date, not a confirmed commitment.

2. The launch remains dependent on completion of security testing and budget approval; neither is presented as completed or approved.

3. Postponement remains conditional on critical findings in testing, rather than being presented as already decided.

4. No replacement launch date is invented.

5. A free version remains under consideration and is not presented as approved or guaranteed.

6. User registration is described as not yet open.

7. The response contains exactly two sentences in Brazilian Portuguese.

8. No unsupported facts or contradictions are introduced.

Equivalent wording is acceptable when it preserves the original degree of certainty and the stated conditions.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
