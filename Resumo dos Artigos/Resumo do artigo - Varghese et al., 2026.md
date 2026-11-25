[[Atv1 - Parte 4 - Entrega Final]]


**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Access**, que propõe uma arquitetura de coordenação centralizada para alocação e execução de tarefas em sistemas multi-robôs heterogêneos, usando um algoritmo híbrido (SVCA + NSGA-II), com replanejamento dinâmico e gestão autônoma de bateria, validado por simulação em Gazebo com ROS 2.

---

### 📌 Metadados do Artigo
*   **Título:** Hybrid Coordination Framework for Centralized Task Allocation and Execution in Heterogeneous Multi-Robot Systems
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** IEEE Access
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (Gazebo com ROS 2 Humble)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Cinco robôs móveis heterogêneos com diferentes capacidades de carga útil, velocidades médias, taxas de consumo de energia e tempos de carga/descarga, operando em cenários de armazém com múltiplas tarefas logísticas.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization; Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS 2 (Humble) |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema adota uma arquitetura de coordenação **centralizada**, na qual um controlador central mantém conhecimento global do estado dos robôs e das tarefas e executa a alocação usando um algoritmo híbrido que combina o **Shapley Value Clustering Algorithm (SVCA)** com o **NSGA-II**. O SVCA agrupa tarefas/robôs para reduzir o espaço de busca, e o NSGA-II otimiza múltiplos objetivos conflitantes (makespan, consumo de energia, cumprimento de prazos e balanceamento de carga). A arquitetura inclui replanejamento dinâmico: ao concluir uma tarefa e retornar à estação de estacionamento, o robô pode detectar e executar tarefas pendentes próximas; e gestão autônoma de energia, que aciona recarga quando o nível de bateria atinge um limiar predefinido. A implementação usa ROS 2 Humble, com comunicação explícita entre o controlador central e os robôs, e validação em Gazebo com cenários de armazém.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de alocação de tarefas logísticas para robôs móveis heterogêneos com diferentes capacidades de carga, consumo de energia, prazos e velocidades, buscando equilibrar qualidade da solução, eficiência computacional e adaptabilidade em tempo real. Propõe uma arquitetura de coordenação centralizada que integra SVCA e NSGA-II para alocação multi-robô de tarefas (MRTA), otimizando simultaneamente makespan, consumo de energia, aderência a prazos e balanceamento de carga. O sistema inclui replanejamento dinâmico de tarefas e gestão autônoma de recarga de bateria. A validação é feita em Gazebo com cinco robôs heterogêneos e múltiplas tarefas logísticas, alcançando 100% de alocação de tarefas com tempo médio de 0,122 segundos, superando IMGA, SVCA, PSO, GA e NSGA-II isolado, e demonstrando convergência em cerca de 30 gerações.