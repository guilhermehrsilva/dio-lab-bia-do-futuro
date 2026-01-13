# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Para que ser o FinEASY? |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores |
| `perfil_investidor.json` | JSON | Personalizar recomendações |
| `produtos_financeiros.json` | JSON | Sugerir produtos adequados ao perfil |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente |

> [!TIP]
> **Quer um dataset mais robusto?** Você pode utilizar datasets públicos do [Hugging Face](https://huggingface.co/datasets) relacionados a finanças, desde que sejam adequados ao contexto do desafio.

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

[Não houve modificações]

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

[ex: Os JSON/CSV são carregados no início da sessão e incluídos no contexto do prompt]

``` python

import pandas as pd
import json

# CSVs
historico = pd.read_csv('data/historico_atendimento.csv')
transacoes = pd.read_csv('data/transacoes.csv')

# JSONs
with open('data/perfil_investidor.json', 'r', encoding='utf-8') as f:
    perfil = json.load(f)

with open('data/produtos_financeiros.json', 'r', encoding='utf-8') as f:
    produtos = json.load(f)

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?


---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
=== DADOS DO USUÁRIO ===
Nome: Ana Souza
Situação Atual: Endividada (Cheque Especial)
Renda Líquida: R$ 3.500,00

=== RESUMO DO MÊS ATUAL ===
Total Gasto: R$ 3.850,00 (Saldo: -R$ 350,00)
Principais Ofensores:
1. Alimentação/Delivery: R$ 1.200,00
2. Assinaturas/Streaming: R$ 300,00
3. Transporte app: R$ 450,00

=== ÚLTIMA INTERAÇÃO ===
Usuário prometeu reduzir delivery para R$ 600,00.
...
```
