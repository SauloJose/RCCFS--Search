[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **Robotics and Computer-Integrated Manufacturing** (Elsevier), que propõe um framework de **Hybrid Cognitive Digital Twin (HCDT)** integrando LLMs e Graph Neural Networks (GNNs) para adaptação generativa de tarefas em sistemas de colaboração multi-humano multi-robô (MHMRC), validado em aplicação de desmontagem de baterias de íons de lítio.

---

### 📌 Metadados do Artigo
*   **Título:** GNN-LLM hybrid cognitive architectures for generative task adaptation in multi-human multi-robot collaborative disassembly
*   **DOI:** Não especificado no texto
*   **Publicação (Veículo/Evento):** Robotics and Computer-Integrated Manufacturing (Elsevier)
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Testbed/Real-world (aplicação de desmontagem de baterias de íons de lítio com resultados experimentais)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Equipe de colaboração multi-humano multi-robô (MHMRC) composta por operadores humanos e robôs com papéis diferenciados, atuando em estações de desmontagem de baterias de íons de lítio. O número exato de agentes não é fixado no texto; a heterogeneidade está na combinação de humanos e robôs com capacidades e funções distintas.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Learning; Rules & Heuristics |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | Digital Twin (Hybrid Cognitive Digital Twin) |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Infrastructure |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | Não especificado |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O framework HCDT é estruturado em três entidades: **Physical Entity (E)**, que coleta dados de sensores (velocidade, tato, visão, força, proximidade, áudio) do ambiente real MHMRC; **Virtual Entity (D)**, que mantém um gêmeo digital sincronizado com reconhecimento de cena, visualização e protocolos de comunicação; e **Cognitive Entity (I)**, que opera em quatro fases (percepção, raciocínio, planejamento e ação) e é responsável pela tomada de decisão autônoma. A entidade cognitiva integra dois módulos principais: (i) **Affordances Learning Module**, com GNN auto-supervisionada (GCN + Graph Self-Attention) para extrair representações de capacidades funcionais e potenciais de interação; e (ii) **Flexible Enhancement Module**, onde um LLM atua em papéis duplos de Retriever e Critic sobre grafos textuais, com um módulo de alinhamento cross-modal que funde representações baseadas em regras (grafo) e semânticas (LLM) para gerar uma representação aprimorada sensível ao contexto. As decisões de alocação de tarefas, sequenciamento de execução e estratégias de colaboração são geradas a partir dessa representação. O sistema lida autonomamente com variações operacionais não planejadas e distúrbios dinâmicos, mantendo a segurança por meio de simulação no gêmeo digital. O processamento é híbrido (entidades física, virtual e cognitiva) e a comunicação é explícita.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de colaboração multi-humano multi-robô (MHMRC) em cenários industriais complexos com multitarefa concorrente, distúrbios dinâmicos e coordenação de papéis heterogêneos, nos quais abordagens tradicionais baseadas em instruções pré-programadas e grafos estáticos falham em se adaptar a tarefas não planejadas. Propõe um framework de Hybrid Cognitive Digital Twin (HCDT) que integra LLMs e GNNs para dotar o sistema de capacidades de compreensão, raciocínio e adaptação generativa. A entidade cognitiva usa GNN auto-supervisionada para aprender affordances e um LLM com papéis de Retriever e Critic para enriquecer semanticamente as representações, com alinhamento cross-modal entre as duas fontes. O sistema é validado em uma aplicação de desmontagem de baterias de íons de lítio automotivas, demonstrando adaptabilidade a tarefas colaborativas dinâmicas e generalização para gerar estratégias em variações operacionais não planejadas, superando abordagens com estratégias pré-codificadas por engenheiros humanos.