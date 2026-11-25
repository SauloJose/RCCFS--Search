[[Atv1 - Parte 4 - Entrega Final]]


**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Automation Science and Engineering**, que propõe o framework **SLEI3D** para exploração e inspeção simultâneas com frotas heterogêneas de UAVs/UGVs sob comunicação limitada, validado por simulação em larga escala e experimentos com hardware.

---

### 📌 Metadados do Artigo
*   **Título:** SLEI3D: Simultaneous Exploration and Inspection via Heterogeneous Fleets Under Limited Communication
*   **DOI:** 10.1109/TASE.2025.3643166
*   **Publicação (Veículo/Evento):** IEEE Transactions on Automation Science and Engineering
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação; Testbed/Real-world

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Frota heterogênea composta por *explorers* equipados com LiDAR de longo alcance, *inspectors* equipados com câmeras de curto alcance e uma estação de controle móvel (GCS). Nos experimentos de hardware, são usados 7 robôs, incluindo UGVs e UAVs; nas simulações, missões com até 48 robôs.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization; Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O framework adota uma coordenação hierárquica em duas camadas e múltiplas escalas de tempo. Na camada superior, a GCS móvel coordena com os *explorers* por meio de um protocolo de comunicação intermitente, alocando *bounding boxes* (BBoxes), coletando mapas e resultados de inspeção e negociando local/tempo dos próximos encontros. Na camada inferior, dentro de cada subgrupo, o *explorer* coordena os *inspectors* via protocolo proativo, alocando áreas de interesse (AoIs) e planejando trajetórias de inspeção. O processamento de SLAM, navegação, exploração e inspeção ocorre localmente nos robôs; a comunicação só ocorre quando há linha de visada e proximidade dentro do alcance ad-hoc.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de exploração e inspeção simultâneas de ambientes desconhecidos por frotas heterogêneas de UAVs/UGVs, sob comunicação limitada, com necessidade de reportar descobertas em tempo hábil a uma estação de controle móvel. Propõe o framework SLEI3D, que integra exploração colaborativa 3D, inspeção adaptativa e comunicação oportuna por meio de protocolos intermitentes e proativos, com planejamento multi-camada e multi-taxa. O método aloca BBoxes e AoIs, planeja trajetórias de inspeção e negocia encontros de comunicação para minimizar o tempo total de missão. A validação inclui simulações de alta fidelidade com até 48 robôs e 384 mil m³, além de experimentos de hardware com 7 robôs, demonstrando eficiência, confiabilidade e robustez a falhas de robôs e perda de comunicação.