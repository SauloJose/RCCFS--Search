[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Robotics and Automation Letters**, que propõe o framework **Swarm-SLAM**, um sistema de SLAM colaborativo (C-SLAM) descentralizado, esparso e escalável para sistemas multi-robô, com suporte a lidar, câmeras estéreo e RGB-D, priorização espectral de loop closures e comunicação ad-hoc, validado por datasets e experimento real com três robôs.

---

### 📌 Metadados do Artigo
*   **Título:** Swarm-SLAM: Sparse Decentralized Collaborative Simultaneous Localization and Mapping Framework for Multi-Robot Systems
*   **DOI:** 10.1109/LRA.2023.3333743
*   **Publicação (Veículo/Evento):** IEEE Robotics and Automation Letters
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (datasets); Testbed/Real-world (três robôs em rede ad-hoc)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Três robôs explorando e mapeando um ambiente indoor, comunicando-se por rede ad-hoc. O framework é genérico e suporta sensores lidar, estéreo e RGB-D, mas o experimento real utilizou robôs similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization; Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc; Opportunistic |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS 2 |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O Swarm-SLAM é composto por três módulos principais: **neighbor management**, **front-end** e **back-end**. O gerenciamento de vizinhos rastreia quais robôs estão ao alcance de comunicação e quais dados já foram trocados, usando mensagens de heartbeat periódicas. O front-end extrai descritores globais (ScanContext para lidar, CosPlace para imagens) e os compartilha para reconhecimento de lugar; uma nova técnica de **priorização espectral de loop closures** baseada na maximização da conectividade algébrica do grafo de poses seleciona um subconjunto orçamentado de candidatos, reduzindo a comunicação antes da verificação geométrica. O back-end realiza otimização descentralizada de grafo de poses com o solver Graduated Non-Convexity (GNC), com um robô dinamicamente eleito entre os que estão ao alcance para executar a otimização, e um processo de seleção de âncora mantém um referencial global consistente entre encontros esporádicos. Todo o processamento é embarcado nos robôs, sem autoridade central, e a comunicação é peer-to-peer e esporádica via redes ad-hoc.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de SLAM colaborativo (C-SLAM) para sistemas multi-robô em ambientes sem GPS, nos quais soluções centralizadas sofrem com gargalos de comunicação e baixa escalabilidade. Propõe o Swarm-SLAM, um framework open-source descentralizado, escalável, flexível e esparso, que suporta lidar, câmeras estéreo e RGB-D. O sistema introduz uma técnica de priorização de loop closures inter-robô baseada na maximização da conectividade algébrica do grafo de poses, que reduz o volume de comunicação ao selecionar candidatos mais informativos antes da verificação geométrica. Inclui ainda um sistema de gerenciamento de vizinhos para redes ad-hoc e um back-end descentralizado de otimização de grafo de poses com seleção de âncora para manter consistência global. A avaliação é feita em cinco datasets (KITTI, KITTI360, GrAco, M2DGR) e em um experimento real com três robôs comunicando-se por rede ad-hoc, demonstrando localização e mapeamento colaborativos eficazes com menor uso de comunicação em comparação com abordagens anteriores.