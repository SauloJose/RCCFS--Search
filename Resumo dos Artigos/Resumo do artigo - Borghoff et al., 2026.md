[[Atv1 - Parte 4 - Entrega Final]]

**O que é:** Artigo científico do tipo **Solution**, publicado na **Future Internet** (MDPI), que propõe o framework **Guarded Swarms**, uma arquitetura híbrida digital-analógica para enxames de UAVs/UGVs que combina coordenação multiagente baseada em Petri nets (TB-CSPN) com camadas de segurança analógica independentes no nível de atuação, visando autonomia confiável sob condições adversariais e de negação de comunicação, validado por estudo de caso conceitual com plataformas UAV e UGV.

---

### 📌 Metadados do Artigo
*   **Título:** Guarded Swarms: Building Trusted Autonomy Through Digital Intelligence and Physical Safeguards
*   **DOI:** 10.3390/fi18010064
*   **Publicação (Veículo/Evento):** Future Internet (MDPI), Vol. 18, Article 64
*   **Ano:** 2026

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** Solution
*   **Tipo de Validação:** Simulação / Estudo de caso conceitual (a arquitetura é um blueprint; o caso demonstra os conceitos de arbitragem digital e veto analógico)

### 🤖 Composição e Descrição da Frota
*   **Composição:** Heterogênea
*   **Descrição da Frota:** Enxame composto por UAVs e UGVs (e potencialmente outros agentes robóticos), organizados em uma hierarquia de papéis: supervisores humanos, agentes de IA (consultores/planejadores autônomos) e trabalhadores robóticos (workers). Cada unidade física é encapsulada em um envelope de segurança analógico independente.

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | Tasks; Motion; Resources (coordenação, segurança, alocação) |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | Hierarchical |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | Rules & Heuristics (Petri nets, threshold consensus); Learning (inferência ML para classificação de ameaças) |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | Hybrid (digital + analógico) |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | None (foco em coordenação digital e segurança analógica, sem DT explícito) |
| **Model (Regime Temporal)** | Online / Offline | Online |
| **Communication (Tipo)** | Explicit / Implicit | Explicit |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | Ad-Hoc (enxame) |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | Não especificado |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | ROS 2 / DDS (mencionado como middleware típico); Outro (TB-CSPN) |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** O Guarded Swarms propõe uma arquitetura em camadas que separa explicitamente a **coordenação digital** da **execução física segura**. Na camada digital, **agentes semânticos** (humanos, LLMs, planejadores clássicos ou módulos de IA específicos de domínio) analisam o contexto e propõem diretivas táticas e decisões negociadas. Essas diretivas são coordenadas pelo **TB-CSPN** (Timed Block Colored Petri Nets), que fornece um substrato de coordenação com sincronização, temporização e validação explícitas, usando tokens que representam condições de controle validadas e com limite de tempo. Na camada física, cada trabalhador robótico (UAV ou UGV) recebe comandos do seu controlador de bordo, que traduz diretivas de alto nível em sinais PWM para atuadores. Crucialmente, cada trabalhador é encapsulado em um **envelope de segurança analógico** — uma camada de hardware independente que valida continuamente os comandos de atuação contra restrições físicas predefinidas (limites de empuxo, atitude, proximidade, corrente, temperatura). Comandos que satisfazem todos os predicados de segurança passam inalterados; comandos que violam qualquer restrição são limitados ou vetados no nível de hardware antes de chegar aos atuadores. A arbitragem entre múltiplas propostas digitais é feita por votação leve baseada em tokens e janelas de decisão com limite de tempo, permitindo autonomia local e degradação graciosa sob estresse de rede. O resultado é uma arquitetura que mantém coesão de missão enquanto permite que os nós continuem operando com segurança mesmo quando o controle de alto nível se torna intermitente. O framework define separação explícita de papéis, semântica de arbitragem e contratos de temporização que ligam raciocínio semântico, lógica de coordenação e vetos de atuação.

### 📖 Resumo do Artigo
*   **O que o artigo faz:** O artigo aborda o problema de confiabilidade e segurança em enxames autônomos de UAVs/UGVs, nos quais arquiteturas puramente digitais são vulneráveis a falhas de temporização, ataques cibernéticos e negação de serviço, podendo levar a falhas em cascata. Propõe o Guarded Swarms, um framework arquitetural que formaliza a fronteira de integração entre coordenação digital multiagente e aplicação de segurança analógica no nível de hardware. A arquitetura combina (i) coordenação semântica baseada em Petri nets (TB-CSPN), (ii) vetos de atuação em hardware não programável (envelopes de segurança analógicos) e (iii) contratos de temporização explícitos que abrangem desde o raciocínio semântico até a execução física. O artigo argumenta que essa separação permite que a camada digital mantenha autoridade sobre a coordenação de missão, enquanto a camada analógica garante que nenhum comando — legítimo ou comprometido — possa ultrapassar os limites operacionais seguros. Um estudo de caso com plataformas cooperativas de UAV e UGV ilustra a arbitragem digital concorrente e o comportamento de veto analógico. O framework é apresentado como um blueprint arquitetural reutilizável para implementações de enxames confiáveis em ambientes adversariais e de comunicação negada.

