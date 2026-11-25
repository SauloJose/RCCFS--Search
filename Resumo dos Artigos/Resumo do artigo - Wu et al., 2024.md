[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Vehicular Technology**, que investiga offloading de tarefas e alocação de recursos em uma rede MEC multi-UAV e multi-servidor, propondo a abordagem **DDPG-MHSA** com actor-critic baseado em multi-head self-attention, validada por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Joint Task Offloading and Resource Allocation in Multi-UAV Multi-Server Systems: An Attention-Based Deep Reinforcement Learning Approach
*   **DOI:** 10.1109/TVT.2024.3377647
*   **Publicação (Veículo/Evento):** IEEE Transactions on Vehicular Technology
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs com tarefas computacionais que podem ser executadas localmente ou descarregadas para M servidores MEC. A rede é composta por N UAVs e M servidores MEC; os UAVs são similares entre si, e a heterogeneidade está nos recursos dos servidores, não na frota robótica.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (OFDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede é uma MEC multi-UAV multi-servidor na qual cada UAV possui uma tarefa computacional que pode ser executada localmente ou descarregada para um dos M servidores MEC. O problema conjunto de decisão de offloading e alocação de recursos (frequência de CPU, largura de banda, potência de transmissão uplink e downlink) é formulado como um MDP de longo prazo com espaço de ações híbrido discreto-contínuo. A abordagem DDPG-MHSA usa um actor-critic com multi-head self-attention e estrutura encoder-decoder, treinado por DDPG; parte das ações contínuas é mapeada para decisões discretas de offloading via argmax. A comunicação UAV-servidor usa OFDMA, com canais ortogonais e interferência desprezada. O processamento é híbrido (local nos UAVs e nos servidores MEC), e a execução das decisões ocorre online.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de otimização de longo prazo para offloading de tarefas e alocação de recursos em uma rede MEC multi-UAV e multi-servidor (JTORA-MUMS), com o objetivo de minimizar a soma ponderada de atraso e consumo de energia dos UAVs. Formula o problema como um MDP com espaço de ações híbrido discreto-contínuo, no qual o offloading é discreto e a alocação de CPU, largura de banda e potências de transmissão é contínua. Propõe o método DDPG-MHSA, que combina DDPG com uma rede actor-critic baseada em multi-head self-attention e estrutura encoder-decoder, permitindo generalização para diferentes números de UAVs e diferentes atributos de tarefas sem treinamento adicional. Experimentos extensivos mostram que o DDPG-MHSA supera métodos DRL do estado da arte e heurísticas convencionais, com boa generalização para variações no número de UAVs e nas propriedades das tarefas.