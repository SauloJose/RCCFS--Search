[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado em veículo Springer, que propõe um framework de offloading de tarefas impulsionado por **Digital Twin** para redes VECN assistidas por UAVs, com decisão descentralizada e avaliação centralizada via A3C e GAT, validado por simulação com dataset real de requisições.

---

### 📌 Metadados do Artigo
*   **Título:** Enhancing UAV-assisted vehicle edge computing networks through a digital twin-driven task offloading framework
*   **DOI:** Não especificado
*   **Publicação (Veículo/Evento):** Springer Science+Business Media
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs despachados por uma estação base, atuando como nós de offloading e também como relays. A rede inclui RSUs e OBUs como nós terrestres, mas a frota robótica é composta apenas por UAVs.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A arquitetura física é composta por uma estação base central, múltiplos UAVs, RSUs e OBUs. A estação base despacha UAVs e mantém a avaliação centralizada do estado global. Cada UAV toma decisões de offloading de forma descentralizada, podendo descarregar localmente para uma RSU ou encaminhar via relay para outro UAV. Sobre a rede física, uma camada de Digital Twin (DT-UAVs e DT-RSUs) replica o estado e a topologia em tempo real. O aprendizado utiliza A3C com GAT para avaliar o estado global no lado da estação base, enquanto cada UAV atualiza independentemente sua política. O processamento é híbrido e a avaliação é centralizada.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** Aborda o problema de offloading em VECNs assistidas por UAVs, especialmente em cenários de congestionamento ou falhas de infraestrutura. Propõe um framework DT com execução descentralizada e avaliação centralizada baseado em A3C, integrando GAT para incorporar a topologia dinâmica do DT à avaliação de estado. O problema é formulado como POMDP com objetivos de maximizar throughput, minimizar atraso e equilibrar carga. A validação usa simulação multi-UAV e dataset real de requisições, demonstrando melhor throughput e estabilidade em cenários de sobrecarga local e ambiente dinâmico.