[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Internet of Things Journal**, que propõe uma arquitetura multi-LEO orientada por **Digital Twin** e o esquema **DEMAT** para handover, treinamento de feixe, alocação de potência e adaptação de largura de feixe, com o objetivo de maximizar eficiência energética em redes de satélites LEO, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** AI-Enabled Digital Twin-Driven Handover and Resource Allocation in Multi-LEO Satellite Networks
*   **DOI:** 10.1109/JIOT.2026.3698242
*   **Publicação (Veículo/Evento):** IEEE Internet of Things Journal
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Constelação de N satélites LEO, cada um com até M feixes, servindo K usuários terrestres. Os satélites são tratados como nós homogêneos de uma rede multi-LEO, com gateways terrestres para troca contínua de dados com seus respectivos Digital Twins.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Resources; Outro (Handover/Beam Management) |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Long-range (Satélite) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A arquitetura integra um sistema real multi-LEO e seu gêmeo digital. O mundo real contém satélites LEO, feixes, usuários terrestres e gateways; o mundo digital replica órbitas, condições meteorológicas, canais e efeitos de propagação via ray tracing. Há troca bidirecional de informações entre domínio real e digital, com entidades DT dos satélites e ambiente virtual. O esquema DEMAT é dividido em duas fases: **DEMAT-HO**, que realiza treinamento de feixe e handover preditivos com base na evolução histórica de feixes e SINR; e **DEMAT-RA**, que usa TD3 multiagente para otimizar potência de transmissão e largura de feixe. A agregação é aprimorada por federated learning, e o problema de maximização de eficiência energética considera atrasos de comunicação, computação e interação real-digital.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda os desafios de constelações LEO densas, incluindo interferência entre feixes e entre satélites, handovers frequentes e canais altamente dinâmicos, que dificultam a otimização em tempo real. Propõe uma arquitetura multi-LEO orientada por Digital Twin, com simulações virtuais baseadas em ray tracing e controle inteligente em órbita, e o esquema DEMAT, que otimiza conjuntamente treinamento de feixe, handover, alocação de potência e adaptação de largura de feixe para maximizar a eficiência energética sob requisitos de throughput dos usuários. O DEMAT usa troca bidirecional de parâmetros DT-LEO e agentes aprimorados por federated learning para gestão cooperativa e de baixa latência. Simulações com dados de terreno GMTED2010 e modelos de canal ITU validam convergência e escalabilidade, com ganho de até 59,6% em eficiência energética sobre o baseline DDPG e mais de 40% sobre outros benchmarks baseados em DT.