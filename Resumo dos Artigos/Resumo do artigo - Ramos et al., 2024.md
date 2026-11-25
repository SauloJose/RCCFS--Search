[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Access**, que propõe a arquitetura cognitiva **ARCog-NET** para enxames de robôs aéreos, baseada no modelo Edge-Fog-Cloud, integrando percepção, planejamento, tomada de decisão e aprendizado adaptativo, validada por simulação com ROS e Gazebo em cenário de inspeção de parque eólico.

---

### 📌 Metadados do Artigo
*   **Título:** ARCog-NET: An Aerial Robot Cognitive Network Architecture for Swarm Applications Development
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** IEEE Access
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (SITL — software-in-the-loop com ROS e Gazebo)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Enxame de UAVs organizado em dois grupos de agentes de borda (Edge Agents), cada grupo coordenado por um UAV coordenador de fog (Fog Coordinator), conectados a um servidor de nuvem central. Os UAVs de borda executam a missão, enquanto os coordenadores de fog fazem processamento intermediário e supervisão dos grupos.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid (Edge-Fog-Cloud) |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (MAVLink) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS (MAVROS); Outro (Gazebo) |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O ARCog-NET adota uma arquitetura cognitiva hierárquica distribuída baseada no modelo Edge-Fog-Cloud (EFC). Os UAVs de borda (*Edge Agents*) realizam coleta de dados em tempo real, percepção ambiental e decisões locais, incluindo desvio de obstáculos e controle de baixo nível. Os UAVs coordenadores de fog (*Fog Coordinators*) fazem processamento intermediário, supervisão dos grupos e coordenação descentralizada do enxame, auxiliando na comunicação, navegação e algoritmos operacionais. O servidor em nuvem realiza análise global, supervisão de missão, armazenamento de longo prazo e intervenção humana (HITL). A arquitetura opera em loop, com iterações paralelas em diferentes nós da rede, e utiliza uma estrutura de mensagens padronizada transmitida via MAVLink, com *workflows* categorizados entre agentes, coordenadores e servidor. A tomada de decisão cognitiva emprega aprendizado por reforço (RL), e há integração de um modelo de autoencoder para compressão de imagens implementado em Keras e ROS para reduzir o tráfego de dados.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda a necessidade de arquiteturas cognitivas para enxames de UAVs que integrem percepção, aprendizado, tomada de decisão e memória de forma organizada e escalável. Propõe o ARCog-NET, uma arquitetura de rede cognitiva para robôs aéreos baseada em Edge-Fog-Cloud, na qual UAVs de borda executam a missão e decisões em tempo real, coordenadores de fog supervisionam grupos e o servidor em nuvem realiza análise global e armazenamento. A arquitetura inclui um modelo de compressão de imagens por autoencoder integrado ao ROS, comunicação via MAVLink com workflows padronizados e tomada de decisão por aprendizado por reforço. A validação é feita por simulação SITL com ROS e Gazebo em um cenário de inspeção de parque eólico, demonstrando melhoria em planejamento de trajetória, evitamento de colisões, redução de latência, aumento de throughput e eficiência no processamento de dados.