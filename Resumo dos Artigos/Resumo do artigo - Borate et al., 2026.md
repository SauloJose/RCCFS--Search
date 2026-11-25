[[Atv1 - Parte 4 - Entrega Final]]


**O que é:** Artigo científico do tipo **Solution**, publicado na **Frontiers in Robotics and AI**, que propõe o framework **CoMuRoS**, uma arquitetura hierárquica baseada em LLM para planejamento e execução de tarefas por equipes heterogêneas de robôs, com replanejamento orientado a eventos, validado por experimentos de hardware e simulação.

---

### 📌 Metadados do Artigo
*   **Título:** CoMuRoS - An LLM-based generalizable hierarchical task planning and execution framework for heterogeneous robot teams with event-driven re-planning
*   **DOI:** 10.3389/frobt.2026.1843313
*   **Publicação (Veículo/Evento):** Frontiers in Robotics and AI
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Testbed/Real-world; Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Equipes heterogêneas de robôs, incluindo quadrúpedes, humanoides e drones, com diferentes capacidades, morfologias e restrições. O benchmark avalia cerca de 20 robôs em 22 cenários e 54 tarefas; os experimentos de hardware incluem recuperação colaborativa de objetos, transporte coordenado e recuperação assistida por humano.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Não especificado |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS 2 |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O CoMuRoS adota uma arquitetura hierárquica inspirada em organizações humanas. Um **task manager LLM centralizado** interpreta instruções em linguagem natural, classifica tarefas (independentes, sequenciais, coordenadas ou inviáveis), aloca tarefas conforme capacidades e restrições dos robôs e replaneja quando eventos relevantes são reportados. Cada robô possui um **LLM local descentralizado** que gera código Python executável a partir de habilidades primitivas ROS 2, além de um executor de baixo nível e um módulo de detecção/classificação de eventos com VLM/percepção. A comunicação é bidirecional: o gerente envia especificações de alto nível e os robôs retornam status e eventos. O replanejamento é acionado por eventos relevantes, permitindo recuperação colaborativa e cooperação humano-robô.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de equipes heterogêneas de robôs interpretarem instruções em linguagem natural, alocarem tarefas conforme capacidades e se adaptarem a eventos inesperados em ambientes dinâmicos. Propõe o CoMuRoS, uma arquitetura hierárquica que combina um LLM gerente centralizado com LLMs locais nos robôs para gerar planos executáveis a partir de habilidades ROS 2, usando regras estáticas de planejamento e contexto dinâmico (histórico, status, eventos detectados). A percepção embarcada com VLM classifica eventos como relevantes ou irrelevantes e dispara replanejamento. Experimentos de hardware demonstram recuperação de eventos disruptivos, filtragem de distrações e transporte coordenado com cooperação humano-robô emergente, com taxas de sucesso de 9/10, 8/8 e 5/5 em diferentes cenários. Estudos de simulação e um benchmark de 22 cenários, 54 tarefas e cerca de 20 robôs avaliam alocação, classificação, IoU, executabilidade e correção, atingindo correção de até 0,91 ± 0,053 e 0,948 ± 0,034 no benchmark de replanejamento.