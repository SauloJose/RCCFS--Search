[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Communications**, que propõe o algoritmo **UMAP** (UAV Movement control, MU Association and MU Power control) baseado em DRL para alocação de recursos em redes MEC assistidas por múltiplos UAVs, com validação por simulação em dataset real.

---

### 📌 Metadados do Artigo
*   **Título:** Deep Reinforcement Learning Based Resource Allocation in Multi-UAV-Aided MEC Networks
*   **DOI:** 10.1109/TCOMM.2022.3226193
*   **Publicação (Veículo/Evento):** IEEE Transactions on Communications
*   **Ano:** 2023

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (com dataset real)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** M UAVs atuando como estações base aéreas em altura fixa H, auxiliando uma estação base terrestre a fornecer acesso rádio e serviço de computação para N usuários móveis (MUs). Os UAVs são similares entre si.

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
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Cellular |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é composto por M UAVs e uma estação base terrestre que cooperam para fornecer serviços de comunicação e computação a N usuários móveis. Os UAVs voam a uma altura fixa H e se movem em intervalos de tempo discretos, ajustando posição e ângulo de guinada. Os MUs descarregam tarefas para os UAVs ou para a BS via enlaces sem fio, e o processamento ocorre nos UAVs/BS. O problema conjunto de controle de movimento dos UAVs, associação de MUs e alocação de potência de transmissão é formulado como um problema de programação não convexa inteira mista em série temporal. O algoritmo UMAP decompõe o problema em três subproblemas otimizados iterativamente: controle de movimento dos UAVs via DDPG, associação de MUs via DQN e controle de potência de transmissão dos MUs com solução em forma fechada. O processamento é híbrido (UAVs e BS) e a execução das decisões ocorre online.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de alocação de recursos em redes MEC assistidas por múltiplos UAVs, considerando um cenário de comunicação uplink. Formula um problema de programação não convexa inteira mista em série temporal para minimizar a latência total do sistema e o consumo de energia, sujeito a restrições de potência de transmissão dos MUs e de latência causada por transmissão e computação. Propõe o algoritmo UMAP, que decompõe o problema em três subproblemas: controle de movimento dos UAVs usando DDPG, associação de MUs usando DQN e controle de potência de transmissão dos MUs com solução em forma fechada. Os subproblemas são otimizados iterativamente até a convergência. Resultados de simulação em dataset real mostram que o UMAP reduz significativamente a latência do sistema e o consumo de energia, além de aumentar a taxa de cobertura em comparação com algoritmos de referência.