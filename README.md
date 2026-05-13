# ⚡ GoodWe ChargeGrid AI

## 📝 Descrição do Projeto

O GoodWe ChargeGrid AI é um chatbot operacional baseado em Inteligência Artificial desenvolvido para a Sprint 1 do EV Challenge 2026.

O projeto tem como objetivo auxiliar operadores comerciais no gerenciamento de eletropostos, oferecendo suporte rápido e contextualizado sobre consumo energético, status de carregadores, potência utilizada, ciclos de recarga e alertas operacionais.

A proposta busca melhorar a eficiência operacional dos eletropostos e facilitar a tomada de decisão através de um assistente inteligente integrado ao contexto da GoodWe.

---

# 👥 Integrantes do Grupo

* Pedro Ribeiro Lopes — RM: 570083
* Lucas Furquim Lima — RM: 568690
* Gustavo Torres de Oliveira — RM: 572952
* Rafael Laprega Gontijo Magalhães — RM: 561975
* Diogo Chiaradia Santos — RM: 570246

---

# 🚩 Problema Abordado

Operadores comerciais de eletropostos enfrentam desafios relacionados ao monitoramento e gerenciamento da infraestrutura de carregamento elétrico.

Entre os principais problemas estão:

* Falta de monitoramento eficiente do consumo energético
* Dificuldade em acompanhar ciclos de recarga
* Controle limitado da potência utilizada
* Lentidão na identificação de falhas operacionais
* Dificuldade na gestão de faturamento e utilização dos carregadores

Esses problemas podem gerar atrasos operacionais, desperdício energético e dificuldades administrativas.

---

# 🤖 Proposta do Chatbot

O chatbot atua como um assistente operacional inteligente voltado para operadores comerciais da GoodWe.

Suas principais funções são:

* Informar o status dos carregadores
* Auxiliar no monitoramento energético
* Identificar alertas operacionais
* Fornecer suporte contextualizado sobre eletropostos
* Auxiliar no acompanhamento de ciclos de recarga
* Apoiar processos operacionais e administrativos

O sistema foi projetado para responder apenas perguntas relacionadas ao contexto operacional dos eletropostos.

---

# 👤 Persona Principal

## Operador Comercial

Responsável pelo gerenciamento operacional dos eletropostos, monitoramento energético, acompanhamento de recargas e suporte administrativo.

---

# 🛠️ Tecnologias Selecionadas

| Tecnologia   | Função                        |
| ------------ | ----------------------------- |
| Llama 3.2 1B | Modelo de IA                  |
| Ollama       | Execução local do modelo      |
| Python 3.10  | Desenvolvimento da aplicação  |
| GitHub       | Versionamento do projeto      |
| Draw.io      | Desenvolvimento do fluxograma |

---

# ⚖️ Justificativa Técnica

As tecnologias escolhidas foram selecionadas considerando simplicidade, baixo custo e facilidade de implementação durante o desenvolvimento do protótipo.

O modelo Llama 3.2 1B foi utilizado por ser leve e permitir execução local através do Ollama, eliminando dependência de APIs externas.

A utilização local também melhora a privacidade dos dados operacionais e reduz latência de resposta.

O Python foi escolhido devido à facilidade de integração com IA e desenvolvimento rápido de protótipos.

---

# 🔄 Fluxo de Funcionamento do Chatbot

1. O operador comercial envia uma pergunta ao chatbot
2. O sistema recebe a solicitação
3. O prompt de contexto operacional é enviado ao modelo de IA
4. O modelo processa a solicitação
5. O chatbot retorna uma resposta contextualizada ao operador

---

# 🧪 Modelo de Teste

| Pergunta                                      | Tipo             |
| --------------------------------------------- | ---------------- |
| O carregador 04 está funcionando normalmente? | Dentro do escopo |
| Existe risco de sobrecarga energética?        | Dentro do escopo |
| Há alertas operacionais ativos no sistema?    | Dentro do escopo |
| Quem ganhou a Copa do Mundo de 2022?          | Fora do escopo   |
| Como fazer lasanha?                           | Fora do escopo   |

---

# 🧠 System Prompt

```python
MEU_SYSTEM_PROMPT = """
Você é um assistente operacional da GoodWe especializado em gerenciamento de eletropostos e carregamento de veículos elétricos.

Seu objetivo é auxiliar operadores comerciais fornecendo respostas claras e objetivas sobre:
- status de carregadores
- consumo energético
- potência utilizada
- ciclos de recarga
- faturamento
- alertas operacionais

REGRAS:
- Responda apenas assuntos relacionados a eletropostos e carregamento elétrico.
- Caso a pergunta esteja fora do escopo, responda:
'Desculpe, só posso ajudar com informações operacionais dos eletropostos GoodWe.'
- Nunca invente informações externas ao contexto operacional.
- Mantenha respostas curtas e diretas.

TOM:
- Profissional
- Técnico
- Objetivo
- Português do Brasil
"""
```

---
