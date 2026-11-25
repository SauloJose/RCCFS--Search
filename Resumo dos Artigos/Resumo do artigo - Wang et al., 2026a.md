[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Cognitive Communications and Networking**, que propõe o algoritmo **CMADDPG** (Clustering-based Multi-agent Deep Deterministic Policy Gradient) para escalonamento cooperativo de tarefas por múltiplos UAVs em Redes Integradas Espaço-Ar-Solo (SAGIN), com validação por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Cluster-Based Multi-Agent Task Scheduling for Space–Air–Ground Integrated Networks
*   **DOI:** 10.1109/TCCN.2025.3553297
*   **Publicação (Veículo/Evento):** IEEE Transactions on Cognitive Communications and Networking
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs (N_u) organizados dinamicamente em clusters, cada um com um UAV Cluster Head (CH) e vários UAVs membros (CMs). A rede inclui também satélites LEO, estações base terrestres e dispositivos móveis. Os UAVs são similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical (CTDE + clustering com CHs) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Optimization (K-Means) |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Cellular; Long-range (Satélite LEO) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede SAGIN é composta por três camadas: espacial (satélites LEO), aérea (UAVs) e terrestre (estações base e dispositivos móveis). Os UAVs coletam tarefas dos dispositivos móveis e podem processá-las localmente, descarregá-las para estações base ou para satélites LEO. A arquitetura adota um modelo de controle distribuído-centralizado: o algoritmo **KMDUC** particiona dinamicamente os UAVs em clusters, cada um gerenciado por um Cluster Head (CH), que delega decisões de offloading aos membros do cluster, reduzindo custos de comunicação intra-cluster e conflitos de decisão. O algoritmo **CMADDPG** usa um framework de aprendizado por reforço multiagente com treinamento centralizado (crítico central no satélite) e execução distribuída (atores nos UAVs), permitindo coordenação eficiente e escalabilidade. A comunicação entre UAVs, CHs, estações base e satélites é explícita e suportada por enlaces sem fio, com bandas de frequência distintas para BSs e satélites LEO.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o desafio de escalonamento cooperativo de tarefas em Redes Integradas Espaço-Ar-Solo (SAGIN), nas quais satélites e nós aéreos auxiliam no offloading de tarefas computacionais. Propõe o algoritmo CMADDPG, que combina um algoritmo de clustering dinâmico baseado em K-Means (KMDUC) com um framework de aprendizado por reforço multiagente (MADDPG) em regime de treinamento centralizado e execução distribuída. Os UAVs são agrupados em clusters com Cluster Heads que gerenciam as decisões de offloading, reduzindo o custo de comunicação e conflitos de decisão. O problema é formulado para maximizar o lucro de longo prazo do sistema, considerando tamanho dos dados, complexidade computacional e requisitos de atraso, com restrições de deadline e capacidade de processamento. Simulações mostram que o CMADDPG otimiza a alocação de recursos, minimiza atrasos de fila, mantém balanceamento de carga e supera métodos existentes em pelo menos 25% no lucro do sistema, com robustez e adaptabilidade em diversos cenários.