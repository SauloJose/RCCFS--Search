[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **Knowledge-Based Systems** (Elsevier), que propõe o metaheurístico **Bounty Hunter Optimizer (BHO)** e o aplica a um sistema **multi-UAV MEC-PP** (computação de borda móvel e planejamento de caminho) com restrições de QoS, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Bounty hunter optimizer: A novel metaheuristic with an application to multi-UAV mobile edge computing and path planning
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** Knowledge-Based Systems (Elsevier), Vol. 341, 2026, artigo 115836
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs homogêneos atuando como nós de borda aérea em um sistema MEC, com número variável conforme a escala dos cenários simulados. Os UAVs executam tarefas de computação e têm suas trajetórias planejadas conjuntamente sob restrições de QoS.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Edge-Fog |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Offline |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Não especificado |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O BHO é usado como otimizador centralizado para o planejamento conjunto de trajetórias e alocação de tarefas/recursos em um sistema multi-UAV MEC-PP com restrições explícitas de QoS. Os UAVs são nós de borda aérea que fornecem capacidade de computação e conectividade sem fio; o artigo não detalha pilha de comunicação, middleware ou topologia específica. Internamente, o BHO usa atualizações descentralizadas de posição, filtragem Explorpolis e seleção por rotação de probabilidade quântica (QPRS), mas isso se refere ao mecanismo populacional do algoritmo, não a uma arquitetura descentralizada da frota. A otimização é conduzida por metaheurística e avaliada por simulação em diferentes escalas.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo propõe o Bounty Hunter Optimizer (BHO), um novo algoritmo metaheurístico inspirado no comportamento de caçadores de recompensas, com três mecanismos principais: regra Explorpolis para filtrar soluções inferiores, seleção por rotação de probabilidade quântica (QPRS) para substituir a roleta e um modelo evolutivo com busca minuciosa, busca grosseira e realocação de caçadores. O BHO é avaliado no conjunto CEC2017 em 30D e 100D, superando 11 algoritmos avançados. Em seguida, é aplicado a um modelo multi-UAV MEC-PP com restrições de QoS, no qual se busca minimizar o custo total do sistema por meio do planejamento conjunto de caminhos e decisões de computação. Simulações em diferentes escalas mostram redução de custo superior a 15% em relação a concorrentes avançados, com convergência mais estável em cenários altamente restritos.