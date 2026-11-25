[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Internet of Things Journal**, que propõe uma abordagem de aprendizado por reforço profundo multiagente (MADRL) baseada em MATD3 para redes MEC descentralizadas com múltiplos UAVs, com um mecanismo de interação entre UAVs gerado por redes neurais e orientado a tarefas, validado por resultados numéricos/simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Multiagent Deep Reinforcement Learning for Decentralized Multi-UAV Mobile Edge Computing Networks
*   **DOI:** 10.1109/JIOT.2025.3527016
*   **Publicação (Veículo/Evento):** IEEE Internet of Things Journal
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (resultados numéricos)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** M UAVs ativos (de um total de M̃ UAVs disponíveis) atuando como servidores de borda aéreos para N usuários móveis (MUs). Os UAVs são similares entre si e compartilham a mesma arquitetura de rede neural (parameter sharing). O número de UAVs ativos pode variar entre blocos do sistema, exigindo escalabilidade.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot (UAVs como servidores de borda) |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (TDD/FDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é uma rede MEC multi-UAV descentralizada na qual os UAVs atuam como servidores de borda e tomam decisões locais com base apenas em observações parciais. O problema é formulado como um **POMDP multiagente**. O método **MATD3** proposto usa três redes ator distintas: (i) **message NN**, que gera mensagens de coordenação (iniciais e temporais) a partir das observações locais; (ii) **coordination NN**, que agrega as mensagens recebidas de outros UAVs usando um mecanismo de atenção inspirado em GAT, no qual as mensagens iniciais servem como embeddings para diferenciar os UAVs; e (iii) **solution NN**, que determina as variáveis de decisão (trajetória, associação UAV-MU, alocação de largura de banda e CPU, e razões de offloading). Uma estratégia de **parameter sharing** permite que a mesma rede seja aplicada a diferentes números de UAVs sem retreinamento. A comunicação UAV-MU usa TDD com FDMA, e os UAVs trocam mensagens explicitamente entre si. O treinamento é conjunto e end-to-end, e a execução é descentralizada, com cada UAV decidindo com base em sua observação local e nas mensagens recebidas.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de minimização do consumo total de energia de usuários móveis em redes MEC assistidas por múltiplos UAVs, no qual os UAVs precisam decidir descentralizadamente sobre mobilidade, associação UAV-MU, alocação de recursos de comunicação e computação, e razões de offloading de tarefas. Modela o sistema como um POMDP multiagente no qual cada UAV decide com informações limitadas. Diferentemente de métodos MADRL convencionais que projetam manualmente as mensagens de interação entre UAVs, o artigo propõe um mecanismo de interação baseado em redes neurais que gera autonomamente mensagens orientadas a tarefas, permitindo a otimização conjunta das interações e das decisões descentralizadas de forma end-to-end. O framework MATD3 utiliza três redes ator (message, coordination e solution) e parameter sharing para escalabilidade a diferentes números de UAVs. Resultados numéricos mostram que a abordagem supera métodos MADRL tradicionais e atinge desempenho próximo a esquemas centralizados ideais, mantendo escalabilidade com a variação do número de UAVs.