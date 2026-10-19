# MAQL-18: Preserve quantities, measurement units, and per-item versus total values

Suite: 01 - Summary Accuracy

Final recorded result: **Passed** — [Run 17](../test-results/run-17.csv)

## Description

Verify that the summary preserves package quantities, per-box weight, total weight, and dimensions without confusing their scope or units.

Documentation update after the initial execution: added the submitted prompt and detailed evaluation criteria to the repository case. This update is not a new test execution.

## Preconditions

ENV-001 is available. Verify and record any environment deviations.

Use a new, empty conversation with Work / 6 Luna / High and an active internet connection.

## Step 1

Action:

Abra uma conversa nova e envie o prompt abaixo uma vez.

Input / baseline:

```text
Resuma o texto abaixo em duas frases, em português do Brasil. Preserve o número da remessa, a quantidade de caixas, o peso de cada caixa, o peso total, as dimensões de cada caixa e a situação do envio. Não converta as unidades nem acrescente fatos.

Texto:

A empresa fictícia Rota Clara preparou a remessa 5820 com quatro caixas. Cada caixa pesa 2,5 kg e mede 30 cm de comprimento, 20 cm de largura e 15 cm de altura. O peso total das quatro caixas é de 10 kg. Todas as caixas têm o mesmo peso e as mesmas dimensões. A remessa aguarda coleta pela transportadora e ainda não foi enviada. Não há previsão de entrega informada.
```

Expected result:

Uma resposta completa é apresentada.

## Step 2

Action:

Compare a primeira resposta com os critérios abaixo.

Expected result:

1. The summary contains exactly two sentences in Brazilian Portuguese.

2. It preserves shipment number 5820 and the quantity of four boxes.

3. It identifies 2.5 kg as the weight of each box.

4. It identifies 10 kg as the total weight of all four boxes.

5. It preserves each box's dimensions: 30 cm long, 20 cm wide, and 15 cm high.

6. It clearly distinguishes per-box measurements from the total shipment weight and does not convert the units.

7. It states that the shipment is awaiting collection by the carrier and has not yet been shipped.

8. No unsupported facts or contradictions are introduced, including an invented delivery date.

Equivalent wording and decimal separators are acceptable. Explicitly mentioning the absence of a delivery estimate is optional.

## Step 3

Action:

Capture o prompt e a resposta completa.

Expected result:

As evidências permitem conferir todos os valores.

## Evidence and execution qualifications

See the [evidence index](../evidence/README.md) and [summary report](../docs/test-summary-report.md). The original run export preserves the execution-time snapshot.
