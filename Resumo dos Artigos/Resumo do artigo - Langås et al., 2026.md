[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo de **Survey** (revisão sistemática da literatura) publicado no **Journal of Intelligent Manufacturing** (Springer), que explora a sinergia entre *human-robot teaming* (HRT), Digital Twins (DT) e Machine Learning (ML) no contexto da Indústria 5.0, propondo um framework unificado para os níveis de colaboração humano-robô e discutindo desafios, lacunas e direções futuras para manufatura sustentável.

---

### 📌 Metadados do Artigo
*   **Título:** Exploring the synergy of human-robot teaming, digital twins, and machine learning in Industry 5.0: a step towards sustainable manufacturing
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** Journal of Intelligent Manufacturing (Springer), Vol. 37, pp. 999–1022
*   **Ano:** 2026 (publicado online em 19 de fevereiro de 2025)

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Survey
*   **Tipo de Validação:** Não especificado (revisão sistemática da literatura)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Não especificado
*   **Descrição da Frota:** Não especificado. O artigo é uma revisão que discute conceitualmente times humano-robô (HRT), cobots, robôs quadrúpedes e outras plataformas em contextos de manufatura, mas não propõe ou valida uma frota específica.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Decentralized (HRT como time com troca de soluções) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid (edge computer + Digital Twin + robô físico) |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Não especificado |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Other (sensores 3D, IMU, sEMG, áudio, Mixed Reality) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O artigo revisa a progressão da integração humano-robô em direção à Indústria 5.0, definindo quatro estágios: **HRI** (troca de comandos), **HRC** (compartilhamento de espaço de trabalho), **pHRC** (troca de forças via contato físico, com controle de impedância/admitância) e **HRT** (troca de soluções, com humanos e robôs atuando como colegas de equipe). A arquitetura habilitadora do HRT combina **Digital Twin** (representação virtual de robôs e humanos, com sincronização em tempo real), **ML** (percepção, predição de ações humanas, tomada de decisão) e **interfaces de Realidade Mista (MR)** para operadores. O ambiente físico inclui sensores (câmeras 3D, IMU, sEMG, áudio, sensores de força/torque), atuadores e um **edge computer** que executa algoritmos em tempo real próximos à fonte de dados. O Digital Twin recebe dados em tempo real, atualiza a interface MR, realiza processamento para manutenção preditiva, percepção e controle, predição de ações humanas e tomada de decisão robótica. A arquitetura é centrada no humano, com foco em segurança, fatores humanos, design de interação, alocação de tarefas e adaptabilidade.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo revisa a literatura sobre a integração de *human-robot teaming* (HRT), Digital Twins (DT) e Machine Learning (ML) no contexto da Indústria 5.0 e manufatura sustentável. Propõe um framework unificado que define e diferencia os estágios de colaboração humano-robô — HRI, HRC, pHRC e HRT — com base nos tipos de troca (comandos, espaço de trabalho, forças e soluções). Discute como DT e ML habilitam percepção, predição e tomada de decisão integradas em sistemas industriais centrados no humano, incluindo o papel de interfaces de Realidade Mista e de sensores vestíveis e ambientais. Aborda aspectos éticos e filosóficos, como privacidade, autonomia e autoridade de decisão, além de desafios técnicos como segurança, fatores humanos, alocação de tarefas e adaptabilidade. Identifica lacunas de pesquisa, como a falta de implementações completas de HRT e a escassez de datasets para treinar algoritmos de ML em ambientes dinâmicos com humanos. Por fim, sugere direções futuras, incluindo a aplicação de HRT em desmontagem de produtos usados para uma economia mais circular e sustentável.
