[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Mobile Computing**, que investiga offloading de tarefas e otimização de trajetória para comunicação segura em sistemas MEC multi-UAV com usuários dinâmicos, usando jamming da estação base e o algoritmo **JDPB** (Joint Dynamic Programming and Bidding), validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Task Offloading and Trajectory Optimization for Secure Communications in Dynamic User Multi-UAV MEC Systems
*   **DOI:** 10.1109/TMC.2024.3442909
*   **Publicação (Veículo/Evento):** IEEE Transactions on Mobile Computing
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** M UAVs de asa fixa atuando como servidores de borda aéreos, voando a altitude fixa H e atendendo K usuários terminais (TUs) móveis. O sistema inclui ainda uma estação base (BS) que emite sinais de jamming contra E eavesdroppers no solo. Os UAVs são similares entre si.

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
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (TDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é uma rede MEC multi-UAV para comunicação segura, na qual uma região é dividida em sub-regiões e os TUs móveis descarregam tarefas para os UAVs que cobrem cada sub-região. A estação base emite sinais de interferência (jamming) para dificultar a escuta por eavesdroppers no solo; os UAVs conhecem previamente o sinal da BS e conseguem separá-lo, enquanto os eavesdroppers o tratam como sinal útil e são prejudicados. Os TUs se movem segundo o modelo Gauss-Markov e o acesso é baseado em TDMA. O problema conjunto de decisão de offloading, alocação de recursos (potência de transmissão, tempo, frequência de CPU) e planejamento de trajetória dos UAVs é formulado para maximizar a capacidade mínima de cálculo seguro dos TUs. A solução JDPB divide o problema em dois subproblemas: variáveis contínuas (potência, tempo, frequência e trajetória), resolvidas por SCA e BCD; e decisão de offloading (variáveis binárias), resolvida por programação dinâmica combinada com leilão (bidding). O processamento é híbrido (TUs e UAVs) e a execução é online.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas e planejamento de trajetória em sistemas MEC multi-UAV com usuários móveis e risco de escuta por eavesdroppers. Propõe uma arquitetura na qual a estação base emite sinais de jamming para proteger o offloading, e os UAVs ajustam dinamicamente suas posições para atender os TUs que se movem segundo o modelo Gauss-Markov. Formula um problema de otimização conjunta de decisão de offloading, alocação de potência, tempo e frequência de CPU, e trajetórias dos UAVs, com o objetivo de maximizar a capacidade mínima de cálculo seguro dos TUs sob restrições de energia, velocidade, distância de segurança e requisitos mínimos de computação segura. Como o problema é complexo e misto, propõe o algoritmo JDPB, que combina SCA e BCD para as variáveis contínuas e programação dinâmica com leilão para as decisões binárias de offloading. Simulações mostram que o JDPB supera estratégias aleatórias, gulosas e outros benchmarks em desempenho de segurança e robustez sob diferentes configurações de parâmetros.