# MAQL-1: Preserve negation when summarizing a rejected order in Portuguese

Suite: 01 - Summary Accuracy

Final recorded result: **Passed** — [Run 01](../test-results/run-01.csv)

## Description

Verify that a Portuguese summary preserves the explicit rejection of an order and does not imply approval, payment, or shipment.

Evaluation is based on the source text and the criteria defined for this independent study. Equivalent wording is acceptable; an exact response is not required.

## Preconditions

1. The ChatGPT Android app is installed and the user is signed in with a Plus account.

2. ENV-001 is available: Samsung Galaxy S24 FE, Android 16, One UI 8.5, ChatGPT app version 1.2026.265.

3. The selected configuration is Work / 6 Luna / Alta (High), as displayed in the app.

4. The app language is Brazilian Portuguese.

5. Claro BR mobile data is enabled and internet connectivity is available.

6. Record the actual environment and any differences from ENV-001 before execution.

7. Record whether memory and custom instructions are enabled, without copying their personal content.

8. Use a new conversation outside this portfolio project, with no previous messages or attached files.

## Postconditions

Retain the exact submitted prompt and the complete response as execution evidence. Record the observed result and any deviations in the test run.

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

A loja fictícia Aurora recebeu o pedido 1042 de Ana Costa para a compra de 12 cadernos. Após verificar o estoque, a equipe constatou que não havia unidades disponíveis. Por esse motivo, o pedido não foi aprovado. Nenhum valor foi cobrado e nenhum produto foi enviado. Ana foi informada da recusa por e-mail. A equipe explicou que ela poderá fazer um novo pedido quando o estoque for reposto, mas não informou uma data para isso.
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

1. The summary explicitly states that the order was not approved or was rejected because the items were out of stock.

2. It preserves that no payment was charged and no products were shipped.

3. It does not imply that the order was approved, paid, or shipped.

4. It does not invent facts, including a restocking date or a guaranteed future approval.

5. Any names, quantities, or order identifiers included in the summary match the source text.

6. The summary is written in Brazilian Portuguese and contains two sentences.

Equivalent wording is acceptable. Exact wording is not required.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
