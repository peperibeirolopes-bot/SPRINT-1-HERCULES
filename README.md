# SPRINT-1-HERCULES

# ⚡ GoodWe ChargeGrid Intelligence Assistant
**Projeto EV Challenge 2026 | FIAP & GoodWe**

## 👥 Integrantes
* **Pedro Ribeiro Lopes** — RM: 570083
* **Lucas Furquim Lima** — RM: 568690
* **Gustavo Torres de Oliveira** — RM: 572952
* **Rafael Laprega Gontijo Magalhães** — RM: 561975
* **Diogo Chiaradia Santos** — RM: 570246

---

## 🎯 1. Problema Abordado
No cenário de eletropostos comerciais e frotas de veículos elétricos (EVs), existe uma lacuna crítica na integração de dados. Atualmente, os eletropostos carecem de sistemas que consigam:
1. **Orquestrar Potência:** Gerenciar o fluxo de energia para não ultrapassar a demanda contratada.
2. **Registrar Ciclos:** Documentar o desgaste e uso das baterias e carregadores.
3. **Faturamento:** Automatizar a cobrança baseada em consumo real e tarifas dinâmicas.

A ausência dessa inteligência gera multas por picos de demanda (Peak Shaving) e falhas na comunicação técnica com o operador.

## 🤖 2. Proposta do Chatbot
O **ChargeGrid Intelligence Assistant** é um chatbot operacional desenvolvido para ser o braço direito do **Operador Comercial de Eletropostos**. Diferente de um chatbot genérico, ele é uma ferramenta de monitoramento e decisão que processa logs técnicos dos inversores GoodWe para oferecer insights sobre faturamento, balanceamento de carga e alertas de segurança em tempo real.

**Justificativa do Escopo (Comercial):** Escolhemos o contexto comercial devido à complexidade técnica da orquestração de potência em larga escala, que exige uma resposta computacional precisa para evitar prejuízos financeiros e danos à rede elétrica.

## 🛠 3. Tecnologias Selecionadas
* **LLM:** Llama 3.2 (via Ollama).
* **Justificativa Técnica:** O processamento local garante a **soberania dos dados** operacionais e financeiros da GoodWe, reduzindo a latência em decisões críticas de carga e eliminando custos variáveis de APIs de terceiros.
* **Backend:** Python para integração de logs e LangChain para gestão de contexto (RAG).

---

## 🧠 4. Contexto-Base (System Prompt)
Este prompt será utilizado para condicionar a IA na Sprint 2:

> "Você é o 'ChargeGrid Operator AI', uma inteligência operacional integrada ao ecossistema GoodWe. Sua persona é de um engenheiro de sistemas: direto, técnico e focado em segurança. Seu objetivo é auxiliar o gestor do eletroposto a manter a rede estável e o faturamento preciso. Priorize sempre o 'Peak Shaving' (redução de pico). Se os dados indicarem carga acima de 90%, emita um alerta imediato. Utilize terminologia técnica (SOC, kW, Harmônicas, Protocolo OCPP) e seja rigoroso com as normas de segurança elétrica."

---

## 📝 5. Modelo de Teste (Validação)
| Pergunta Esperada | Resposta Ideal (Comportamento Desejado) |
| :--- | :--- |
| "Qual o consumo total do grid agora?" | "O grid opera com 142kW. Estamos operando dentro da margem de 150kW contratados." |
| "Algum alerta de segurança nas estações?" | "A Estação 02 reportou alta temperatura no conector. Recomendo redução de carga para 7kW imediatamente." |
| "Quanto foi faturado no carregador 05 hoje?" | "O carregador 05 registrou 12 ciclos (480kWh), totalizando R$ 816,00 em faturamento." |
| "O que fazer se a demanda bater o limite?" | "Inicie o protocolo de Peak Shaving: reduza a potência das estações de carga lenta e priorize frotas de saída imediata." |
| "Como está a eficiência do inversor da Estação 1?" | "Eficiência atual de 94.2%. Níveis de distorção harmônica dentro dos padrões GoodWe." |
