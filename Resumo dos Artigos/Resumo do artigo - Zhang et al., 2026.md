[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Mobile Computing**, que propõe o algoritmo **SSAC-MGI** (Shared Soft Actor-Critic com Markov Game of Intervention) para planejamento seguro e energeticamente eficiente de trajetórias em redes MEC heterogêneas com múltiplos UAVs, combinando agendamento de jobs e alocação de recursos, validado por simulação com dados reais do cluster Alibaba.

---

### 📌 Metadados do Artigo
*   **Título:** Safe and Energy-Efficient Trajectory Planning for Heterogeneous Multi-UAV Enabled Mobile Edge Computing
*   **DOI:** 10.1109/TMC.2025.3632884
*   **Publicação (Veículo/Evento):** IEEE Transactions on Mobile Computing
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (trace-driven com dados do cluster Alibaba)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** N UAVs rotativos heterogêneos em termos de tipos de serviço pré-implantados e capacidades de recursos (CPU, memória) para executar instâncias de cada tipo de serviço. Cada UAV hospeda um subconjunto dos tipos de serviço disponíveis, e a união dos tipos entre todos os UAVs cobre toda a gama de requisições geradas pelos UEs. A frota atende M UEs estáticos ou móveis.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (DTDE: treinamento e execução descentralizados) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot (UAVs como nós de borda) |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (OFDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede MEC é composta por N UAVs heterogêneos e M UEs que geram requisições de jobs com tipos de serviço e requisitos de recursos diversos. Cada UAV é pré-configurado com um subconjunto de tipos de instâncias computacionais e capacidades de CPU/memória, introduzindo heterogeneidade entre UAVs. Os jobs chegam segundo um processo de Poisson e são compostos por múltiplas subtarefas que exigem o mesmo tipo de serviço; cada tarefa é executada por instâncias computacionais de granularidade fina. Os UAVs planejam trajetórias dinamicamente com base em restrições de tipo de serviço e recursos disponíveis, e os UEs se comunicam com os UAVs via OFDMA. O problema é formulado como um **Dec-POMDP** de dois agentes (um agente de segurança e um agente padrão por UAV) e resolvido pelo algoritmo **SSAC-MGI**, que combina uma arquitetura Shared Soft Actor-Critic para extrair características de UAVs heterogêneos com um mecanismo **two-agent Markov Game of Intervention (MGI)** para evitamento de colisões. O treinamento e a execução são descentralizados (DTDE), cada UAV decide com base apenas em observações locais, sem comunicação inter-UAV. Um método **Round-Robin** de alocação de instâncias é usado para atribuir instâncias computacionais às filas de workflow, melhorando a utilização de recursos e reduzindo a taxa de jobs perdidos.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de agendamento de jobs e alocação de recursos em redes MEC heterogêneas com múltiplos UAVs, nas quais os UAVs têm tipos de serviço e capacidades de recursos distintos, e os UEs têm distribuição desconhecida e chegadas de jobs com dinâmica espaço-temporal. O objetivo é reduzir a taxa de jobs perdidos e o consumo médio de energia de UAVs e UEs por meio do planejamento seguro de trajetórias e alocação de recursos embarcados. O problema é formulado como um Dec-POMDP e resolvido pelo algoritmo SSAC-MGI, que desacopla explicitamente o controle de segurança da otimização de desempenho por meio de um mecanismo de dois agentes (segurança e padrão) e utiliza uma arquitetura Shared Soft Actor-Critic com compartilhamento de políticas entre UAVs heterogêneos. O treinamento e a execução são descentralizados, sem comunicação inter-UAV, e um método Round-Robin aloca instâncias computacionais às filas de workflow. Simulações extensas baseadas em dados reais do cluster Alibaba validam a eficácia e superioridade do SSAC-MGI em comparação com algoritmos do estado da arte.
* 