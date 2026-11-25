[[Atv1 - Parte 4 - Entrega Final]]


**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Intelligent Transportation Systems**, que propõe um sistema de computação de borda colaborativa multi-UAV (UCC) com um framework de otimização bilevel (TDE) para implantação de UAVs, offloading colaborativo de tarefas e alocação de recursos de computação/comunicação, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Multi-UAV-Enabled Collaborative Edge Computing: Deployment, Offloading and Resource Optimization
*   **DOI:** 10.1109/TITS.2024.3432818
*   **Publicação (Veículo/Evento):** IEEE Transactions on Intelligent Transportation Systems
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs (I UAVs) atuando como servidores de borda aéreos (*UAV edge nodes*), com capacidade de computação e comunicação, atendendo J usuários distribuídos de forma não uniforme em uma área geográfica. Os UAVs são interconectados e podem colaborar entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization; Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema UCC é composto por múltiplos UAVs servidores de borda e usuários com dispositivos. Os usuários podem executar tarefas localmente, descarregá-las para um UAV ou dividi-las para computação colaborativa entre UAVs (offloading colaborativo). Os UAVs são interconectados em uma rede *ad-hoc* totalmente conectada e se comunicam explicitamente por enlaces A2A para encaminhar subtarefas. O problema conjunto de implantação dos UAVs, decisão de offloading e alocação de recursos de computação e comunicação é formulado como um MINLP e resolvido por um framework bilevel chamado TDE: no nível superior, um algoritmo de Evolução Diferencial (DE) aprimorado otimiza a implantação dos UAVs; no nível inferior, um algoritmo TD3 (DRL) otimiza offloading e alocação de recursos, observando a implantação e o estado de carga da rede. O processamento é híbrido (local nos dispositivos e nos UAVs) e a execução das decisões ocorre online.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de distribuição não uniforme de usuários em sistemas de computação de borda com UAVs, que dificulta a implantação ótima e o balanceamento de carga. Propõe um sistema de computação de borda colaborativa multi-UAV (UCC), no qual tarefas podem ser divididas e processadas colaborativamente entre UAVs para equilibrar a carga e melhorar a utilização de recursos. Formula um problema conjunto de implantação de UAVs, offloading colaborativo de tarefas e alocação de recursos de computação e comunicação, com o objetivo de minimizar o consumo total de energia sob restrições de atraso. Para resolver o MINLP não convexo, decompõe o problema em dois níveis e propõe o framework TDE: DE aprimorado (com inicialização gulosa, fatores adaptativos e operador de eliminação) para implantação no nível superior, e TD3 (DRL) para offloading e alocação de recursos no nível inferior. Resultados experimentais mostram redução de 32,4% no consumo de energia e aumento médio de 30% na taxa de conclusão de tarefas em comparação com DDPG, ToDeTAS e outros benchmarks.