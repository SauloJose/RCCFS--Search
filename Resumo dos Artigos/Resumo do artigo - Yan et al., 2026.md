[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Consumer Electronics**, que propõe o algoritmo **LMADRL-UTRCS**, combinando otimização de Lyapunov e aprendizado por reforço profundo multiagente (MADRL) para otimização conjunta de trajetórias de UAVs e coordenação de recursos de borda em sistemas de computação de borda assistidos por múltiplos UAVs, validado por simulação.

---

### 📌 Metadados do Artigo
*   **Título:** Joint UAV Trajectory Optimization and Edge-End Resource Coordination via Lyapunov-Guided Multi-Agent DRL
*   **DOI:** 10.1109/TCE.2025.3649242
*   **Publicação (Veículo/Evento):** IEEE Transactions on Consumer Electronics
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos UAVs (L UAVs) equipados com capacidades de computação de borda, operando em espaço 3D sem restrição fixa de altitude, atendendo M dispositivos IoT industriais (IoTDs) estáticos no solo. Os UAVs são similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (CTDE: treinamento centralizado, execução descentralizada) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Optimization (Lyapunov) |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Não especificado |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema é uma rede ar-solo com L UAVs equipados com módulos leves de inteligência de borda e M IoTDs no solo. Cada IoTD pode executar a tarefa localmente, descarregá-la totalmente para um UAV ou fazer offloading parcial, dividindo a tarefa entre processamento local e envio de porções para múltiplos UAVs. O problema é formulado como um MINLP estocástico multi-estágio que otimiza conjuntamente partição de tarefas, potência de transmissão, frequência de computação local e trajetórias dos UAVs. A otimização de Lyapunov decompõe o problema de longo prazo em subproblemas determinísticos por slot, garantindo estabilidade das filas e consumo médio de energia limitado. Cada subproblema é modelado como um MDP multiagente, resolvido pelo algoritmo LMADRL-UTRCS com actor-critic, redes alvo, estimadores duplos e exploração ε-greedy escalonada, em CTDE. O processamento é híbrido (local nos IoTDs e nos UAVs) e a execução das políticas é descentralizada nos IoTDs.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de offloading de tarefas e coordenação de recursos em sistemas de computação de borda assistidos por múltiplos UAVs, no qual IoTDs com recursos limitados precisam processar tarefas computacionalmente intensas sob canais dinâmicos, mobilidade e restrições de energia. Formula um MINLP estocástico multi-estágio para minimizar o consumo total de energia do sistema, otimizando conjuntamente partição de tarefas, potência de transmissão, frequência de computação local e trajetórias 3D dos UAVs. Usa otimização de Lyapunov para decompor o problema de longo prazo em subproblemas por slot, garantindo estabilidade de filas, e modela cada subproblema como um MDP multiagente. Propõe o algoritmo LMADRL-UTRCS, baseado em actor-critic com redes alvo e estimadores duplos, em regime de treinamento centralizado e execução descentralizada. Simulações mostram convergência mais rápida, menor consumo de energia e planejamento de trajetória mais eficiente em comparação com métodos de referência.