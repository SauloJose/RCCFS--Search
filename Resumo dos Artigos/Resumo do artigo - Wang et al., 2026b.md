[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Internet of Things Journal**, que investiga uma arquitetura MEC cooperativa ar-solo com múltiplos UAVs e edge servers (ESs) terrestres, formulando um problema multiobjetivo de otimização conjunta de offloading de tarefas, alocação de recursos e trajetórias dos UAVs, resolvido pelo framework **JAOTRU** (Joint Alternating Optimization for Task offloading, Resource allocation, and UAV trajectory control), validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Joint Optimization of Task Offloading, Resource Allocation, and Trajectory Design in Cooperative Multi-UAV MEC Networks
*   **DOI:** 10.1109/JIOT.2026.3673398
*   **Publicação (Veículo/Evento):** IEEE Internet of Things Journal
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs rotativos (I UAVs) equipados com módulos de computação e comunicação, atuando como edge servers aéreos, em cooperação com E edge servers terrestres fixos, para atender M usuários móveis. Os UAVs são similares entre si; a heterogeneidade está na coexistência de UAVs e ESs terrestres com capacidades distintas.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (OFDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede é uma MEC cooperativa ar-solo composta por múltiplos UAVs, edge servers terrestres fixos e usuários móveis. Os usuários podem descarregar tarefas para o UAV atual, para outro UAV via enlace A2A, para o ES atual ou para outro ES, caracterizando cooperação UAV-UAV e ES-ES. O sistema considera três modos de transmissão: G2A (usuário-UAV), A2A (UAV-UAV) e G2G (usuário-ES). O problema conjunto de decisão de offloading, alocação de recursos computacionais e controle de trajetória dos UAVs é formulado como um MINLP NP-hard multiobjetivo, com o objetivo de minimizar simultaneamente a latência total de offloading e o consumo total de energia do sistema. A solução JAOTRU adota uma estrutura iterativa de **Block Coordinate Descent (BCD)** que decompõe o problema em dois subproblemas: (i) offloading de tarefas e alocação de recursos, resolvido por **Differential Evolution (DE)**; e (ii) otimização de trajetória dos UAVs, resolvido por **Successive Convex Approximation (SCA)**. O processamento é híbrido (UAVs e ESs) e a execução das decisões é centralizada, com os operadores de rede móvel coletando informações de usuários e UAVs para determinar as decisões.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de distribuição espacial não uniforme de usuários em sistemas MEC assistidos por UAVs, no qual estratégias de implantação fixas ou predeterminadas não se adaptam a distribuições heterogêneas. Propõe uma arquitetura MEC cooperativa ar-solo com múltiplos UAVs e edge servers terrestres, na qual tarefas podem ser processadas cooperativamente por UAVs e ESs, aliviando limitações de capacidade computacional e cobertura de UAVs individuais. Formula um problema multiobjetivo para minimizar a latência total de offloading e o consumo total de energia do sistema, considerando restrições de QoS, energia dos UAVs, dinâmica de comunicação com small-scale fading, path loss e shadowing. Como o problema é um MINLP NP-hard, desenvolve o framework JAOTRU, que usa BCD para decompor o problema em dois subproblemas resolvidos por DE e SCA. Simulações mostram que o JAOTRU supera benchmarks em latência total de offloading, consumo de energia e valor objetivo global, validando sua eficácia e robustez para sistemas MEC assistidos por UAVs.