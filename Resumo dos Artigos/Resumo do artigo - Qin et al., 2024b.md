[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Network Science and Engineering**, que propõe um sistema de computação de borda colaborativa ar-solo com múltiplos UAVs (associados e auxiliares), usando otimização de Lyapunov e PMADDPG para minimizar o consumo total de energia sob restrições de estabilidade de fila, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Joint Task Allocation and Trajectory Optimization for Multi-UAV Collaborative Air–Ground Edge Computing
*   **DOI:** 10.1109/TNSE.2024.3481061
*   **Publicação (Veículo/Evento):** IEEE Transactions on Network Science and Engineering
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea (por função)
*   **Descrição da Frota:** M UAVs associados (*associated UAVs*) que atendem diretamente os dispositivos terrestres (GDs) e N UAVs auxiliares (*auxiliary UAVs*) que recebem tarefas dos associados e as encaminham para uma estação base remota. Todos os UAVs voam a altitude constante H e velocidade constante v, mas exercem papéis funcionais distintos na arquitetura.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical (dois tipos de agentes cooperando) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (FDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede é uma computação de borda colaborativa ar-solo com múltiplos UAVs, uma estação base (BS) remota e K dispositivos terrestres (GDs). Os GDs descarregam tarefas para os UAVs associados, que estão próximos dos usuários mas não conseguem manter comunicação eficaz com a BS distante. Os UAVs associados podem processar parte das tarefas localmente e descarregar o restante para os UAVs auxiliares, que por sua vez processam parte e encaminham o restante para a BS. O processamento é paralelo e distribuído entre UAVs associados, UAVs auxiliares e BS. O problema conjunto de associação de offloading, trajetórias dos dois tipos de UAVs, particionamento de tarefas e alocação de recursos computacionais é formulado como um MINLP de longo prazo com restrições de estabilidade de fila. A otimização de Lyapunov transforma o problema em dois subproblemas por slot: (i) offloading e trajetórias, resolvido por PMADDPG (Probabilistic Multi-Agent DDPG), que converte decisões binárias em probabilidades contínuas para lidar com espaço de ações híbrido; e (ii) particionamento de tarefas e alocação de recursos, resolvido por dualidade de Lagrange com solução em forma fechada. A comunicação usa FDMA para evitar interferência, e o processamento é híbrido entre UAVs e BS.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de consumo de energia em redes de computação de borda colaborativa ar-solo com múltiplos UAVs, nas quais dispositivos IoT em locais isolados têm recursos limitados e podem estar fora da cobertura de redes terrestres. Propõe uma arquitetura com UAVs associados (que atendem diretamente os GDs) e UAVs auxiliares (que recebem tarefas dos associados e as encaminham para a BS remota), permitindo processamento paralelo e colaborativo. Formula um problema de minimização do consumo total de energia de longo prazo, otimizando conjuntamente decisões de offloading, trajetórias dos UAVs, particionamento de tarefas e alocação de recursos computacionais, sob restrições de estabilidade das filas de tarefas. Usa otimização de Lyapunov para decompor o problema em dois subproblemas por slot, resolvidos por PMADDPG e por dualidade de Lagrange com solução em forma fechada. Simulações mostram que a abordagem proposta supera benchmarks em consumo total de energia, com melhor convergência e equilíbrio entre consumo energético e estabilidade das filas.