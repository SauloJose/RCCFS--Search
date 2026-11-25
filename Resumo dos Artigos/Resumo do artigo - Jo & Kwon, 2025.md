[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Access**, que propõe um mecanismo de geração e compartilhamento de informações críticas em tempo real e uma estratégia de alocação de tarefas para sistemas multi-robô cooperativos, utilizando arquitetura descentralizada e assíncrona baseada em QoS do ROS 2 e middleware DDS, validado por simulação e experimentos com robôs reais.

---

### 📌 Metadados do Artigo
*   **Título:** Generation of Critical Information and Sharing Mechanism for Multi-Robot Mission Success
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** IEEE Access, Vol. 13, 2025
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação; Testbed/Real-world

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos robôs móveis TurtleBot3 operando em ambientes de armazém, com plataformas idênticas nos experimentos de simulação (Gazebo) e reais (laboratório). O framework é projetado para ser extensível a frotas heterogêneas, mas a validação experimental utilizou uma frota homogênea.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | WLAN (Wi-Fi) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS 2 (DDS) |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema adota uma arquitetura **descentralizada e assíncrona** baseada em ROS 2 e no middleware DDS, sem controlador central. Cada robô gera **informações críticas** (obstáculos, zonas de perigo) a partir de análise contextual do ambiente e as compartilha seletivamente com outros robôs usando **perfis de QoS** diferenciados: dados críticos (alertas de obstáculos, zonas de perigo) usam políticas `RELIABLE` e `TRANSIENT_LOCAL` para garantir entrega; dados volumosos e menos sensíveis ao tempo (atualizações de mapa) usam `BEST_EFFORT` e `VOLATILE` para conservar largura de banda. A **alocação de tarefas** é distribuída e baseada em custo, avaliando relevância e proximidade em tempo real, com realocação dinâmica conforme mudanças no ambiente ou no desempenho dos robôs. O **planejamento de caminho** usa o framework Nav2 com planejadores globais (A*, ACO) e locais (DWA, AMCL). O sistema é projetado para ser modular e escalável, com separação entre sensoriamento, raciocínio e comunicação, e inclui integração conceitual de **transfer learning** para adaptação a novos ambientes. O processamento é embarcado nos robôs e a comunicação é explícita via Wi-Fi.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de compartilhamento de informações em tempo real e alocação de tarefas em sistemas multi-robô cooperativos operando em ambientes incertos e dinâmicos, nos quais arquiteturas centralizadas sofrem com baixa escalabilidade e ponto único de falha. Propõe um mecanismo de geração de informações críticas e compartilhamento assíncrono baseado em QoS do ROS 2/DDS, no qual cada robô identifica e prioriza informações relevantes para a missão (obstáculos, zonas de perigo) e as dissemina com políticas de QoS adequadas à criticidade. A alocação de tarefas é distribuída, baseada em custo e com realocação dinâmica, e o planejamento de caminho combina planejadores globais e locais do Nav2. A validação inclui experimentos em simulação (Gazebo) e com robôs reais TurtleBot3 sob diferentes condições de rede, avaliando atraso de mensagem, tempo de reação, perda de pacotes e taxa de sucesso da missão. Resultados mostram que as configurações `RELIABLE` e `TRANSIENT_LOCAL` proporcionam o desempenho mais consistente para transmissão de informações de obstáculos e atualizações de mapa, e que o framework é robusto e adaptável a restrições de comunicação, com potencial para implantação em frotas heterogêneas.