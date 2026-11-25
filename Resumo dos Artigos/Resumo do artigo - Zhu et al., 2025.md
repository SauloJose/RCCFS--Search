[[Atv1 - Parte 4 - Entrega Final]]

# 📄 Artigo 7 — Zhu et al. (2025)

**O que é:** Artigo científico do tipo **Solution**, publicado na revista **Sensors** (MDPI), que propõe o algoritmo **LLM-QTRAN** para planejamento de trajetória e offloading de tarefas em computação de borda assistida por UAVs, combinando LLM, QTRAN, GCN e self-attention, com validação por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Task Offloading with LLM-Enhanced Multi-Agent Reinforcement Learning in UAV-Assisted Edge Computing
*   **DOI:** 10.3390/s25010175
*   **Publicação (Veículo/Evento):** Sensors (MDPI)
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs rotativos equipados com servidores de computação de borda, atuando como nós aéreos de MEC para atender equipamentos de usuário (UEs). O número exato de UAVs não é fixado no modelo; a frota é composta por UAVs similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Robot |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Não especificado |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (TDMA) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é uma rede de MEC assistida por UAVs, na qual UAVs equipados com servidores de borda atendem UEs que descarregam tarefas computacionais. A comunicação ar-solo é modelada com enlace LoS e acesso TDMA, e o offloading é binário: a tarefa é integralmente descarregada para o UAV mais próximo dentro da cobertura. O problema de controle de trajetória é formulado como um Dec-POMDP, com treinamento centralizado e execução descentralizada (CTDE). O algoritmo LLM-QTRAN usa um LLM para decompor a área em regiões, GCN e self-attention para capturar relações inter-regionais e QTRAN para decomposição de valor. Cada UAV toma decisões locais de rumo e velocidade com base em observações parciais, enquanto a coordenação global é facilitada pela decomposição regional e pelo mecanismo de atenção.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de planejamento de trajetória e offloading de tarefas em computação de borda assistida por múltiplos UAVs, no qual os UAVs têm apenas observabilidade parcial e precisam maximizar a taxa de conclusão de tarefas. Propõe o algoritmo LLM-QTRAN, que integra um LLM para decomposição regional, GCN e self-attention para modelar relações entre sub-regiões e o algoritmo QTRAN para decomposição de valor em um cenário cooperativo Dec-POMDP. O modelo considera enlaces LoS, acesso TDMA, offloading binário, restrições de cobertura, deslocamento máximo, capacidade computacional e número máximo de usuários por UAV. Os resultados de simulação mostram que o método supera algoritmos de DRL existentes, com ganhos superiores a 10% em velocidade de convergência e taxa de conclusão de tarefas.