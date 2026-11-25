[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Cloud Computing**, que propõe um framework distribuído de atribuição de tarefas para sistemas de computação de borda cooperativa multi-UAV, com o algoritmo **MA²DDPG** (Multi-head self-Attention critic-assisted MADDPG) para controle conjunto de trajetória e atribuição de tarefas, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Multi-Agent Deep Reinforcement Learning-Based Distributed Task Assignment in Multi-UAV Cooperative Edge Computing
*   **DOI:** 10.1109/TCC.2026.3668236
*   **Publicação (Veículo/Evento):** IEEE Transactions on Cloud Computing
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Enxame de M UAVs equipados com servidores de borda, atuando como nós aéreos de computação, mais uma estação base (BS) terrestre com recursos abundantes e dispositivos de usuário (UDs) distribuídos em áreas de hotspot. Os UAVs são similares entre si e voam a altitude fixa H.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (CTDE: treinamento centralizado, execução descentralizada) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é uma rede de computação de borda cooperativa multi-UAV composta por um enxame de UAVs, uma estação base terrestre e dispositivos de usuário. Os UAVs atuam como nós aéreos de borda, estendendo a cobertura da BS e agregando tarefas heterogêneas em áreas de hotspot. Cada UAV toma decisões distribuídas com base apenas em observações locais, considerando explicitamente a cooperação horizontal com outros UAVs e a cooperação vertical com a BS. O problema conjunto de controle de trajetória e atribuição de tarefas é formulado como um **dec-POMDP**, no qual cada UAV é um agente independente. A solução usa o algoritmo **MA²DDPG**, que segue o paradigma CTDE com um **Critic centralizado** compartilhado entre todos os UAVs (reduzindo redundância de parâmetros) e um mecanismo de **multi-head self-attention (MHSA)** no Critic para capturar dependências cooperativas implícitas e mitigar a maldição da dimensionalidade à medida que o número de UAVs cresce. Os atores são redes locais que executam decisões distribuídas online. A comunicação entre UAVs e BS ocorre via rede core sem fio, com enlaces LoS e modelo de perda log-distance. O processamento é híbrido (UAVs e BS).

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de atribuição distribuída de tarefas em sistemas de computação de borda cooperativa multi-UAV, nos quais restrições de recursos embarcados impedem que um único UAV processe grandes volumes de tarefas heterogêneas em tempo real. Diferentemente de trabalhos anteriores que focam apenas na cooperação vertical entre UAVs e dispositivos/cloud, o artigo incorpora cooperação horizontal intra-enxame, permitindo que cada UAV atribua dinamicamente parte de suas tarefas locais a outros UAVs ou à BS, enquanto controla sua trajetória para melhorar a qualidade dos enlaces. O problema conjunto é formulado como um dec-POMDP com o objetivo de minimizar a latência total acumulada de conclusão de tarefas ao longo do horizonte. Propõe o algoritmo MA²DDPG, que utiliza CTDE com um Critic centralizado e MHSA para capturar dependências cooperativas e melhorar a escalabilidade em enxames grandes. Simulações extensas, variando o número de UAVs e a largura de banda, mostram que a abordagem supera baselines em latência total do sistema, utilização de recursos computacionais e consumo total de energia.