[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **IEEE Transactions on Automation Science and Engineering**, que propõe um método leve de SLAM visual-inercial multi-robô assistido por borda (edge) com comunicação eficiente, usando rastreamento de fluxo óptico predito por IMU e compressão sem perdas de features, validado por experimentos no dataset EuRoC.

---

### 📌 Metadados do Artigo
*   **Título:** Edge-Assisted Multi-Robot Visual-Inertial SLAM With Efficient Communication
*   **DOI:** 10.1109/TASE.2024.3376427
*   **Publicação (Veículo/Evento):** IEEE Transactions on Automation Science and Engineering
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (experimentos no dataset EuRoC; não há implantação em robôs reais reportada no trecho)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Múltiplos robôs equipados com sensores visuais-inerciais (câmera monocular + IMU), organizados em um sistema centralizado de SLAM multi-robô com arquitetura hierárquica robô-edge-cloud. A infraestrutura inclui servidores de borda e nuvem; os robôs são similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Motion; Tasks (localização e mapeamento) |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Optimization; Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid (Robot-Edge-Cloud) |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado (baseado em ORB-SLAM3) |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O sistema adota uma arquitetura hierárquica em três camadas: **robô**, **edge** e **cloud**. No robô, realiza-se detecção rápida de features e rastreamento de fluxo óptico LK assistido por IMU para frames não-chave, enquanto descritores ORB são calculados apenas em frames-chave. No **edge**, executa-se o front-end de VIO em tempo real, estimando a pose da frame atual por rastreamento de fluxo óptico e mantendo um mapa local de tamanho limitado para cada agente. Na **cloud**, executam-se tarefas globalmente custosas e não críticas em tempo real: eliminação de keyframes redundantes, fechamento de loop, PGO e GBA, além da fusão de mapas global. A comunicação entre robô, edge e cloud transmite apenas pontos-chave e descritores de keyframes, com codificação e compressão sem perdas, reduzindo a largura de banda sem perda de precisão. A arquitetura é centralizada e o processamento é híbrido entre as três camadas.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de SLAM visual-inercial multi-robô com consistência global e tempo real sob limitações de largura de banda e recursos computacionais embarcados. Propõe um método leve de SLAM baseado em ORB-SLAM3 e fluxo óptico esparso de Lucas-Kanade, no qual o cálculo de descritores ocorre apenas em keyframes e o rastreamento entre frames não-chave usa fluxo óptico predito por pré-integração de IMU em pirâmide. Sobre esse método, propõe um sistema centralizado de SLAM multi-robô com arquitetura robô-edge-cloud, que desacopla extração de features, VIO e otimização global. A comunicação transmite apenas pontos-chave e descritores de keyframes com codificação e compressão sem perdas, e introduz map backbone profiling (MBP) para eficiência de otimização e armazenamento. Experimentos no dataset EuRoC mostram menor volume de dados transmitidos em comparação com métodos de compressão de features do estado da arte e precisão de localização igual ou superior sob baixa carga computacional.