# MAQL-20: Retrieve a completed conversation after closing and reopening the Android app

Suite: 04 - Mobile Usability and Connectivity

Final recorded result: **Passed** — [Run 19](../test-results/run-19.csv)

## Description

Verify that a completed conversation remains available with its original prompt and response after the app is dismissed from Android Recent Apps and reopened.

Documentation update after the initial execution: added the planned Rota Clara response baseline and detailed recovery criteria.

Execution deviation: the initial execution used the conversation containing the test instructions instead of the planned Rota Clara conversation. Its before-and-after evidence belongs to that alternative conversation.

This documentation update is not a new test execution and does not establish that the planned Rota Clara conversation was tested.

## Preconditions

ENV-001 is available. Verify and record any environment deviations.

Use the existing Rota Clara conversation about shipment 5820 and four boxes. The response is complete and the message input field is empty.

Keep the internet connection active and unchanged throughout the test.

## Step 1

Action:

Abra a conversa da **remessa 5820**, confira a resposta e faça um print antes de fechar.

Input / baseline:

```text
A empresa fictícia Rota Clara preparou a remessa 5820 com quatro caixas, cada uma pesando 2,5 kg e medindo 30 cm de comprimento, 20 cm de largura e 15 cm de altura; o peso total é de 10 kg. A remessa aguarda coleta pela transportadora e ainda não foi enviada.
```

Expected result:

O pedido e a resposta original estão acessíveis, sem geração em andamento.

## Step 2

Action:

Abra os aplicativos recentes do Android e deslize o cartão do ChatGPT para removê-lo da lista.

Expected result:

O cartão do aplicativo deixa de aparecer nos recentes.

## Step 3

Action:

Abra novamente o ChatGPT pelo ícone.

Expected result:

O aplicativo abre sem erro ou solicitação inesperada de login.

## Step 4

Action:

Se a conversa não abrir automaticamente, localize-a no histórico e abra.

Expected result:

A conversa da remessa 5820 pode ser recuperada.

## Step 5

Action:

Role para conferir o pedido e a resposta completa. Toque no campo de mensagem, sem digitar ou enviar, e capture a resposta novamente.

Expected result:

1. The original Rota Clara conversation is accessible after reopening, either automatically or through history.

2. The original prompt and complete response remain accessible by scrolling.

3. The response text matches the before-closing evidence, without missing, altered, or duplicated content.

4. No additional message or regenerated response appears.

5. Scrolling and tapping the message input field work normally.

6. No crash, error dialog, unexpected login request, or additional app restart is required.

A different scroll position or changed visual line wrapping is acceptable. Opening the conversation through history is an allowed step.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
