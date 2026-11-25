[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Wireless Communications**, que investiga a otimização conjunta de sensoriamento, comunicação e computação em uma rede de computação de borda aérea (AEC) colaborativa com múltiplos UAVs e uma plataforma de alta altitude (HAP), usando otimização de Lyapunov e MADRL baseado em PPO, com validação por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Joint Optimization of Sensing, Communication, and Computing for Collaborative Multi-UAV Edge Computing System
*   **DOI:** 10.1109/TWC.2025.3590253
*   **Publicação (Veículo/Evento):** IEEE Transactions on Wireless Communications
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs atuando como relays de coleta de dados entre dispositivos de sensoriamento IoT (SDs) e uma HAP estacionária que funciona como estação base aérea (ABS) e provedora de computação de borda. Os UAVs são similares entre si; a HAP é uma infraestrutura fixa de nível superior.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization; Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (NOMA, OMA/OFDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede AEC é composta por uma HAP estacionária, múltiplos UAVs e dispositivos de sensoriamento IoT agrupados em clusters. A HAP atua como estação base aérea, fornecendo acesso sem fio e serviços de computação de borda aos UAVs; os UAVs atuam como relays de coleta de dados, recebendo dados dos SDs e encaminhando-os à HAP. O uplink D2U usa NOMA com SIC, enquanto o uplink U2H usa OMA/OFDMA. O problema conjunto de tempos de sensoriamento, trajetórias dos UAVs, controle de potência de transmissão, estratégia de offloading e alocação de recursos de comunicação é formulado para minimizar o tempo médio de conclusão de tarefas sob estabilidade de consumo de energia. A otimização de Lyapunov transforma o problema de longo prazo; subproblemas são resolvidos por análise numérica, aproximação convexa sucessiva (SCA) e algoritmo de Dinkelbach, e embutidos em um framework MADRL baseado em PPO para trajetórias, offloading e alocação de recursos. O processamento é híbrido (UAVs e HAP) e a execução é online.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda a otimização conjunta de sensoriamento, comunicação e computação (JSCC) em redes de computação de borda aérea colaborativas com múltiplos UAVs e HAP, visando minimizar o tempo médio de conclusão de tarefas e o consumo de energia. Formula um problema que otimiza conjuntamente tempos de sensoriamento, trajetórias dos UAVs, controle de potência de transmissão, estratégia de offloading e alocação de recursos de comunicação, sob restrições de estabilidade energética. Usa otimização de Lyapunov para transformar o problema de longo prazo em subproblemas: tempos de sensoriamento resolvidos analiticamente; controle de potência D2U e U2H resolvidos por SCA e Dinkelbach; trajetórias, offloading e alocação de recursos resolvidos por MADRL baseado em PPO. Resultados de simulação mostram desempenho superior em tempo médio de conclusão de tarefas e consumo de energia em comparação com quatro esquemas de referência.