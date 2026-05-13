# 📝 Descrição do Projeto
O ChargeGrid Intelligence é um assistente operacional baseado em Inteligência Artificial desenvolvido para a Sprint 1 do EV Challenge 2026. O projeto foca em resolver os desafios de infraestrutura e gestão financeira em eletropostos comerciais, garantindo que a operação de recarga seja eficiente, segura e lucrativa para o gestor.

# 👥 Integrantes do Grupo

Pedro Ribeiro Lopes — RM: 570083

Lucas Furquim Lima — RM: 568690

Gustavo Torres de Oliveira — RM: 572952

Rafael Laprega Gontijo Magalhães — RM: 561975

Diogo Chiaradia Santos — RM: 570246

# 🚩 Problema Abordado

Operadores de eletropostos comerciais enfrentam três dificuldades críticas:

Multas por Excesso de Demanda: A falta de controle em tempo real faz com que o consumo do pátio ultrapasse a demanda contratada com a concessionária.

Complexidade de Faturamento: Dificuldade em consolidar dados de múltiplos ciclos de carga para faturamento preciso de frotas e usuários.

Segurança Operacional: Atrasos na identificação de anomalias técnicas (temperatura e falhas de protocolo) que podem danificar equipamentos caros.

# 🤖 Proposta do Chatbot

O chatbot assume a persona de um Engenheiro de Sistemas (ChargeGrid Operator AI). Suas principais funções são:

Orquestração de Potência: Monitorar o consumo e aplicar protocolos de Peak Shaving automaticamente.

Assistente de Manutenção: Interpretar códigos de erro (Protocolo OCPP) e emitir alertas de segurança.

Gestão Comercial: Calcular rapidamente o faturamento e ciclos de energia (kWh) processados por cada estação.

Rigor de Escopo: O sistema ignora qualquer solicitação não técnica (como lazer ou assuntos gerais), mantendo o foco estritamente na operação do eletroposto.

# 🛠️ Tecnologias Selecionadas

LLM (Large Language Model): Llama 3.2 1b.

Engine de Execução: Ollama (Local).

Linguagem: Python 3.10.

# ⚖️ Justificativa Técnica

A escolha dessas tecnologias baseia-se em três pilares:

Soberania e Privacidade de Dados: Como o chatbot lida com dados de faturamento e infraestrutura crítica da empresa, o uso de um modelo local (Ollama) evita o envio de informações sensíveis para nuvens de terceiros.

Custo-Benefício: O modelo Llama 3.2 1b é extremamente leve, permitindo que a solução rode em hardware modesto (como um servidor local no eletroposto) sem a necessidade de GPUs de alto custo ou assinaturas mensais de APIs.

Latência Reduzida: Para decisões de segurança elétrica e alertas de Peak Shaving, a resposta precisa ser imediata. A execução local elimina o atraso de rede (latência de internet), garantindo agilidade operacional.
