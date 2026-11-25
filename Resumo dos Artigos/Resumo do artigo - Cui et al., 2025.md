[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Automation Science and Engineering**, que propõe uma arquitetura de controle resiliente em duas camadas (Twin Layer e Cyber-Physical Layer) para consenso de sistemas multi-UAV heterogêneos sob ataques bizantinos de aresta e de nó, com líder de entrada desconhecida, validado por experimento real de voo de enxame de UAVs.

---

### 📌 Metadados do Artigo
*   **Título:** Resilient Consensus Control of Heterogeneous Multi-UAV Systems With Leader of Unknown Input Against Byzantine Attacks
*   **DOI:** 10.1109/TASE.2024.3420697
*   **Publicação (Veículo/Evento):** IEEE Transactions on Automation Science and Engineering
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Testbed/Real-world

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Sistema multi-UAV com N+1 drones, sendo N seguidores com dinâmicas distintas (parâmetros α_si e α_vi diferentes por agente) e 1 líder com entrada desconhecida. A heterogeneidade está nas diferentes dinâmicas dos seguidores. O experimento de validação é um voo de enxame de UAVs.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Motion |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O artigo propõe uma arquitetura de controle resiliente em duas camadas inspirada em Digital Twin: uma **Twin Layer (TL)** virtual, imune a ataques bizantinos de nó, e uma **Cyber-Physical Layer (CPL)** física. Um governador da TL reconfigura a topologia adicionando um número mínimo de arestas-chave para garantir robustez forte (2f+1). Na TL, estimadores distribuídos baseados em funções de sinal estimam o estado do líder; na CPL, controladores descentralizados sem chattering garantem convergência exponencial do erro de rastreamento. As duas camadas compartilham a mesma topologia, e a TL atua como modelo virtual de backup, permitindo desacoplar as defesas contra ataques de aresta (na TL) e ataques de nó (na CPL). A execução dos controladores é embarcada nos UAVs, com troca explícita de informações entre vizinhos.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de controle de consenso de sistemas multi-UAV heterogêneos sob ataques bizantinos, nos quais drones comprometidos transmitem valores falsos aos vizinhos e aplicam entradas incorretas a si mesmos, com um líder de entrada desconhecida. Propõe uma arquitetura hierárquica em duas camadas inspirada em Digital Twin, que separa as defesas em ataques de aresta na Twin Layer e ataques de nó na Cyber-Physical Layer. Na TL, uma estratégia de reconfiguração de topologia adiciona arestas mínimas para garantir robustez forte (2f+1), e estimadores distribuídos baseados em sinal estimam o estado do líder. Na CPL, controladores descentralizados garantem consenso resiliente com convergência exponencial. A eficácia e praticidade dos resultados teóricos são verificadas por um experimento real de voo de enxame de UAVs.