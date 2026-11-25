[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo de **Survey** que revisa protocolos de roteamento em redes veiculares aéreas não tripuladas (FANETs/UAVs), detalhando métodos de construção, métricas de desempenho, topologias de comunicação e áreas de pesquisa aberta.

---

### 📌 Metadados do Artigo
*   **Título:** A Fresh Look at Routing Protocols in Unmanned Aerial Vehicular Networks: A Survey
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** Não especificado no texto
*   **Ano:** 2023

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Survey
*   **Tipo de Validação:** Não especificado (survey)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Não especificado (survey abrange múltiplos sistemas multi-UAV)
*   **Descrição da Frota:** Não especificado. O artigo revisa redes de UAVs/FANETs em geral, incluindo múltiplos UAVs e estações terrestres, sem uma frota específica proposta ou validada.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Outro (Roteamento/Comunicação) |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Não especificado (survey; protocolos variam) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (RF); Cellular; Long-range |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Nenhum |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O survey analisa redes FANETs formadas por UAVs que se comunicam entre si e com estações terrestres. São discutidas topologias star, mesh, cluster-based e híbrida, com estações terrestres conectadas diretamente a UAVs ou a cluster heads. Os protocolos revisados operam de forma embarcada nos UAVs, usando troca explícita de pacotes de controle (RREQ, RREP, hello, beacons etc.) e estratégias reativas, geográficas, oportunistas, clusterizadas e bioinspiradas. O foco está no roteamento sob alta mobilidade, topologia dinâmica, enlaces intermitentes e restrições de energia.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo apresenta uma revisão abrangente de protocolos de roteamento recentemente desenvolvidos para comunicação em redes de UAVs/FANETs. Ele descreve o funcionamento de protocolos como BR-AODV, RGR, eAntHocNet, JarmRout, CORF, LA, SecRIP, entre outros, e discute os desafios de roteamento decorrentes de alta mobilidade, topologia fluida, enlaces intermitentes, restrições de energia e mudanças na qualidade dos enlaces. O survey propõe métricas de desempenho para comparar eficiência, estabilidade e confiabilidade dos protocolos, analisa suas forças e limitações e identifica áreas abertas de pesquisa em roteamento para redes veiculares aéreas.
