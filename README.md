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

Seu objetivo é auxiliar operadores comerciais fornecendo respostas claras, rápidas e contextualizadas sobre:

- status de carregadores
- consumo energético
- potência utilizada
- ciclos de recarga
- faturamento
- alertas operacionais

Responda sempre de maneira profissional, objetiva e técnica.

Caso não possua determinada informação, informe isso claramente e sugira uma ação apropriada.


TOM:
- Profissional
- Curto
- Claro
- Em português do Brasil
"""
```
## SPRINT2

# 🚀 Instalação e Execução

## Pré-requisitos

Antes de executar o projeto, é necessário possuir:

- Python 3.10+
- Ollama instalado
- Google Colab (ou IDE Python)
- Modelo Llama 3.2:1b

---

## Instalação das dependências

Instale as bibliotecas necessárias:

```bash
pip install ollama
pip install ipywidgets
```

Caso esteja utilizando Google Colab:

```python
!pip install ollama -q
!apt-get install -y zstd -q
```

---

## Instalação do Ollama

Instale o servidor Ollama:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

Inicie o servidor:

```bash
ollama serve
```

Baixe o modelo utilizado:

```bash
ollama pull llama3.2:1b
```

---

# 🔐 Variáveis de Ambiente

Neste projeto não foi utilizada API Key, pois o modelo foi executado localmente via Ollama.

Mesmo assim, seguindo boas práticas, caso APIs externas sejam utilizadas futuramente, recomenda-se armazenar credenciais através de:

- Variáveis de ambiente
- Google Colab Secrets

Exemplo:

```python
import os

API_KEY = os.getenv("API_KEY")
```

---

# ▶ Como Executar

Após instalar as dependências:

Execute o notebook ou script Python:

```bash
python chatbot.py
```

ou execute diretamente no Google Colab.

O chatbot iniciará:

```text
==================================================
CHATBOT GOODWE
Digite sair para encerrar
==================================================
```

---

# 💬 Exemplos de Uso

Exemplos de perguntas dentro do escopo:

```text
Qual é o status do carregador 04?
```

```text
Existe risco de sobrecarga energética?
```

```text
Há alertas operacionais ativos?
```

```text
Qual carregador está consumindo mais energia?
```

---

Exemplo de uso do histórico:

```text
Meu nome é Pedro e sou operador comercial de um eletroposto.
```

Depois:

```text
Qual carregador nós estávamos discutindo?
```

O chatbot utiliza histórico de mensagens para manter contexto e gerar respostas contínuas.

---

Exemplos fora do escopo:

```text
Quem ganhou a Copa do Mundo de 2022?
```

```text
Como fazer lasanha?
```

Durante os testes, observou-se que perguntas fora do contexto podem gerar respostas inconsistentes devido às limitações do modelo.
