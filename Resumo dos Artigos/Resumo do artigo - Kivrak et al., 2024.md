[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **Computer Communications** (Elsevier), que propõe uma arquitetura de sistema ciber-físico (CPS) para governar um ecossistema autônomo de múltiplos robôs heterogêneos em missões de inspeção remota de ativos industriais, com Digital Twin e gestão dinâmica de largura de banda, validado por simulação em ambiente representativo.

---

### 📌 Metadados do Artigo
*   **Título:** Cyber-physical system architecture of autonomous robot ecosystem for industrial asset monitoring
*   **DOI:** 10.1016/j.comcom.2024.02.013
*   **Publicação (Veículo/Evento):** Computer Communications (Elsevier), Vol. 218, pp. 72–84
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (ambiente representativo com frota de robôs mapeando um edifício desconhecido)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Frota heterogênea composta por robôs com diferentes capacidades de locomoção — robôs com rodas (*wheeled*), robôs com pernas (*legged*) e robôs aéreos (*aerial*) — equipados com sensores complementares como LiDAR 3D, câmeras de profundidade, encoders de roda e IMUs. Os robôs cooperam para mapear e caracterizar ambientes remotos e desafiadores.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Centralized (mapeamento centralizado no Digital Twin; robôs com autonomia local) |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics; Optimization |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | WLAN; Cellular (4G/5G) |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS (ROS 1 e ROS 2 / DDS) |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** A arquitetura CPS proposta é composta por três camadas: **Physical Twin**, **Digital Tissue** e **Digital Twin**. O *Physical Twin* contém a frota heterogênea de robôs (rodas, pernas e aéreos) e o ambiente físico, com sensores como LiDAR 3D, câmeras de profundidade, encoders e IMUs. O *Digital Tissue* é a infraestrutura de comunicação (rede sem fio, 4G/5G, nuvem) que interliga os mundos físico e digital; inclui downsampling (filtro voxel), compressão (Graco/KD-Tree) e um **Bandwidth Manager** que controla dinamicamente a frequência de transmissão dos dados comprimidos para reduzir largura de banda e latência. O *Digital Twin* mantém um mapa 3D probabilístico por voxel-grid (Octomap) construído a partir da fusão sequencial das nuvens de pontos de todos os robôs, além de uma interface gráfica (Rqt/Rviz) para teleoperação, visualização de streams de vídeo, monitoramento de status e controle da frota. O fluxo de dados é bidirecional: dados de pose e sensores dos robôs são enviados ao Digital Twin, e comandos do operador são enviados de volta aos robôs. O sistema usa ROS como middleware, com publicação-assinatura via TCP/IP, e adota uma abordagem centralizada para o mapeamento multi-robô, mantendo autonomia local nos robôs.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de inspeção remota de ativos industriais em ambientes perigosos e desafiadores, nos quais frotas heterogêneas de robôs precisam ser coordenadas e monitoradas em tempo quase real por meio de gêmeos digitais. Propõe uma arquitetura CPS generalizada para governar um ecossistema autônomo multi-robô via rede de comunicação escalável, integrando técnicas de downsampling, compressão e gerenciamento dinâmico de largura de banda para permitir troca bidirecional eficiente de dados entre os gêmeos físico e digital. A arquitetura é composta por Physical Twin (frota heterogênea com sensores complementares), Digital Tissue (infraestrutura de comunicação com gestão de banda) e Digital Twin (mapa 3D Octomap, interface gráfica para teleoperação e monitoramento). A viabilidade é demonstrada por simulações em ambiente representativo, nas quais uma frota de robôs mapeia um edifício desconhecido e gera um mapa 3D probabilístico comum, avaliando e gerenciando os requisitos de largura de banda. O trabalho contribui para a implementação prática de inspeção remota contínua com sistemas multi-robô por meio de infraestrutura ciber-física, com melhorias em escalabilidade, interoperabilidade e desempenho para monitoramento de ativos industriais.