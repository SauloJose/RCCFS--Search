[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado no **Journal of Network and Computer Applications** (Elsevier), que propõe uma abordagem de offloading de tarefas e otimização de trajetória para MEC assistida por múltiplos UAVs, usando **MADDPG** (Multi-Agent Deep Deterministic Policy Gradient) e gerenciamento centralizado via **SDN**, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** A multi-UAV assisted task offloading and path optimization for mobile edge computing via multi-agent deep reinforcement learning
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** Journal of Network and Computer Applications (Elsevier)
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs (M UAVs) equipados com servidores MEC, atuando como nós de borda aérea para N UEs no solo. A rede é gerenciada centralmente por um controlador SDN, com UAVs de computação e um UAV manager (UAV-C) na camada de borda. Os UAVs de computação são similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical (SDN centralizado + execução descentralizada via MADDPG) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Outro (SDN/OpenFlow) |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede MEC multi-UAV é organizada em três camadas com **SDN**: camada de controle (controlador SDN com OpenFlow, responsável por gerenciamento centralizado, alocação de recursos e decisões de offloading), camada de borda (switches/roteadores, UAV manager UAV-C e UAVs de computação) e camada de dados (dispositivos IoT e UEs). Os UAVs de computação atuam como servidores MEC aéreos e o UAV manager coleta informações dos usuários e encaminha decisões do controlador SDN. O problema conjunto de offloading de tarefas e trajetórias dos UAVs é resolvido com **MADDPG** em regime de **treinamento centralizado e execução descentralizada**, no qual cada UAV é um agente que aprende sua política de offloading e trajetória. A função objetivo considera o consumo total de energia do sistema, com **Jain's fairness index** para medir e promover balanceamento de carga entre UAVs e justiça no atendimento aos UEs. O processamento é híbrido (local nos UEs e nos UAVs) e a comunicação é explícita.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas e planejamento de trajetória em sistemas MEC assistidos por múltiplos UAVs, nos quais a distribuição desigual de UEs e as limitações de energia dos UAVs podem causar desbalanceamento de carga e maior consumo energético. Propõe um modelo de sistema MEC multi-UAV gerenciado centralmente por SDN, com uma arquitetura em três camadas (controle, borda e dados) e uso de OpenFlow para controle e encaminhamento de dados. Formula um problema conjunto de offloading de tarefas e otimização de trajetórias com o objetivo de minimizar o consumo total de energia do sistema, incorporando o índice de justiça de Jain para medir o balanceamento de carga entre UAVs e a equidade no serviço aos UEs. A solução emprega **MADDPG** com treinamento centralizado e execução descentralizada, no qual cada UAV é um agente que aprende políticas de offloading e trajetória em ambiente dinâmico ar-solo. Simulações demonstram que o método reduz consumo de energia e latência de computação em comparação com benchmarks, mantendo eficiência, estabilidade e confiabilidade do sistema.