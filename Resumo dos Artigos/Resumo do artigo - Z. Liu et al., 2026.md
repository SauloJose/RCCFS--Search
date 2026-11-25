[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Systems, Man, and Cybernetics: Systems**, que propõe o framework **ConstrucTwin**, um sistema multi-robô de construção civil orientado por **Digital Twin**, com arquitetura de comunicação 5G, planejamento integrado em níveis de tarefa, movimento e motor, e supervisão humana em loop, validado por estudos de caso em simulação e cenários reais.

---

### 📌 Metadados do Artigo
*   **Título:** ConstrucTwin: Digital Twin-Driven Multirobot Construction System Toward Industry 5.0
*   **DOI:** 10.1109/TSMC.2026.3658622
*   **Publicação (Veículo/Evento):** IEEE Transactions on Systems, Man, and Cybernetics: Systems
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação; Testbed/Real-world

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Sistema multi-robô de construção composto por manipuladores industriais, sistemas de pórtico com atuadores, garras e efetuadores finais, além de armários de controle e interfaces de hardware. Os estudos de caso envolvem construção de gaiola de vergalhões e parede de tijolos.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Cellular (5G); Other (rede cabeada) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS 2 |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O ConstrucTwin adota uma estrutura frontend-backend: o módulo de Digital Twin atua como frontend para monitoramento, controle, planejamento e replanejamento por operadores humanos; o processamento cross-level atua como backend e conecta o mundo físico ao digital. A arquitetura inclui o sistema físico (robôs, efetuadores, atuadores e armários de controle), o Digital Twin (modelos CAD/URDF/Xacro em ambiente como Unity3D) e uma rede que interliga controladores, dispositivos de usuário e dispositivos locais/de borda, com suporte a 5G e estimação de qualidade de rede baseada em ray tracing. O pipeline cross-level é dividido em nível motor (interfaces de hardware e controladores ros2_control), nível de movimento (planejamento de trajetórias, checagem de colisão e otimização) e nível de tarefa (decomposição do produto em procedimentos e ações primitivas). Há fluxo bidirecional de dados entre físico e digital, com supervisão humana em loop e servoing visual.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda a lacuna de implementações de Digital Twin para sistemas multi-robô de construção, que costumam se limitar a robô único ou simulações offline. Propõe o ConstrucTwin, um framework que integra sistema físico multi-robô, Digital Twin, comunicação 5G com estimação de qualidade de rede e planejamento cross-level (tarefa, movimento e motor), permitindo sincronização bidirecional, supervisão humana remota e servoing visual. A arquitetura unifica planejamento de tarefas, planejamento de movimento e controle de baixo nível, com suporte a análise de construtibilidade, comissionamento virtual e ajustes remotos. Estudos de caso de construção de gaiola de vergalhões e parede de tijolos demonstram melhoria em velocidade de execução, precisão e escalabilidade, alinhando o sistema aos objetivos human-centered, resilientes e sustentáveis da Indústria 5.0.