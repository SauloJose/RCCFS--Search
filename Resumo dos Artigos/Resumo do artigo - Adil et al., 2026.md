[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo de **Survey** que revisa sistematicamente a gestão de comunicação em sistemas robóticos cooperativos aplicados à saúde (CRHS), abordando requisitos de QoS, tecnologias de rede, computação em edge/fog/cloud, aprendizado profundo e por reforço, além de desafios abertos e direções futuras.

---

### 📌 Metadados do Artigo
*   **Título:** Toward Effective Communication Management in Cooperative Robotic-Enabled Healthcare Systems: Open Challenges and Future Research Directions
*   **DOI:** 10.1109/JIOT.2025.3631333
*   **Publicação (Veículo/Evento):** IEEE Internet of Things Journal
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Survey
*   **Tipo de Validação:** Não especificado (survey)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Não especificado (survey abrange múltiplos sistemas cooperativos heterogêneos)
*   **Descrição da Frota:** Não especificado. O survey discute sistemas robóticos cooperativos em ambiente hospitalar (robôs cirúrgicos, de reabilitação, dispensação de medicamentos, telepresença e sanitização), sem uma frota específica proposta ou validada.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Resources; Outro (Comunicação/QoS) |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Não especificado |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Não especificado |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Cellular; Other (TSN, SDN/NFV, uRLLC) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O survey analisa arquiteturas de comunicação em sistemas robóticos cooperativos de saúde, com integração de camadas de edge, fog e cloud. Discute o uso de tecnologias como 5G/uRLLC, TSN, SDN/NFV e network slicing para prover baixa latência, alta confiabilidade e QoS previsível em ambientes hospitalares multi-robô. A comunicação é explícita entre robôs, sensores, servidores de farmácia e profissionais de saúde, com processamento distribuído entre robôs e infraestrutura de borda/nuvem. O survey destaca que aprendizado por reforço e aprendizado profundo podem melhorar o escalonamento e o offloading em cargas variáveis, mas não propõe uma arquitetura única.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo apresenta uma revisão sistemática (estilo PRISMA) sobre gestão de comunicação em sistemas robóticos cooperativos aplicados à saúde (CRHS). Analisa casos de uso como cirurgia robótica, reabilitação, dispensação de medicamentos, telepresença e controle de infecção, detalhando requisitos de QoS (latência, confiabilidade, largura de banda, jitter) para cada um. Examina tecnologias de comunicação e computação (5G, uRLLC, TSN, SDN, NFV, edge/fog/cloud) e o papel de DL e RL na melhoria do desempenho. A partir da análise de 178 artigos, identifica lacunas como falta de interoperabilidade entre fornecedores, ausência de benchmarks padronizados de QoS e limitações de adaptabilidade em ambientes dinâmicos. Por fim, propõe direções de pesquisa para superar esses desafios e viabilizar a implantação real da tecnologia.