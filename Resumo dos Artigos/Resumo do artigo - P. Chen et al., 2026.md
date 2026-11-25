[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Wireless Communications**, que propõe um esquema de offloading de tarefas orientado a QoS em sistemas MEC cooperativos multi-UAV baseados em NOMA, com prioridade de tarefas, otimização conjunta de trajetórias 3D, associação, razões de offloading e alocação de recursos, resolvido por um algoritmo DRL aprimorado (ISAC) e validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** QoS-Oriented Task Offloading in NOMA-Based Multi-UAV Cooperative MEC Systems
*   **DOI:** 10.1109/TWC.2025.3593884
*   **Publicação (Veículo/Evento):** IEEE Transactions on Wireless Communications
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs (L UAVs) equipados com servidores de computação de borda, atuando de forma cooperativa para atender K usuários móveis (MUs) em uma área de serviço. O número exato de UAVs não é fixado no modelo; a frota é composta por UAVs similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (NOMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é um MEC cooperativo multi-UAV baseado em NOMA, no qual múltiplos MUs geram tarefas com diferentes prioridades e podem executá-las localmente ou descarregá-las para UAVs equipados com servidores de borda. Os MUs usam mensagens beacon (ping-ACK) para descobrir UAVs próximos, e um controlador central agrega as informações de beacon e constrói o estado global do sistema, selecionando o UAV mais adequado para cada offloading. A transmissão uplink usa NOMA com SIC no UAV. O problema conjunto de trajetórias 3D dos UAVs, associação MU-UAV, razões de offloading e alocação de recursos é formulado como um MDP e resolvido com dualidade de Lagrange e o algoritmo ISAC (Improved Soft Actor-Critic). O processamento é híbrido: parte local nos MUs e parte nos UAVs (borda aérea).

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas orientado a QoS em sistemas MEC cooperativos multi-UAV com NOMA, considerando explicitamente prioridades de tarefas e requisitos de atraso. Formula um problema de maximização da utilidade média do sistema por meio da otimização conjunta de trajetórias 3D dos UAVs, associação dos MUs, razões de offloading e alocação de recursos, sob restrições de mobilidade, capacidade computacional e deadlines. Para lidar com a não convexidade, aplica dualidade de Lagrange para desacoplar restrições e propõe o algoritmo ISAC, que introduz um termo de perturbação na função de perda para evitar mínimos locais. Simulações demonstram convergência e desempenho superior ao SAC, PPO e DDPG em taxa de transmissão de offloading, taxa de conclusão de tarefas e utilidade global do sistema.