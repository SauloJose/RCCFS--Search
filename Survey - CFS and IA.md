---
titulo: Recent Advances in Artificial Intelligence for Wireless Internet of Things and Cyber-Physical Systems- A Comprehensive Survey
autores:
  - Salau BA
  - Rawal A
  - Rawat DB
ano: 2022
tipo: artigo
tema: Survey AI/ML para IoT/CPS sem fio
publicacao: IEEE Access
status: lido
doi: 10.1109/ACCESS.2022.3159573 (exemplo)
citekey: Salau2022
tags:
  - artigo
  - survey
  - IoT
  - CPS
  - redes_sem_fio
  - machine_learning
  - federated_learning
  - transfer_learning
  - revisao_bibliografica
---

> [!NOTE] Ficha Sintética (Visão Rápida)
> 
> - **O que busca resolver:** Mapear como técnicas de IA/ML estão sendo aplicadas para enfrentar os desafios de comunicação, controle e computação (3Cs) em sistemas IoT e CPS que dependem de redes sem fio.
> - **Problema Principal:** A explosão de dispositivos IoT/CPS (~14,7 bi até 2023) gera dados massivos que exigem redes sem fio adaptáveis, de baixa latência, alta vazão e seguras — requisitos que métodos tradicionais de otimização não atendem.
> - **Diferencial:** Diferente de surveys anteriores focados em ML específico (ex: só DL ou só RL), este trabalho inclui paradigmas emergentes cruciais para o cenário descentralizado e com restrições de privacidade: **Aprendizado Federado (FL), Distribuído e por Transferência (TL)**.
> - **Principais áreas de aplicação:** Comunicação (escalonamento, alocação de recursos, conectividade), Controle (tomada de decisão autônoma, roteamento) e Computação (processamento em borda, redução de latência).
> - **Desafios abertos identificados:** Conectividade/escalabilidade, latência imposta pela IA, gerenciamento de energia, segurança contra ataques adversariais e fusão de dados multimodais.
> - **Relevância:** Alta — serve como mapa do estado da arte e base para justificar escolhas de ML (ex: FL para privacidade) e identificar gargalos práticos em projetos de sistemas multiagente.

---

# Recent Advances in Artificial Intelligence for Wireless Internet of Things and Cyber-Physical Systems

---

## 1. Referência Bibliográfica e Arquivo Fonte

- **ABNT:** SALAU, B. A.; RAWAL, A.; RAWAT, D. B. Recent Advances in Artificial Intelligence for Wireless Internet of Things and Cyber-Physical Systems: A Comprehensive Survey. **IEEE Access**, v. 10, p. 12916-12935, 2022. DOI: 10.1109/ACCESS.2022.3159573.
- **Arquivo PDF:** [[Babajide et al. (2022).pdf]]

---

## 2. Contexto, Problema e Escopo

- **O que o artigo busca resolver?** Oferecer uma visão abrangente e atualizada sobre o uso de IA/ML para melhorar redes sem fio em IoT e CPS, com ênfase em paradigmas emergentes (Federated, Distributed, Transfer Learning) que permitem treinamento descentralizado, preservação de privacidade e eficiência.

- **Contexto:** IoT/CPS conectam bilhões de dispositivos (sensores, atuadores, veículos, máquinas) que geram dados massivos e exigem comunicação de baixa latência, alta confiabilidade e segurança. Exemplos: carros autônomos (comunicação V2X), saúde inteligente (monitoramento remoto), Indústria 4.0.

- **Escopo:**
  - Revisão das principais tecnologias de comunicação sem fio para IoT/CPS (curto, médio e longo alcance).
  - Taxonomia e descrição de técnicas de ML (Supervisionado, Não-Supervisionado, Reforço, Deep Learning, Federado, Distribuído, Transferência).
  - Mapeamento de pesquisas atuais que aplicam ML para resolver problemas de comunicação, controle e computação.
  - Identificação de desafios abertos e direções futuras.

---

## 3. Principais Tecnologias de Comunicação para IoT/CPS

O artigo classifica as tecnologias sem fio por alcance:

| Alcance                | Tecnologias                                                        | Características                                                                                                                                           |
| :--------------------- | :----------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Curto** (< 150 m)    | Bluetooth, ZigBee, Z-Wave, WiFi, M-Bus, X-bus                      | WPAN/WLAN; baixo consumo; Bluetooth BLE-backscatter para uplink de sensores sem modificação de hardware [16,17]; WiFi usado para localização indoor [20]. |
| **Médio** (5-10 km)    | Wi-SUN, WM-Bus                                                     | Redes de vizinhança (WNAN); usadas em smart metering e infraestrutura avançada de medição (AMI).                                                          |
| **Longo** (até 100 km) | LPWAN: NB-IoT, LTE-M (licenciados); LoRa, Sigfox (não licenciados) | Baixa potência, longa distância; pesquisas em andamento para desenvolvimento pleno [33-35].                                                               |

---

## 4. Taxonomia das Técnicas de ML e Aplicações em IoT/CPS

### 4.1. Aprendizado Supervisionado
- **Objetivo:** Aprender mapeamento entrada-saída a partir de dados rotulados.
- **Algoritmos:** SVM (Suport Vector Machines), KNN, Random Forest, Redes Neurais.
- **Aplicações citadas:**
	1. **SVM** para prever cobertura WiFi e colher energia de RF (Eid et al. [48]).
	2. **KNN e Random Forest** para classificar tráfego de rede em dispositivos IoT móveis (Acar et al. [42]).
	3. **SVM** para monitoramento e controle de qualidade do ar interno (Meris et al. [52]).
	4. Classificação de ambientes indoor usando assinaturas RF (AlHajri et al. [43]).
	
> [!NOTE] **Observações Pessoais**
> Métodos de Machine Learning para que um modelo aprenda a classificar corretamente dados tendo os resultados previamente rotulados. Inicialmente é realizado o treino com dados rotulados e, após isso, o treino é feito com dados não rotulados e avalia-se o resultado do modelo.
### 4.2. Aprendizado Não-Supervisionado
- **Objetivo:** Encontrar padrões em dados não rotulados.
- **Algoritmos:** K-means, PCA, Redes Neurais (autoencoders).
- **Aplicações citadas:**
	1. **K-means** para escalonamento prioritário em LoRaWAN, minimizando atraso e colisões (Alenezi et al. [67]).
	2. **K-means com SDN** para aumentar conectividade em redes mesh no campo de batalha (Taylor & Sharif [51]).
	3. **K-means** para otimização de implantação de nós atuadores em CPS (Li et al. [68]).
	4. **Recursive PCA** para detecção de outliers e agregação de dados em IoT (Yu et al. [49]).
	5. **Recursive Principal Component Regression** para controle e diagnóstico de falhas em CPS veiculares (Jiang & Yin [50]).

> [!NOTE] **Observações Pessoais**
> O algoritmo analisa dados sem rótulos ou respostas prévias para descobrir padrões, agrupamentos e estruturas ocultas por conta própria, como na segmentação de clientes.
### 4.3. Aprendizado por Reforço (RL) e Deep RL (DRL)
- **Objetivo:** Agente aprende política de ações por tentativa e erro, maximizando recompensa cumulativa.
- **Algoritmos:** Q-Learning, DQN, DDQN
- **Aplicações citadas:**
	1. **RL** para reconfiguração automática de redes em IoT industrial (Xu et al. [37]).
	2. **DRL** para planejamento de rotas evitando interrupções em redes elétricas inteligentes (Jin et al. [38]).
	3. **Deep Q-Network** para alocação de serviços e recursos em CPS industrial sob incerteza (Hao et al. [39]).
	4. **Q-learning** para alocação de largura de banda e redução de congestionamento (Cetin et al. [74]).
	5. **Transfer RL** com Q-learning para transferência de experiência em contextos (Zhang & Zavlanos [71]).

> [!NOTE] **Observações Pessoais**
> O agente aprende por tentativa e erro ao interagir com um ambiente, recebendo recompensas por acertos e penalidades por erros para otimizar suas decisões, muito usado em jogos e robótica.
### 4.4. Deep Learning (DL)
- **Objetivo:** Aprender representações hierárquicas em múltiplas camadas.
- **Arquiteturas:** FNN (Fully connected), RNN (Recurrent), CNN (Convolutional) (supervisionado); DBN, SAE (não-supervisionado).
- **Aplicações citadas:**
  - **DL** para clustering dinâmico de rede IoT com edge computing (Liu et al. [98]).
  - **Semi-supervised DL com autoencoders** para localização indoor via Bluetooth (Mohammadi et al. [27]).
  - **Deep Q-learning semi-supervisionado** para reconhecimento de atividade humana em saúde IoT (Zhou et al. [99]).
  - **DNN e Deep TL** para offloading computacional em MIMO cloud RAN (Pradhan et al. [100]).

> [!NOTE] **Observações Pessoais**
> O Deep Learning (Aprendizado Profundo) é uma subárea da Inteligência Artificial baseada em redes neurais artificiais com múltiplas camadas. Inspirado no funcionamento do cérebro humano, esse método analisa grandes volumes de dados complexos — como imagens, áudio e texto — para identificar padrões automaticamente. Com isso, o sistema consegue aprender tarefas sofisticadas e fazer previsões sem a necessidade de programação explícita para cada regra.
### 4.5. Aprendizado Federado (Federated Learning - FL)

- **Objetivo:** Treinar modelos descentralizadamente, mantendo dados locais nos clientes e compartilhando apenas parâmetros com servidor central, preservando privacidade.
- **Classificação:** Horizontal (mesmas features), Vertical (mesmos IDs), Federated TL (diferentes features e IDs).
- **Aplicações citadas:**
  - Análise de escalabilidade entre blocos de rádio e número de clientes usando transmissão analógica (Guo et al. [45], Yang et al. [46], Amiri & Gündüz [47]).
  - Compressão de gradientes para reduzir sobrecarga de rede (Amiri & Gündüz [87,88], Abdi et al. [86]).
  - **FL com NOMA** para reduzir latência de agregação (Sun et al. [82]).
  - Avaliação de políticas de escalonamento (RS, RR, PF) para convergência do FL (Yang et al. [81]).
  - Alocação de recursos em sistemas FL sem fio (Ren et al. [79]).
  - Framework FL robusto contra dispositivos maliciosos (Wen et al. [80]).

> [!NOTE] **Observações Pessoais**
> FL é que o que é guardado no servidor central é apenas os modelos atualizados e o treinamento é feito localmente. Ou seja, teriamos uma interligação de dispositivos que enviam seu modelo atualizado com dados locais para o servidor central, o qual terá um **Modelo Global**, resultando do agregado dos modelos locais.
> Esse modelo foi apresentado pelo Google em 2016, como uma alternativa para garantir a evolução do modelo de IA e a privacidade dos dados privados dos usuários.
> A ideia é de que enviando apenas os modelos atualizados localmente, eles não enviam os dados sensivos, apenas os insights que foram tirados desses dados.
> Existe **FL verticais, Horizontais** e **Federeted Transfer Learning**

![[Pasted image 20260831220418.png]]

> [!OBS] **Insight** 
> E se eu utilizasse essa ideia de **Federated Learning** para um grupo de robôs aprender a entender os dados e, consequentemente, melhorar o **modelo global.**?
> Isso pode trazer problemas de sobrecarga na rede, talvez utilizar algum método de compressão possa resolver, ou novos métodos de gradiente descendentes.

Link útil: [https://www.youtube.com/watch?v=zqv1eELa7fs](Federated Learning)
### 4.6. Aprendizado Distribuído (Distributed Learning)
- **Objetivo:** Dividir treinamento em múltiplos nós (workers) em paralelo para acelerar processo.
- **Modalidades:** Data Parallelism (dados divididos entre nós) e Model Parallelism (modelo dividido entre nós).
- **Aplicações citadas:**
  - **Feature Distributed ML (FDML)** para convergência assíncrona com SGD (Hu et al. [40]).
  - **SVM distribuído** com algoritmo gossip para redes de sensores (Kim et al. [92,93]).

> [!NOTE] **Observações Pessoais**
> Em resumo, o treinamento é realizado em paralelo com diversos indivíduos, de modo que o treinamento seja, em teoria, mais rápido. Isso é um dos grandes motivos da velocidade dos treinamentos de IA ultimamente, utilizando grandes datacenters.
### 4.7. Aprendizado por Transferência (Transfer Learning - TL)
- **Objetivo:** Reutilizar conhecimento de uma tarefa fonte para melhorar aprendizado em tarefa alvo com poucos dados.
- **Aplicações citadas:**
  1. **Deep TL** para reconhecimento de atividade humana via WiFi CSI (Yang et al. [107], Arshad et al. [108]).
  2. **TL com ensembles de random trees** entre nós de redes de sensores (Casale et al. [109]).
  3. **Deep TL** para detecção de sinal em backscatter communications (Liu et al. [110]).
  4. **Deep TL** para segurança de camada física em ambientes contestados (Rawat [103]).

> [!NOTE] **Observações Pessoais**
> É uma técnica em que um modelo previamente treinado para uma determinada tarefa é reaproveitado como ponto de partida para resolver um problema novo e correlato. Em vez de ensinar o sistema do zero, aproveita-se o conhecimento já adquirido, reduzindo drasticamente o tempo de treino, os custos computacionais e a quantidade de dados necessária.

---

## 5. Resumo das Pesquisas em Andamento (Tabela IV do Artigo)

| Abordagem | Objetivo | Mérito (+) | Limitação (-) |
| :--- | :--- | :--- | :--- |
| **K-means** [67] | Minimizar colisões/atraso em LoRaWAN | + Escalável, reduz interferência | - Resultado depende do nº de nós |
| **PCA Recursivo** [49] | Detecção de outliers e agregação | + Reduz carga computacional | - Modelo centralizado (ponto falha) |
| **Recursive PCR** [50] | Controle/diagnóstico em CPS veicular | + Minimiza memória, monitora lotes | - KPI limitado |
| **DRL** [38] | Evitar interrupções em smart grid | + Baixo risco | - Alta complexidade |
| **Q-learning** [74] | Alocar largura de banda | + Aplicável a sistemas não-lineares | - Complexidade computacional |
| **FL** [81] | Analisar escalonamento em redes sem fio | + Elimina ponto falha, privacidade | - Custo computacional nos UEs |
| **FL** [79] | Alocação de recursos descentralizada | + Privacidade, baixa complexidade | - Carga nos UEs |
| **Deep Q-learning** [99] | Rotulagem automática para atividade humana | + Lida com dados fracamente rotulados | - |
| **TL** [107,108] | Reconhecimento de atividade via WiFi | + Usa poucos dados, reduz complexidade | - Requer função genérica |
| **DNN + Deep TL** [100] | Offloading em MIMO cloud | + Baixa complexidade, rápido | - |
| **Deep TL** [110] | Detecção de sinal em backscatter | + Poucos dados | - |

---

## 6. Desafios Abertos Identificados

### 6.1. Conectividade
- **Escalonamento:** Ordem de execução de tarefas afeta vazão; modelos de ML podem ser grandes e consumir banda.
- **Gerenciamento de Energia:** Dispositivos em áreas remotas dependem de bateria; ML consome muita energia.
- **Escalabilidade:** Adição de novos dispositivos exige reconfiguração; TL pode reutilizar conhecimento de arquiteturas anteriores.

### 6.2. Latência
- ML na nuvem (GPUs) introduz latência; edge computing e FL são soluções para processar localmente.
- Requisitos 3GPP: 20 bytes em ≤10s para aplicações críticas [113].
- **Pesquisas citadas:** FL descentralizado para minimizar latência em MEC (Chen et al. [114]); multi-state learning para alocação de recursos em IoT massivo (Park & Saad [115]); GAN para escalonamento downlink em IoT industrial (Liu & Bennis [116]).

### 6.3. Distribuição e Computação
- Dados em IoT/CPS são naturalmente distribuídos (sensores/atuadores na borda).
- FL e Distributed Learning são paradigmas promissores para treinar modelos localmente.
- Desafio: dados podem ser não identicamente distribuídos (non-IID); energia e banda são limitadas.

### 6.4. Segurança e Privacidade
- Ataques adversários a modelos de ML (ex: envenenamento, evasão).
- IoT/CPS têm grande superfície de ataque; sistemas devem ser proativos e reativos.
- FL oferece privacidade, mas ainda vulnerável a ataques.
- Referências para segurança: Uprety & Rawat [70], Rawal et al. [123], Olowononi et al. [124], Rawat [125].

### 6.5. Fusão de Dados
- Desafios: multimodalidade (dados de diferentes sensores), registro/calibração, trivialidade dos dados, timing operacional (sensores com frequências diferentes).
- Soluções: extração de features antes da fusão; incorporação de diferentes escalas temporais [120,121].

---

## 7. Conclusões e Direções Futuras

- IA/ML são fundamentais para realizar o potencial de IoT/CPS, especialmente para os 3Cs (Comunicação, Controle, Computação).
- Paradigmas emergentes (FL, Distributed Learning, TL) são chave para lidar com privacidade, descentralização e eficiência.
- Desafios práticos (latência, energia, segurança, fusão de dados) ainda precisam de soluções robustas.
- Futuro: sistemas de IA distribuídos, leves e seguros, integrados a tecnologias como blockchain e edge computing.

---

## 8. Anotações Pessoais

> [!NOTE] Insights para o projeto
> 1. **FL é a tendência mais relevante** para cenários com múltiplos agentes móveis que precisam preservar privacidade dos dados (ex: sensoriamento colaborativo sem compartilhar dados brutos).
> 2. **Latência é o maior gargalo prático** — modelos precisam ser leves (TinyML) ou executados em edge, com inferência rápida.
> 3. **Segurança é crítica** — ataques adversariais a modelos de ML são uma ameaça real; pesquisar robustez é uma oportunidade.
> 4. **TL pode reduzir necessidade de dados rotulados** — útil para adaptar modelos a novos ambientes sem retreinamento completo.
> 5. **O survey é um mapa, não um manual** — serve para orientar a escolha de técnicas e justificar decisões de projeto, mas não fornece implementação pronta.