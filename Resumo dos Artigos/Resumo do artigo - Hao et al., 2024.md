[[Atv1 - Parte 4 - Entrega Final]]


**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Mobile Computing**, que investiga offloading de tarefas com prioridade em um sistema MEC assistido por múltiplos UAVs cooperativos, com projeto de trajetória, alocação de recursos de computação/comunicação e decisão binária de offloading, resolvido por um algoritmo DRL baseado em espaço latente e validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Joint Task Offloading, Resource Allocation, and Trajectory Design for Multi-UAV Cooperative Edge Computing With Task Priority
*   **DOI:** 10.1109/TMC.2024.3350078
*   **Publicação (Veículo/Evento):** IEEE Transactions on Mobile Computing
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs cooperativos (N UAVs) equipados com recursos de comunicação e computação, atendendo M UEs e com acesso a um servidor de edge cloud (EC). Os UAVs podem encaminhar tarefas entre si e para o EC, além de fornecer recursos de computação aos UEs. O número exato de UAVs não é fixado no texto.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é composto por N UAVs, M UEs e um servidor de edge cloud. Os UAVs atuam tanto na transmissão quanto na computação: podem receber tarefas dos UEs via enlaces G2A, encaminhar tarefas para outros UAVs via A2A ou para o EC via A2G, e também processar tarefas com seus próprios recursos. As tarefas são indivisíveis (offloading binário) e podem ser executadas localmente no UE, em qualquer UAV ou no EC. O problema conjunto de trajetória dos UAVs, decisão de offloading, alocação de recursos computacionais e gerenciamento de recursos de comunicação é formulado como um problema de programação inteira mista e transformado em um MDP com espaço de ações híbrido discreto-contínuo. A solução usa um algoritmo DRL com tabela de embedding para ações discretas e autoencoder variacional condicional para ações contínuas, combinado com TD3. O processamento é distribuído entre UEs, UAVs e EC; a otimização conjunta é formulada como um MDP único resolvido por DRL, embora o texto não detalhe explicitamente a entidade controladora.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas em sistemas MEC assistidos por múltiplos UAVs cooperativos, considerando prioridade de tarefas e modo de offloading binário. Define um ganho de sistema baseado em consumo de energia e atraso de tarefa e formula a otimização conjunta de trajetória dos UAVs, decisão binária de offloading, alocação de recursos de computação e gerenciamento de recursos de comunicação como um problema de programação inteira mista, com objetivo de maximizar o ganho médio de longo prazo. Como o problema tem espaço de ações híbrido discreto-contínuo, propõe um algoritmo DRL baseado em espaço latente, com embedding para ações discretas e CVAE para ações contínuas, combinado com TD3. Os resultados de avaliação mostram que o algoritmo proposto supera três soluções alternativas de estado da arte em termos de atraso de tarefa e ganho de sistema.