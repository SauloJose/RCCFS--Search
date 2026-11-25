[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na revista **Sensors** (MDPI), que propõe um framework genérico para planejamento e execução de missões com sistemas multi-robôs heterogêneos (UGVs e UAVs), incluindo alocação de tarefas, controle descentralizado de formação 2D/3D e comunicação via ROS 2, validado por estudo de caso simulado.

---

### 📌 Metadados do Artigo
*   **Título:** Toward a Generic Framework for Mission Planning and Execution with a Heterogeneous Multi-Robot System
*   **DOI:** 10.3390/s24216881
*   **Publicação (Veículo/Evento):** Sensors (MDPI)
*   **Ano:** 2024

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Frota composta por UGVs e UAVs com capacidades complementares (sensores, carga útil, comunicação etc.), sem número fixo especificado. O estudo de caso simulado envolve exploração coordenada e coleta de dados com robôs terrestres e aéreos.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Não especificado |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS 2 |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O framework é dividido em **Mission Planning** e **Mission Handling**. O planejador de missão avalia requisitos, verifica factibilidade com base nas capacidades dos robôs disponíveis e aloca tarefas/subtarefas aos robôs mais adequados. A execução usa uma estratégia de controle descentralizada, na qual cada robô possui driver, worker e controller; um componente Oracle combina estados e percepções individuais em conhecimento global, e cada controller decide localmente os comandos. A comunicação entre os módulos e robôs é feita via ROS 2, com acoplamento fraco entre componentes para escalabilidade e manutenção.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de planejamento e execução de missões com frotas heterogêneas de UGVs e UAVs em ambientes dinâmicos e não estruturados, incluindo controle de formação 2D/3D e alocação de tarefas conforme capacidades. Propõe um framework genérico com dois componentes principais: um planejador de missão, que interpreta descrições de missão e de robôs, verifica factibilidade e gera um plano alocando tarefas; e um manipulador de missão, que orquestra a execução com controladores descentralizados e conhecimento global obtido por oráculos. O framework usa ROS 2 para comunicação confiável e é demonstrado por meio de um estudo de caso simulado de exploração coordenada e coleta de dados, mostrando a integração dos blocos de construção e a capacidade de coordenar robôs heterogêneos.