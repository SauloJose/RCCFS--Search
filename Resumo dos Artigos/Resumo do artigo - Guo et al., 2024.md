[[Atv1 - Parte 4 - Entrega Final]]

### 📌 Metadados do Artigo
*   **Título:** Multi-UAV Cooperative Task Offloading and Resource Allocation in 5G Advanced and Beyond
*   **DOI:** 10.1109/TWC.2023.3277801
*   **Publicação (Veículo/Evento):** IEEE Transactions on Wireless Communications
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Múltiplos UAVs de computação atuando como servidores aéreos e um UAV gerente (*head UAV*) equipado com SDN-C, CDC e CCC. Os UAVs de computação são similares entre si, mas o conjunto é heterogêneo devido ao UAV gerente com função e configuração distintas.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization; Rules & Heuristics (TGAOA) |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Não especificado |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Cellular |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Nenhum |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é um MUEAC cooperativo aprimorado por SDN. O UAV gerente hospeda o controlador SDN central (SDN-C), além dos clouds centralizados de dados e controle (CDC/CCC), e gerencia a rede global. Os UAVs de computação coletam informações via UAV-Cs e executam regras de offloading/alocação enviadas pelo controlador. Dispositivos terrestres descarregam tarefas divisíveis e dependentes por enlaces G2A, D2D e A2A, com offloading parcial para diferentes UAVs. O processamento ocorre nos UAVs de computação, enquanto a decisão de associação D2D, offloading e alocação de recursos é centralizada e resolvida pelo esquema MCCCO, com otimização convexa e o algoritmo TGAOA.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading e alocação de recursos em computação aérea com múltiplos UAVs (MUEAC), especialmente em cenários remotos sem infraestrutura terrestre de edge/cloud. Propõe um sistema MUEAC cooperativo aprimorado por SDN, com offloading em dois saltos via D2D e A2A e offloading parcial para tarefas divisíveis com dependência de dados. Formula um problema conjunto de agendamento de tarefas e alocação de recursos para minimizar o atraso de processamento sob restrições de dependência de dados e consumo de energia dos UAVs. Para resolver o problema não convexo, apresenta o esquema MCCCO, que decompõe o problema e utiliza otimização convexa e o algoritmo TGAOA. Os resultados numéricos indicam redução do atraso e melhor balanceamento de carga no consumo de energia dos UAVs em comparação com esquemas tradicionais.