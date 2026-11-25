[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Internet of Things Journal**, que propõe o algoritmo **QMIXDM** (QMIX-based Delay Minimization) para offloading cooperativo de computação e otimização de trajetória em redes de computação de borda aérea (AEC) habilitadas por enxames heterogêneos de UAVs, com validação por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Joint Cooperative Computation Offloading and Trajectory Optimization in Heterogeneous UAV-Swarm-Enabled Aerial Edge Computing Networks
*   **DOI:** 10.1109/JIOT.2024.3362321
*   **Publicação (Veículo/Evento):** IEEE Internet of Things Journal
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Enxame composto por M UAVs leves (*lightweight*) e 1 UAV aprimorado (*enhanced*), todos equipados com servidores MEC. O UAV aprimorado possui capacidade de computação superior e atua como nó central de cooperação; os UAVs leves atuam simultaneamente como servidores MEC e relays, podendo descarregar parte de suas tarefas para o UAV aprimorado.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (CTDE: treinamento centralizado, execução descentralizada) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede AEC é composta por um enxame heterogêneo de UAVs (M leves + 1 aprimorado) que atuam como servidores MEC móveis para UEs no solo. Cada UE pode executar parte de sua tarefa localmente e descarregar o restante para um UAV (*access offloading*); os UAVs leves podem, por sua vez, repassar parte da carga ao UAV aprimorado (*network offloading*), caracterizando cooperação em dois níveis. A comunicação usa FDMA com enlaces LoS dominantes. O problema conjunto de trajetória dos UAVs e decisões de offloading é formulado como um MINLP para minimizar a soma dos atrasos máximos fim-a-fim ao longo do horizonte temporal. A solução decompõe o problema em dois subproblemas: planejamento de trajetória, resolvido por QMIX multiagente com arquitetura de ramificação de ações; e decisão de offloading, resolvido por análise teórica e algoritmo de limiar com solução em forma fechada via KKT. O treinamento é centralizado e a execução é descentralizada; o processamento é híbrido entre UEs, UAVs leves e UAV aprimorado.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading cooperativo de computação e otimização de trajetória em redes AEC habilitadas por enxames heterogêneos de UAVs, nos quais UAVs com diferentes capacidades computacionais cooperam para atender demandas variáveis no tempo e no espaço de UEs com tarefas sensíveis a atraso. Formula um problema MINLP para minimizar a soma dos atrasos máximos fim-a-fim ao longo do horizonte, otimizando conjuntamente trajetórias dos UAVs, razões de access offloading e razões de network offloading. Como o problema é acoplado e não convexo, decompõe-no em dois subproblemas: planejamento de trajetória, resolvido por um algoritmo multiagente baseado em QMIX (QMIXDM) com arquitetura de ramificação de ações para reduzir a complexidade; e decisão de offloading, resolvido por análise teórica, condições KKT e algoritmo de limiar. Simulações mostram ganhos significativos de desempenho em relação a benchmarks e confirmam que a coordenação eficiente entre UAVs heterogêneos melhora o desempenho do sistema.