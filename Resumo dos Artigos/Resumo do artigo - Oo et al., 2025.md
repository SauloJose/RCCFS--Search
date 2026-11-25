[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado no **Journal of Industrial Information Integration** (Elsevier), que propõe um framework de **Digital Twin** com camada de integração de informações e interface de **Realidade Virtual** para montagem colaborativa de peças não organizadas por múltiplos robôs, com validação experimental em bancada física e gêmeo digital.

---

### 📌 Metadados do Artigo
*   **Título:** Digital twin-enabled multi-robot system for collaborative assembly of unorganized parts
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** Journal of Industrial Information Integration (Elsevier)
*   **Ano:** 2025

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Testbed/Real-world (bancada física com gêmeo digital e interface VR)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Homogênea
*   **Descrição da Frota:** Duas estações robóticas colaborativas (braços robóticos) montadas em uma bancada de montagem, com garras e controladores. O sistema inclui uma câmera na estação de montagem e uma estação de preparação de informações das peças. A frota robótica é composta por robôs colaborativos similares entre si.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O framework é composto por um **mundo físico** (robôs colaborativos, câmera, estação de preparação de peças, operador) e um **mundo digital** (gêmeo digital dos robôs, módulos de planejamento de montagem, modificação de programas, controle em tempo real, reconhecimento de peças e integração de informações). A camada de **integração de informações** faz a ponte entre os dois mundos, gerenciando dados OT (valores de juntas, status de garras, sensores em tempo real) e dados IT (arquivos CAD, imagens, instruções de modificação). O operador usa uma interface de **Realidade Virtual imersiva** e controladores para planejar, modificar e treinar os robôs no mundo virtual, sem interromper a operação física. O módulo de planejamento de montagem gera programas livres de colisão para cada configuração estável das peças, e o módulo de reconhecimento de peças usa processamento de imagens para identificar peças em orientações aleatórias. Os programas são armazenados e chamados conforme a orientação detectada. A execução física é feita pelos robôs colaborativos, com monitoramento em tempo real.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de montagem colaborativa por múltiplos robôs de peças complexas que chegam à estação em posições e orientações aleatórias, demanda típica de produção personalizada de pequenos lotes. Propõe um framework de Digital Twin com uma camada de integração de informações que permite ao operador humano implantar suas habilidades por meio de uma interface de Realidade Virtual para planejar, simular, modificar e treinar programas de montagem sem interromper a operação física. O sistema usa processamento de imagens para reconhecer peças em orientações aleatórias, gera programas livres de colisão para cada configuração estável e seleciona o programa adequado com base na orientação detectada. A validação é feita em uma bancada física com gêmeo digital e interface VR, demonstrando a viabilidade do fluxo de informações entre os mundos físico e digital, o planejamento de montagem, a modificação de programas e o controle em tempo real.