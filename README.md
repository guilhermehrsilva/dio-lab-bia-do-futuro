# 💰 FinEasy: Seu Mentor Financeiro Inteligente

O **FinEasy** é um assistente financeiro pessoal especializado em organização financeira, controle de gastos e estratégias práticas para sair das dívidas. Diferente de ferramentas tradicionais, ele combina análise de dados técnicos com uma abordagem profundamente empática, didática e livre de julgamentos.

---

## 🎯 Visão Geral

### O Problema
Muitas pessoas sofrem com a "ansiedade financeira" e a falta de clareza sobre o destino do seu dinheiro. O medo do julgamento e o uso de termos técnicos complexos ("economês") afastam o usuário comum da organização de suas contas, gerando um ciclo de endividamento.

### A Solução
O FinEasy atua como um organizador proativo que analisa transações reais para identificar gargalos e recomendar estratégias de saneamento (como o método bola de neve ou a regra 50/30/20). Ele oferece acolhimento para reduzir o estresse e prevenir o superendividamento através de tecnologia humanizada.

---

## 🤖 Persona e Tom de Voz

* **Nome:** FinEasy.
* **Personalidade:** Mentor compreensivo, educativo e extremamente paciente.
* **Tom de Voz:** Acessível e **jamais julgador**. Entende que gastar é humano, mas ajuda a retomar o controle.
* **Regras de Ouro:**
    * Basear respostas estritamente nos dados financeiros fornecidos.
    * **Não fornece recomendações de investimento** (Ações, Cripto, FIIs).
    * Nunca solicita senhas ou dados sensíveis.
    * Foco em ações práticas (ex: sugerir reduções específicas em categorias de lazer/delivery).

---

## 🛠️ Arquitetura e Dados

O sistema utiliza arquivos locais para contextualizar cada atendimento, garantindo que a IA conheça o histórico e o perfil do usuário:

| Arquivo | Formato | Finalidade |
| :--- | :--- | :--- |
| `transacoes.csv` | CSV | Análise do padrão real de gastos e identificação de excessos. |
| `perfil_investidor.json` | JSON | Personalização do tom de voz e das metas educativas. |
| `historico_atendimento.csv`| CSV | Continuidade do atendimento e contexto de conversas passadas. |
| `produtos_financeiros.json`| JSON | Sugestão de produtos focados em organização e reserva de segurança. |

---

## 🚀 Instalação e Configuração

Siga os passos abaixo para configurar o ambiente do FinEasy em sua máquina:

### 1. Pré-requisitos
* Python 3.9 ou superior.
* Uma chave de API de um provedor de LLM (OpenAI, Anthropic ou Google Gemini).

### 2. Clonar o Repositório
```bash
git clone [https://github.com/seu-usuario/fineasy.git](https://github.com/seu-usuario/fineasy.git)
cd fineasy

# Criar o ambiente
python -m venv venv

# Ativar o ambiente (Windows)
.\venv\Scripts\activate

# Ativar o ambiente (Linux/Mac)
source venv/bin/activate

pip install pandas streamlit openai  # Adicione outras libs se houver (ex: google-generativeai)
