[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na revista **Applied Sciences** (MDPI), que propõe um framework de geração de código de controle adaptativo baseado em LLM com verificação integrada por **Digital Twin** para sistemas robóticos heterogêneos, visando mitigar "alucinação física" e garantir viabilidade dinâmica antes da execução, validado por simulação em PyBullet e verificação analítica via RNEA.

---

### 📌 Metadados do Artigo
*   **Título:** LLM-Based Adaptive Control Code Generation Framework with Digital Twin-Integrated Verification for Heterogeneous Robot Systems
*   **DOI:** 10.3390/app16083883
*   **Publicação (Veículo/Evento):** Applied Sciences (MDPI)
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação (PyBullet); Analítico (RNEA para UR5e e Franka Panda)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Pool de seis manipuladores industriais com capacidades de carga útil entre 3 kg e 25 kg: Franka Panda (3 kg, 7 DoF), UR5e (5 kg, 6 DoF), Doosan M0609 (6 kg, 6 DoF), Doosan M1013 (10 kg, 6 DoF), KUKA iiwa14 (14 kg, 7 DoF) e Doosan H2515 (25 kg, 6 DoF). A heterogeneidade abrange robôs colaborativos leves, manipuladores de carga média e um robô industrial pesado, refletindo a diversidade de HMLV.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning (LLM); Rules & Heuristics (módulos determinísticos) |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O framework é um pipeline de cinco estágios que integra tradução por LLM e verificação determinística. Primeiro, uma instrução em linguagem natural é transformada por um LLM (Gemini 2.5 Pro com prompting aumentado por recuperação) em uma **representação intermediária estruturada** (TDL), independente de fornecedor. Segundo, referências espaciais simbólicas são **grounded** usando informações de runtime do **Digital Twin**, convertendo-as em parâmetros executáveis conforme o estado atual do ambiente. Terceiro, um módulo de **seleção de robô ciente de factibilidade** avalia o pool heterogêneo com hard constraints (payload, alcance, DoF) e uma função de fitness ponderada com score de payload tri-modal (Gaussiana em torno de R=1,2, penalidade logarítmica para R>3). Quarto, a trajetória grounded é validada dinamicamente por **RNEA** (Recursive Newton-Euler Algorithm), verificando se os torques articulares excedem os limites do robô selecionado. Quinto, se infeasible, um **fator de escala global** é aplicado para reduzir velocidade e aceleração preservando a forma da trajetória; só então o LLM gera o **código específico do fornecedor** (RAPID, KRL, DRS, URScript). O LLM atua apenas como motor de tradução; todas as decisões de segurança são tomadas por módulos determinísticos. O processamento é híbrido (LLM, Digital Twin e robô físico) e a verificação é online, antes da execução.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de geração automática de código de controle para frotas heterogêneas de robôs em manufatura HMLV, no qual abordagens baseadas em LLM sofrem de "alucinação física" — comandos espacialmente inconsistentes ou dinamicamente inviáveis. Propõe um framework de verificação integrado a Digital Twin que transforma linguagem natural em uma representação intermediária estruturada, faz grounding espacial com informações de runtime do DT, seleciona o robô mais adequado por factibilidade física, valida a dinâmica da trajetória via RNEA e aplica escala adaptativa de movimento quando os torques excedem os limites, antes de gerar código específico do fornecedor. A avaliação com 170 cenários de descrição de tarefas e oito tarefas de seleção de robôs mostrou melhor discriminabilidade em casos de carga leve e cobertura total de factibilidade com escala adaptativa (vs. 50% sem escala), indicando que a verificação baseada em Digital Twin pode melhorar a confiabilidade da programação multi-fornecedor baseada em LLM.