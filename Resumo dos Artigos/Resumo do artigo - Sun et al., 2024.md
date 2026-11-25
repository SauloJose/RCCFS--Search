[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Mobile Computing**, que propõe o algoritmo **JTORATC** (Joint Task Offloading, Resource Allocation and Trajectory Control) para otimização multiobjetivo em sistemas MEC assistidos por múltiplos UAVs, com validação por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Multi-Objective Optimization for Multi-UAV-Assisted Mobile Edge Computing
*   **DOI:** 10.1109/TMC.2024.3446819
*   **Publicação (Veículo/Evento):** IEEE Transactions on Mobile Computing
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** M UAVs rotativos equipados com um ou múltiplos servidores MEC, servindo U usuários. Os UAVs são similares entre si e voam a uma altitude constante H.

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
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é uma rede MEC assistida por múltiplos UAVs, na qual cada UAV é equipado com servidores MEC e se move em espaço 3D para atender usuários no solo. Os usuários podem executar tarefas localmente ou descarregá-las para os UAVs. O problema multiobjetivo de minimizar o atraso total de conclusão das tarefas, reduzir o consumo total de energia dos UAVs e maximizar o número total de tarefas descarregadas é formulado como um MINLP NP-hard. A abordagem JTORATC transforma o problema multiobjetivo em um problema mono-objetivo por ponderação linear e o decompõe em três subproblemas: offloading de tarefas, resolvido por splitting distribuído e arredondamento com limiar; alocação de recursos computacionais, resolvido por KKT; e controle de trajetória dos UAVs, resolvido por SCA. O processamento é híbrido (local e nos UAVs) e a comunicação é explícita.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de otimização multiobjetivo em sistemas MEC assistidos por múltiplos UAVs, considerando requisitos de baixa latência, limitações de energia dos UAVs e qualidade de experiência dos usuários. Formula um problema que busca simultaneamente minimizar o atraso total de conclusão das tarefas, reduzir o consumo total de energia dos UAVs e maximizar o número total de tarefas descarregadas, otimizando decisões de offloading, alocação de recursos computacionais e trajetórias dos UAVs. Como o problema é um MINLP NP-hard, propõe a abordagem JTORATC, que transforma o problema multiobjetivo em mono-objetivo por ponderação linear e o divide em três subproblemas, resolvidos por splitting distribuído com arredondamento por limiar, KKT e SCA, respectivamente. Simulações mostram que o JTORATC supera benchmarks em valor da função objetivo, atraso total de conclusão e consumo total de energia dos UAVs, além de apresentar boa escalabilidade.