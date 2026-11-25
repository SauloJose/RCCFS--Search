Aqui está o material completo em formato Markdown (`.md`). Ele está dividido em duas partes: o **Prompt de Instrução** (que você usará para configurar a IA) e o **Template de Extração** (o formato exato em que a IA deverá devolver as informações). 

Este material foi desenhado para ser rigoroso e alinhado com a taxonomia **RC-SCF** apresentada no seu PDF.

---

# 📄 Prompt para Extração de Dados (Copie e cole no seu LLM)

**Contexto:** Você é um pesquisador especialista em Sistemas Multi-Robôs (MRS) e no Contínuo Ciber-Físico. Sua tarefa é ler o texto de um artigo científico fornecido e extrair informações estruturadas de acordo com a taxonomia **RC-SCF** (Robot, Communication, Scope, Decision, Cyber-Physical Continuum).

**Instruções de Execução:**
1. Leia atentamente o artigo fornecido.
2. Preencha o template abaixo de forma estritamente técnica.
3. Se uma informação não estiver explícita no texto, escreva **"Não especificado"**.
4. Baseie suas respostas exclusivamente nas categorias fornecidas na taxonomia. Não invente categorias, a menos que o artigo traga algo completamente fora do escopo (nesse caso, use "Outro").
5. Retorne o resultado apenas em formato Markdown, seguindo a estrutura do template.

**Definições da Taxonomia para Classificação:**
*   **Escopo:** *Task* (alocação/divisão de tarefas), *Motion* (movimentação/navegação/controle de frota), *Resource* (gerenciamento de recursos compartilhados).
*   **Estrutura de Decisão:** *Centralized* (um nó mestre decide), *Decentralized* (agentes decidem autonomamente/consenso), *Hierarchical* (múltiplos níveis de comando).
*   **Método de Decisão:** *Optimization* (matemática/otimização), *Rules & Heuristics* (regras fixas), *Learning* (RL, DRL, ML), *Negotiation* (contratos, leilões).
*   **Processamento:** *Robot* (onboard), *Edge/Fog* (servidores locais), *Cloud* (nuvem), *Hybrid* (combinação).
*   **Integração Digital:** *Digital Model* (manual, sem sincronização automática), *Digital Shadow* (fluxo físico -> digital automático), *Digital Twin* (fluxo bidirecional automático), *None*.
*   **Regime Temporal:** *Online* (tempo real/sincronizado), *Offline* (processamento posterior).
*   **Comunicação (Tipo):** *Explicit* (troca de mensagens direta), *Implicit* (via ambiente/stigmergia).
*   **Topologia:** *Infrastructure* (depende de infraestrutura fixa), *Ad-Hoc* (MANET/FANET), *Opportunistic* (contato intermitente).
*   **Tecnologia:** *WLAN* (Wi-Fi), *Cellular* (5G/6G/4G), *Long-range* (LoRa, Satélite), *Short-range* (Bluetooth, UWB), *Other*.

---

# 📝 Template de Saída (Preenchimento da IA)

### 📌 Metadados do Artigo
*   **Título:** [Inserir título exato]
*   **DOI:** [Inserir DOI]
*   **Publicação (Veículo/Evento):** [Inserir nome do Journal ou Conferência]
*   **Ano:** [Inserir ano]

### 🎯 Classificação do Artigo
*   **Tipo de Artigo:** [Survey | Solution | Benchmark | Other]
*   **Tipo de Validação:** [Simulação | Testbed/Real-world | Hardware-in-the-Loop (HIL) | Co-simulation | Analítico | Não especificado]

### 🤖 Composição e Descrição da Frota
*   **Composição:** [Homogênea | Heterogênea]
*   **Descrição da Frota:** [Ex: 3 UAVs e 2 UGVs; ou 10 robôs terrestres; ou Frota heterogênea de drones aéreos e aquáticos]

### 🧩 Dimensões da Taxonomia (RC-SCF)

| Dimensão | Categoria / Sub-ramo | Classificação no Artigo |
| :--- | :--- | :--- |
| **Scope (Escopo)** | Tasks / Motion / Resources | [Selecione uma ou mais] |
| **Decision (Estrutura)** | Centralized / Decentralized / Hierarchical | [Selecione uma] |
| **Decision (Método)** | Optimization / Rules & Heuristics / Learning / Negotiation | [Selecione uma ou mais] |
| **Processing (Local)** | Robot / Edge-Fog / Cloud / Hybrid | [Selecione uma] |
| **Model (Integração Digital)**| Digital Model / Digital Shadow / Digital Twin / None | [Selecione uma] |
| **Model (Regime Temporal)** | Online / Offline | [Selecione uma] |
| **Communication (Tipo)** | Explicit / Implicit | [Selecione uma] |
| **Communication (Topologia)**| Infrastructure / Ad-Hoc / Opportunistic | [Selecione uma] |
| **Communication (Tecnologia)**| WLAN / Cellular / Long-range / Short-range / Other | [Selecione uma ou mais] |
| **Middleware** | ROS 2, DDS, Zenoh, Outro, Nenhum | [Inserir qual] |

### 🏗️ Arquitetura Utilizada
*   **Descrição da Arquitetura:** [Descreva em 3 a 5 linhas como se dá a comunicação e a distribuição de processamento. Ex: "Os robôs se comunicam via rede Ad-Hoc usando ROS 2, processam tarefas de navegação localmente (Edge), mas enviam dados de percepção para um servidor Cloud para treinamento de modelos de aprendizado. A tomada de decisão é descentralizada via negociação (leilões)."]

### 📖 Resumo do Artigo
*   **O que o artigo faz:** [Resumo conciso de 4 a 6 linhas explicando o problema abordado, a solução proposta e os principais resultados obtidos.]

