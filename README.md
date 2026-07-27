# 🛡️ LAB 01: Prompt Injection & Defense in Depth (OWASP LLM01)

Este repositório contém o laboratório prático de cibersegurança em Inteligência Artificial focado em **Prompt Injection Direct** e implementação de **Defesa em Profundidade (*Defense in Depth*)**.

---
## 🎯 Objetivo do Laboratório
Demonstrar na prática como um ataque de *Prompt Injection* pode manipular o comportamento de uma LLM (Large Language Model) para vazar informações confidenciais corporativas e como implementar camadas defensivas com *Guardrails* em Python para mitigar esse risco.
---
## 🧪 Estrutura da Atividade

### 🔴 Red Team (Ataque)
* **Conceito:** Exploração da vulnerabilidade **OWASP LLM01**, onde a entrada do usuário é concatenada diretamente com a instrução do sistema (*System Prompt*).
* **Desafio:** Utilizar técnicas de *Jailbreak*, *Roleplay* (Engenharia Social) e comandos de autoridade (*Override*) para fazer a IA esquecer suas regras internas e vazar o código confidencial da diretoria (`SUPER_SECRET_2026_OFF`).

### 🔵 Blue Team (Defesa)
* **Conceito:** Aplicação do princípio de *Defense in Depth* (nunca confiar apenas no System Prompt da IA).
* **Solução:** Implementação de uma barreira de segurança na saída (*Output Guardrail*) em código Python que inspeciona a resposta antes de exibi-la ao usuário, bloqueando qualquer tentativa de vazamento de dados sensíveis.
---
## 🚀 Como Executar no Google Colab

1. Acesse o notebook do laboratório clicando em [`PROMPT INJECTION.ipynb`](./PROMPT%20INJECTION.ipynb) ou abra diretamente pelo Google Colab.
2. Certifique-se de ativar a GPU T4:
   * Menu: `Ambiente de Execução` ➔ `Alterar tipo de ambiente de execução` ➔ `Acelerador de Hardware: GPU T4`.
3. Execute as células em sequência para carregar o modelo `TinyLlama/TinyLlama-1.1B-Chat-v1.0`.
4. Faça as missões práticas de **Red Team** e **Blue Team** indicadas no notebook.
---
## 🧰 Tecnologias Utilizadas
* **Ambiente:** Google Colab (GPU T4)
* **Linguagem:** Python 3.10+
* **Frameworks:** Hugging Face `transformers`, `torch`
* **Modelo LLM:** `TinyLlama/TinyLlama-1.1B-Chat-v1.0`
