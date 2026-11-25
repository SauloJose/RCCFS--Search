[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Vehicular Technology**, que propõe um esquema de caching colaborativo multi-UAV habilitado por NOMA para redes 6G, com alocação de recursos e planejamento de trajetória 3D baseados em DRL, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** DRL-Based Resource Allocation and Trajectory Planning for NOMA-Enabled Multi-UAV Collaborative Caching 6G Network
*   **DOI:** 10.1109/TVT.2024.3357086
*   **Publicação (Veículo/Evento):** IEEE Transactions on Vehicular Technology
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs com capacidade de cache e comunicação, atuando como nós de borda aérea para entrega de conteúdo a usuários móveis. O sistema inclui ainda uma HAPS (High Altitude Platform Station) como relay/backhaul e servidores em nuvem, mas a frota robótica é composta por UAVs similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Cellular; Other (NOMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A rede é composta por uma HAPS, múltiplos UAVs com cache, usuários móveis e servidores em nuvem. Os UAVs armazenam conteúdos populares e os entregam diretamente aos usuários via enlaces U-M; quando o conteúdo não está no UAV associado, ele pode ser obtido de outro UAV por meio da HAPS (enlaces U-H) ou, em último caso, da nuvem via feeder link. O acesso é habilitado por NOMA, com reuso de subcanais ortogonais e alocação de potência. O problema conjunto de caching, trajetória 3D e alocação de espectro é decomposto em dois subproblemas: decisões de caching colaborativo via MAPPO e otimização de trajetória/potência/canal via matching-DRL. O treinamento é centralizado, mas a execução das decisões é distribuída entre os UAVs, com processamento híbrido entre UAVs, HAPS e nuvem.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo investiga uma rede 6G de caching colaborativo multi-UAV habilitada por NOMA, na qual UAVs armazenam conteúdos populares e cooperam para entregá-los a usuários móveis em áreas de hotspot, aliviando o backhaul e reduzindo a latência. Formula um problema conjunto de decisão de caching, planejamento de trajetória 3D e alocação de recursos de espectro/potência para minimizar o atraso de recuperação de conteúdo, considerando a dinamicidade da popularidade dos conteúdos. Como o problema é NP-hard e não convexo, decompõe-no em dois subproblemas: caching colaborativo, resolvido por MAPPO, e otimização conjunta de trajetória, potência e reuso de canais, resolvida por uma abordagem matching-DRL com DDPG. As simulações mostram convergência rápida e melhor desempenho em taxa de acerto de cache, atraso de recuperação e throughput em comparação com benchmarks.