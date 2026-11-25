[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Wireless Communications**, que propõe uma estrutura hierárquica de enxames de UAVs para redes de acesso aéreo 6G, com otimização conjunta de implantação, trajetória e controle de potência por meio de um problema multiobjetivo resolvido pelo algoritmo **INS-WOA** (Improved Non-dominated Sorting Whale Optimization Algorithm), validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Dynamic Trajectory Optimization and Power Control for Hierarchical UAV Swarms in 6G Aerial Access Network
*   **DOI:** 10.1109/TWC.2025.3603432
*   **Publicação (Veículo/Evento):** IEEE Transactions on Wireless Communications
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea (por função)
*   **Descrição da Frota:** S enxames hierárquicos de UAVs, cada um composto por 1 H-UAV (*head UAV*) atuando como estação base aérea e M_s T-UAVs (*tail UAVs*) responsáveis por coleta e relay de dados de GUs em áreas remotas. O número de T-UAVs por enxame é variável e otimizado conforme a distribuição dos usuários. Os UAVs exercem papéis funcionais distintos (H-UAV versus T-UAV).

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot (UAVs) |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (OFDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A arquitetura é hierárquica, com enxames de UAVs operando em áreas remotas de grande escala. Cada enxame possui um **H-UAV** que permanece pairando como estação base aérea e vários **T-UAVs** que partem do ponto de implantação do enxame e voam sucessivamente entre posições de pairamento para coletar dados dos GUs e retransmiti-los ao H-UAV. O modelo de mobilidade segue o padrão *successive-hover-fly*: os T-UAVs pairam para coletar dados e voam entre pontos de pairamento. A comunicação G2A usa modelo probabilístico de path loss com LoS/NLoS; a comunicação A2A usa apenas LoS. O acesso é baseado em OFDMA para evitar interferência. O problema multiobjetivo de minimizar o consumo de energia dos enxames e dos GUs e o atraso de transmissão dos GUs é formulado como um MOP inteiro misto não linear. A solução divide o problema: (i) partição de área via K-means e diagramas de Voronoi; (ii) estabelecimento de conexões via pontos de Fermat; (iii) otimização do MOP transformado via INS-WOA, que busca soluções de Pareto. O processamento é embarcado nos UAVs e a comunicação é explícita.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de implantação cooperativa de múltiplos enxames de UAVs em áreas remotas de grande escala para redes de acesso aéreo 6G, nas quais os UAVs atuam como estações base aéreas e relays. Propõe uma estrutura hierárquica com H-UAVs (estações base aéreas) e T-UAVs (relays de coleta de dados) e formula um problema de otimização multiobjetivo (USDC-MOP) para minimizar simultaneamente o consumo de energia dos enxames de UAVs, o consumo de energia dos GUs e o atraso de transmissão dos GUs, otimizando implantação, trajetórias e controle de potência. Como o problema é um MINLP NP-hard, desenvolve uma partição de área baseada em K-means e Voronoi, conexões baseadas em pontos de Fermat e o algoritmo INS-WOA para buscar soluções de Pareto. Simulações extensas mostram superioridade sobre benchmarks em eficácia e baixa complexidade, com redução de 50% na complexidade.