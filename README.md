# 💰 FinEasy: Seu Mentor Financeiro Inteligente

O **FinEasy** é um assistente financeiro pessoal especializado em organização financeira, controle de gastos e estratégias práticas para sair das dívidas. Ele combina análise de dados técnicos com uma abordagem profundamente empática, didática e livre de julgamentos para transformar a saúde financeira do usuário.

---

## 🎯 Visão Geral

### O Problema
Muitas pessoas sofrem com a "ansiedade financeira" e a falta de clareza sobre o destino do seu dinheiro. O medo do julgamento e o uso de termos técnicos complexos ("economês") afastam o usuário comum da organização de suas contas, gerando um ciclo de endividamento crônico.

### A Solução
O FinEasy atua como um organizador proativo que analisa transações reais para identificar gargalos e recomendar estratégias de saneamento, como o método bola de neve ou a regra 50/30/20. Ele oferece acolhimento para reduzir o estresse e prevenir o superendividamento através de tecnologia humanizada.

---

## 🤖 Persona e Tom de Voz

* **Nome:** FinEasy.
* **Personalidade:** Mentor compreensivo, educativo e extremamente paciente.
* **Tom de Voz:** Acessível e **jamais julgador**; entende que lidar com dinheiro é estressante.
* **Regras de Ouro:**
    * Basear respostas estritamente nos dados financeiros fornecidos no contexto (transações, perfil, histórico).
    * **Não fornece recomendações de investimento** (Ações, Cripto, FIIs).
    * Nunca solicita senhas, tokens ou dados sensíveis.
    * Ser prático e específico em vez de genérico.

---

## 🛠️ Arquitetura e Base de Conhecimento

O sistema utiliza arquivos locais para contextualizar cada atendimento:

| Arquivo | Formato | Finalidade |
| :--- | :--- | :--- |
| `transacoes.csv` | CSV | Analisar o padrão real de gastos e identificar ofensores no orçamento. |
| `perfil_investidor.json` | JSON | Personalizar o atendimento de acordo com o perfil do usuário. |
| `historico_atendimento.csv`| CSV | Contextualizar interações anteriores para continuidade do plano. |
| `produtos_financeiros.json`| JSON | Sugerir produtos adequados ao perfil (focados em organização/segurança). |

### Estratégia de Integração
Os dados são carregados via Python (Pandas/JSON) e incluídos dinamicamente no contexto do prompt do agente.

---

## 🚀 Instalação e Configuração

Siga os passos abaixo para configurar o ambiente do FinEasy:

### 1. Pré-requisitos
* Python 3.9+
* Chave de API de um provedor de LLM (ex: OpenAI, Gemini).

### 2. Configurar o Ambiente
```bash
# Clone o repositório
git clone [https://github.com/seu-usuario/fineasy.git](https://github.com/seu-usuario/fineasy.git)
cd fineasy

# Crie e ative um ambiente virtual
python -m venv venv
source venv/bin/activate  # Linux/Mac
.\venv\Scripts\activate   # Windows

# Instale as dependências
pip install pandas streamlit openai
