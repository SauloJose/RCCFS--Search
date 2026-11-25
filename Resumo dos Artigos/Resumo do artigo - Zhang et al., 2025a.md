[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Vehicular Technology**, que investiga offloading de tarefas e alocação de recursos em uma rede MEC colaborativa ar-solo assistida por múltiplos UAVs, usando a métrica **Age of Processing (AoP)** e o algoritmo **HAPPO**, com validação por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Task Offloading in UAV-Assisted Mobile Cloud-Edge Computing Networks: An AoP-Aware HAPPO Approach
*   **DOI:** 10.1109/TVT.2025.3566431
*   **Publicação (Veículo/Evento):** IEEE Transactions on Vehicular Technology
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos servidores UAV estáticos, posicionados a uma altitude constante, equipados com servidores de borda e conectados por backhaul sem fio a um edge cloud (EC). Os UAVs atendem N usuários móveis; a frota robótica é composta por UAVs similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (FDMA / backhaul sem fio) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede é uma MEC colaborativa ar-solo com M UAVs servidores estáticos, N usuários móveis e um edge cloud central. O EC conhece inicialmente as posições dos usuários, particiona-os em M clusters via K-Means++ e determina as posições horizontais dos UAVs. Os UAVs recebem requisições dos usuários, decidem associação, alocação de largura de banda e recursos computacionais e a razão de offloading para o EC. O uplink usuário-UAV usa FDMA e canais probabilísticos LoS/NLoS; os UAVs se conectam ao EC por backhaul sem fio. O problema é formulado como POMDP e resolvido pelo HAPPO, com treinamento centralizado e execução descentralizada, no qual cada UAV é um agente e as políticas são atualizadas sequencialmente para melhorar monotonicamente a política conjunta.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas e alocação de recursos em uma rede MEC colaborativa ar-solo assistida por múltiplos UAVs, na qual recursos de borda aérea e de nuvem são usados para melhorar QoS em aplicações sensíveis a latência. Adota a métrica Age of Processing (AoP) para medir a frescor dos resultados processados e formula um problema de minimização do AoP médio e do consumo de energia dos UAVs, sujeito a restrições de acesso de usuários e recursos, por meio da otimização conjunta de associação usuário-UAV, alocação de recursos, razões de offloading e potência de transmissão. Para resolver o problema não convexo, modela-o como POMDP e propõe o algoritmo cooperativo HAPPO, com atualização sequencial de políticas em CTDE para mitigar ineficiências causadas pela sobreposição de cobertura entre UAVs. Simulações mostram que a abordagem supera outras alternativas em desempenho e adaptabilidade em ambientes dinâmicos.
