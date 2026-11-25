[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Wireless Communications**, que investiga offloading de tarefas em um sistema MEC assistido por múltiplos UAVs com múltiplas edge clouds (ECs), usando um framework cooperativo de aprendizado por reforço profundo multiagente (MADRL) com TD3, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Multi-Agent Deep Reinforcement Learning for Task Offloading in UAV-Assisted Mobile Edge Computing
*   **DOI:** 10.1109/TWC.2022.3153316
*   **Publicação (Veículo/Evento):** IEEE Transactions on Wireless Communications
*   **Ano:** 2022

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** N UAVs atuando como servidores MEC aéreos (*flying MEC servers*), atendendo M UEs em subáreas não sobrepostas, e conectados a K edge clouds (ECs) com recursos superiores via enlaces de backhaul sem fio. Os UAVs são similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (multiagente cooperativo) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (OFDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é composto por N UAVs, M UEs e K edge clouds (ECs). Os UAVs atuam como servidores MEC aéreos, atendendo UEs em subáreas não sobrepostas para evitar colisões e sobreposição de cobertura. As tarefas dos UEs são descarregadas via enlaces G2A para os UAVs, que podem processar parte localmente e encaminhar o restante para as ECs via enlaces A2G. As ECs possuem mais recursos computacionais e de comunicação. O problema conjunto de trajetória dos UAVs, alocação de tarefas e gerenciamento de recursos de comunicação é formulado como um MDP multiagente com espaço de ações contínuo e alta dimensionalidade, e resolvido por um framework cooperativo MADRL com o algoritmo TD3 (Twin Delayed DDPG), no qual cada UAV é um agente que aprende sua política de movimento, razões de partição de tarefas e potência de transmissão. O processamento é híbrido (UAVs e ECs) e a comunicação é explícita via OFDMA.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas em sistemas MEC assistidos por múltiplos UAVs e múltiplas edge clouds, nos quais os UAVs têm capacidade limitada de computação e energia. Formula um problema de otimização para minimizar a soma ponderada de atrasos de execução e consumos de energia, otimizando conjuntamente as trajetórias dos UAVs, a alocação de tarefas computacionais e o gerenciamento de recursos de comunicação. Como o problema é não convexo e envolve um ambiente dinâmico com informações incompletas, modela-o como um MDP multiagente e propõe um framework cooperativo de MADRL com TD3, no qual cada UAV é um agente e a recompensa é a soma das recompensas individuais (com penalidades por violação de restrições de sobreposição, colisão e cobertura). Resultados de simulação mostram que o método proposto supera outras abordagens de otimização, especialmente em adaptabilidade à mobilidade dos UEs, robustez a mudanças nos recursos de comunicação e computação, e flexibilidade à dinamicidade das tarefas.