[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado em periódico Springer (nome não explicitado no trecho), que investiga offloading de tarefas e alocação de recursos em um sistema MEC assistido por múltiplos UAVs, propondo o framework **MADDPG-DTLCM** (Multi-Agent Deep Deterministic Policy Gradient com mecanismo Distance to Task Location and Capability Match), validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Task offloading and resource allocation for multi-UAV asset edge computing with multi-agent deep reinforcement learning
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** Springer (periódico não explicitado no trecho; © The Author(s) 2025)
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** N UAVs equipados com servidores MEC, atuando como nós de borda aérea para V dispositivos de usuário (UDs) no solo, com apoio de um MEC server/edge cloud (EC). Os UAVs são similares entre si e planejados para trajetórias não sobrepostas.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (CTDE: treinamento centralizado, execução descentralizada) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Rules & Heuristics (DTLCM) |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (OFDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é uma rede MEC multi-UAV na qual os UDs geram tarefas computacionalmente intensivas e as descarregam para UAVs equipados com servidores MEC, que podem processá-las localmente ou encaminhá-las para outros UAVs (A2A) ou para um MEC server/edge cloud. O acesso G2A usa OFDMA com canais dominados por LoS. O problema conjunto de trajetória dos UAVs, decisão de offloading, alocação de recursos computacionais e gerenciamento de recursos de comunicação é formulado como um problema de programação inteira mista e resolvido por um framework MADDPG (Multi-Agent Deep Deterministic Policy Gradient) com CTDE. A seleção de UAV é guiada pelo mecanismo **DTLCM**, que combina a distância normalizada até a localização da tarefa com a correspondência entre a capacidade computacional do UAV e os requisitos da tarefa, produzindo um *Suitability Score* que prioriza UAVs próximos e com recursos adequados. O processamento é híbrido (UDs, UAVs e EC) e a execução das políticas é descentralizada nos UAVs, com comunicação explícita.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas e alocação de recursos em ambientes MEC assistidos por múltiplos UAVs, nos quais tarefas computacionalmente intensivas e sensíveis a atraso precisam ser distribuídas entre dispositivos de usuário, UAVs e infraestrutura de nuvem/borda. Propõe um framework colaborativo que integra o mecanismo **DTLCM** (Distance to Task Location and Capability Match) ao algoritmo **MADDPG**, garantindo que as tarefas sejam atribuídas a UAVs que sejam simultaneamente próximos espacialmente e computacionalmente capazes. O sistema define o ganho com base em eficiência energética e atraso de tarefa, formula o problema como programação inteira mista e o resolve com aprendizado por reforço profundo multiagente em regime CTDE, otimizando conjuntamente trajetórias, decisões de offloading, alocação de recursos computacionais e gerenciamento de comunicação. Simulações abrangentes mostram que o MADDPG-DTLCM supera MADQN, MADDPG sem DTLCM e offloading guloso, com 18% mais taxa de conclusão de tarefas e 12% menos latência, especialmente em cenários de alta densidade de usuários com colaboração entre UAVs.