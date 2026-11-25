[[Atv1 - Parte 4 - Entrega Final]]


**O que é:** Artigo científico do tipo **Solution**, publicado na **Engineering Applications of Artificial Intelligence** (Elsevier), que propõe um método de alocação de tarefas para colaboração humano-robô em montagem, combinando **Digital Twin**, **Realidade Aumentada** e **aprendizado por reforço com transferência** (MA-PPO + destilação de conhecimento), validado por estudo de caso.

---

### 📌 Metadados do Artigo
*   **Título:** A transfer reinforcement learning and digital-twin based task allocation method for human-robot collaboration assembly
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** Engineering Applications of Artificial Intelligence (Elsevier), Vol. 144, 2025, artigo 110064
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (com dados de simulação AR/DT e estudo de caso; não há implantação física em larga escala reportada no trecho)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Sistema de colaboração humano-robô composto por um trabalhador humano e um robô colaborativo (braço robótico) em uma estação de montagem, com ferramentas e componentes. O estudo de caso utiliza montagem de volante de direção com AGV. Não é uma frota multi-robô; trata-se de um time humano-robô.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (execução); treinamento centralizado (CTDE) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Offline (pré-treinamento e treinamento com dados de simulação); Online (execução da política) |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (TCP/IP, Bluetooth) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema usa um **Digital Twin** do ambiente de colaboração humano-robô, com modelos digitais do humano (corpo e mãos), do robô e dos componentes, sincronizados em tempo real com o espaço físico via captura de movimento, controlador do robô e HoloLens2. Antes da montagem física, um ambiente de simulação com **Realidade Aumentada** permite ao usuário executar subtarefas virtuais e coletar dados de execução (tempo, dificuldade, ergonomia, acessibilidade, segurança). Esses dados alimentam um framework de **aprendizado por reforço multiagente com transferência** baseado em MA-PPO e destilação de conhecimento: políticas pré-treinadas com randomização de domínio servem como professores para acelerar o aprendizado da política alvo em novas condições. O treinamento é centralizado (crítico central com informações globais) e a execução é descentralizada (atores locais), com o humano e o robô como agentes. A política treinada é sincronizada com o dispositivo AR para guiar o trabalhador e com o controlador do robô para executar as instruções.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de alocação de tarefas entre humanos e robôs em sistemas de montagem colaborativa, no qual modelos de decisão tradicionais dependem de grandes volumes de dados precisos de execução, frequentemente indisponíveis para novos produtos, novos trabalhadores ou mudanças de condições. Propõe um método baseado em Digital Twin e aprendizado por reforço com transferência: um ambiente AR/DT coleta dados de execução antes da montagem física; um algoritmo multiagente de RL (MA-PPO) pré-treina políticas com randomização de domínio; e um framework de transferência com destilação de conhecimento reutiliza o conhecimento pré-treinado para aprender rapidamente a política alvo com os dados coletados. Um estudo de caso de montagem de volante de direção com AGV demonstra a eficácia do método no treinamento e na tomada de decisão para múltiplos agentes humanos e robóticos.