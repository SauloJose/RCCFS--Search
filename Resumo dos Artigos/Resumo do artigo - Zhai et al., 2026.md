[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Intelligent Transportation Systems**, que propõe o método **DPDTS** (DNN Partitioning and Dynamic Trajectory Selection) baseado em aprendizado por reforço profundo para offloading de tarefas com inferência colaborativa de DNNs em redes MEC assistidas por múltiplos UAVs, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Deep Reinforcement Learning-Based Task Offloading With Collaborative Inference in UAV-Assisted Mobile Edge Computing Networks
*   **DOI:** 10.1109/TITS.2025.3629117
*   **Publicação (Veículo/Evento):** IEEE Transactions on Intelligent Transportation Systems
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** K UAVs equipados com servidores de computação de borda, voando a altitude constante H e atendendo M usuários terrestres (GUs). Os UAVs circulam no ar e alocam recursos cooperativamente; são similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (DRL multiagente com UAVs como agentes) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Outro (TDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é uma rede MEC multi-UAV na qual cada GU gera tarefas de inferência de DNN que podem ser executadas localmente ou parcialmente descarregadas para um UAV, usando **inferência colaborativa**: a DNN é particionada em uma parte frontal executada no dispositivo e uma parte traseira executada no UAV, transmitindo apenas o resultado intermediário, menor que a entrada original. O problema conjunto de ponto de partição ótimo da DNN, trajetória dos UAVs, alocação de recursos computacionais, potência de transmissão dos GUs e decisão de offloading é formulado como um problema de otimização não convexo com restrições de cobertura, velocidade, potência, capacidade energética e número máximo de usuários por UAV. A solução usa um framework de otimização alternada com três subproblemas: **OPPS** (Optimal Partition Point Selection) para escolher o ponto de partição ótimo por tarefa; um **algoritmo de matching baseado em fairness** para associar GUs a UAVs e alocar recursos computacionais; e um **algoritmo DRL** que integra OPPS e matching para otimizar trajetórias e potência de transmissão, com os UAVs como agentes. O processamento é híbrido (dispositivo e UAV) e a comunicação é explícita via TDMA.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas de DNN em redes MEC assistidas por múltiplos UAVs, no qual o grande volume de dados e a complexidade computacional das DNNs tornam inviáveis abordagens de offloading total, local ou particionamento arbitrário. Propõe o método DPDTS, que combina inferência colaborativa com decisões de offloading e trajetória. O algoritmo OPPS seleciona o ponto de partição ótimo de cada DNN com base na hierarquia de camadas e na capacidade de borda do UAV, minimizando o custo ponderado de latência e energia. Um algoritmo de matching baseado em fairness otimiza a associação GU-UAV e a alocação de recursos computacionais. Por fim, um algoritmo DRL integra OPPS e matching para otimizar trajetórias dos UAVs e potência de transmissão dos GUs em ambientes dinâmicos. Simulações mostram que o DPDTS supera benchmarks em latência e eficiência energética.