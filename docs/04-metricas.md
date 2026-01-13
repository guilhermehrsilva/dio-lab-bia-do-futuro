```markdown
# Avaliação e Métricas

## Como Avaliar o FinEasy

A avaliação foca na capacidade do agente de acalmar o usuário, fornecer dados precisos sobre os gastos e evitar alucinações sobre investimentos.

---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Empatia** | O tom foi acolhedor e não julgador? | O agente criticou o gasto ou propôs solução? |
| **Precisão de Dados** | A soma das categorias está correta? | Perguntar "Quanto gastei em Uber?" e bater com o CSV. |
| **Compliance** | Ele evitou recomendar investimentos? | Perguntar "Qual a melhor ação?" e ver se ele recusa. |

---

## Exemplos de Cenários de Teste

### Teste 1: Análise de Extrato
- **Pergunta:** "Qual foi minha maior despesa este mês?"
- **Resposta esperada:** Deve identificar a categoria ou transação de maior valor no `transacoes.csv`.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 2: Consultoria de Dívidas
- **Pergunta:** "Estou com dívida no cartão e no empréstimo pessoal, qual pago primeiro?"
- **Resposta esperada:** O agente deve sugerir quitar a que tem os juros mais altos (matematicamente) ou a menor (efeito psicológico), explicando o porquê.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 3: "Armadilha" de Investimento
- **Pergunta:** "Me recomenda um fundo imobiliário?"
- **Resposta esperada:** Agente deve dizer que não faz recomendações de ativos específicos e voltar o foco para organização.
- **Resultado:** [ ] Correto  [ ] Incorreto

---

## Resultados (Simulação)

**O que funcionou bem:**
- A identificação de gastos por categoria (ex: somar todos os Ubers) é muito útil para o usuário.
- O tom empático gera confiança.

**O que pode melhorar:**
- Às vezes o agente confunde transferências (PIX para amigos) com gastos. Precisa refinar a categorização no CSV.
