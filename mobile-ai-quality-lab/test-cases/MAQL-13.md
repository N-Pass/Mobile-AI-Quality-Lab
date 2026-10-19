# MAQL-13: Handle an offline message submission and recover after reconnecting

Suite: 04 - Mobile Usability and Connectivity

Final recorded result: **Passed** — [Run 12](../test-results/run-12.csv)

## Description

Verify that an offline message submission provides visible feedback or a pending state, preserves the submitted text, and allows recovery after connectivity is restored without duplicating messages.

Documentation update after the initial execution: added the exact prompt used for the offline submission and recovery test. This update is not a new test execution.

## Preconditions

ENV-001 is available. Record any environment deviations.

Start a new, empty conversation with Work / 6 Luna / High.

Confirm that the app works while connected.

No response generation is in progress.

## Step 1

Action:

Em uma conversa nova, cole o prompt abaixo, sem enviar.

Input / baseline:

```text
Resuma o texto abaixo em uma frase, em português do Brasil, sem acrescentar fatos.

Texto:

A biblioteca fictícia Jardim das Letras estará fechada em 26 de novembro de 2026 para manutenção elétrica. O atendimento será retomado em 27 de novembro de 2026, às 9h.
```

Expected result:

O texto completo aparece no campo de mensagem.

## Step 2

Action:

Desative os dados móveis e confirme que o Wi-Fi também está desligado. Volte ao aplicativo.

Expected result:

O aparelho permanece sem conexão com a internet.

## Step 3

Action:

Toque em enviar uma única vez. Observe por até 60 segundos e capture a tela.

Expected result:

O aplicativo mostra erro de conexão, estado pendente ou envio indisponível. O texto permanece visível ou recuperável.

## Step 4

Action:

Reative os dados móveis Claro BR e volte ao aplicativo. Se houver opção de tentar novamente, use-a uma vez; se o texto continuar no campo sem envio pendente, envie uma vez.

Expected result:

O envio pode ser retomado sem precisar reescrever o texto.

## Step 5

Action:

Aguarde até 120 segundos e confira a conversa.

Expected result:

Uma resposta é concluída, sem mensagens duplicadas, travamento ou necessidade de reiniciar o aplicativo.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
