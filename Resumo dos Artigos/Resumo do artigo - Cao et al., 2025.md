[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Mobile Computing**, que propõe o algoritmo **SAMARL**, um método escalável de aprendizado por reforço profundo multiagente com atenção multi-head, e um framework de treinamento impulsionado por **Digital Twin** para busca cooperativa de alvos por enxames de AAVs, com transferência sim-to-real, validado por simulação e experimentos reais de voo.

---

### 📌 Metadados do Artigo
*   **Título:** AAV Swarm Cooperative Search Based on Scalable Multiagent Deep Reinforcement Learning With Digital Twin-Enabled Sim-to-Real Transfer
*   **DOI:** 10.1109/TMC.2025.3530438
*   **Publicação (Veículo/Evento):** IEEE Transactions on Mobile Computing
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação; Testbed/Real-world

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Enxame de AAVs (autonomous aerial vehicles) de escala variável, com sensoriamento e comunicação limitados, realizando busca cooperativa de fontes de sinal desconhecidas em ambientes dinâmicos com ameaças. Experimentos reais envolveram enxames de diferentes tamanhos e áreas de missão de diferentes escalas.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (CTDE: treinamento centralizado, execução descentralizada) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot; Hybrid (treinamento em DT) |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado (rádio de comunicação) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é um enxame de AAVs distribuído que realiza busca cooperativa de alvos em uma área discretizada em grid. Cada AAV mantém um mapa individual de probabilidade de alvo, atualizado por regra bayesiana a partir de detecções imperfeitas, e troca informações com vizinhos dentro do alcance de comunicação. Cada agente executa uma política descentralizada (SAMARL) que observa apenas uma região de campo de visão (FOV) com representação em grafo e mapa de cognição ambiental, escolhendo entre cinco ações discretas (norte, sul, leste, oeste, parado). O treinamento é feito em um framework de Digital Twin com três fases (“twin training, decentralized execution, continuous evolution”), que combina controle de voo real, ferramentas de simulação de comunicação e motor de física 3D para reduzir o gap sim-to-real. O SAMARL estende o MAPPO com mecanismo de atenção multi-head e função de recompensa composta por cognição de exploração, alvo encontrado, consumo de tempo, cobertura de área e segurança colaborativa. A execução é embarcada nos AAVs, com comunicação explícita entre vizinhos para compartilhamento de mapas e detecções.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de busca cooperativa de alvos (CTS) por enxames de AAVs em ambientes desconhecidos e dinâmicos com ameaças, no qual os veículos têm sensoriamento e comunicação limitados e os métodos tradicionais carecem de escalabilidade e colaboração eficiente. Propõe o SAMARL, um algoritmo de aprendizado por reforço multiagente escalável baseado em MAPPO com atenção multi-head, que utiliza um espaço de observação com representação em grafo e mapa de cognição ambiental para considerar taxa de busca, cobertura de área e segurança. Propõe também um framework de treinamento impulsionado por Digital Twin para evolução contínua dos modelos e transferência sim-to-real, além de um sistema de validação distribuído com controle de voo real, simulação de comunicação e motor de física 3D. Extensas simulações mostram superioridade sobre o estado da arte, e experimentos reais de voo com diferentes escalas de área e enxame demonstram generalização e escalabilidade dos modelos treinados.