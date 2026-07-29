# Caderno Temático: Regulação do Setor Elétrico — REN 1000/2021 ANEEL, MMGD e Mercado Livre

Este repositório documenta a construção de um **Caderno Temático inteligente no NotebookLM**, projetado para atuar como um assistente de consulta rápida regulatória na prática da Engenharia Elétrica, gestão de clientes, consultoria autônoma e defesa contra abusos de distribuidoras de energia elétrica.

---

## 📌 Contexto e Objetivos

### 🎯 Contexto
Na atuação técnica e comercial com o **Mercado Livre de Energia (ACL)** e a **Micro e Minigeração Distribuída (MMGD)**, enfrentar gargalos operacionais no relacionamento com as distribuidoras de energia é uma rotina. Entre os desafios mais recorrentes na gestão e consultoria estão:

* **Erros de Faturamento e Medição:** Cobranças indevidas, estimativas incorretas de consumo, divergências na aplicação tarifária e falhas no faturamento bidirecional;
* **Descumprimento de Prazos:** Atrasos na emissão de Pareceres de Acesso/Orçamentos de Conexão, vistorias, trocas de titularidade e adequações de medição para migração ao Mercado Livre;
* **Negativas Unilaterais e Exigências Indevidas:** Barreiras burocráticas e indeferimentos de solicitações sem o devido embasamento regulatório por parte dos canais de atendimento das concessionárias.

A **Resolução Normativa ANEEL nº 1.000/2021 (REN 1000)** é a principal norma consolidadora dos direitos e deveres dos consumidores e das obrigações das distribuidoras no Brasil. No entanto, por ser um texto extenso e denso, a localização rápida de respaldos regulatórios para a defesa técnica de clientes costuma ser um processo moroso.

### 🚀 Objetivos do Caderno Temático
1. **Centralizar o Respaldo Regulatório:** Mapear de forma precisa artigos, parágrafos e prazos da REN 1000/2021 e da Lei 14.300/2022.
2. **Agilizar a Solução de Divergências:** Criar um fluxo de consulta capaz de fundamentar minutas de contestação e defesas técnicas contra erros e atrasos das distribuidoras.
3. **Reduzir o Tempo de Resposta:** Automatizar a localização de regras de compensação financeira por descumprimento de prazos ou violação de indicadores (DIC/FIC).
4. **Construir um Repositório Reutilizável:** Disponibilizar para a comunidade técnica um acervo de prompts otimizados e um miniguia prático de consulta.

---

## 📚 Curadoria de Fontes

Para garantir rigor técnico e aplicabilidade prática no dia a dia da engenharia, foram selecionadas fontes oficiais (para leitura direta do NotebookLM) e análises de mercado em vídeo:

### 📄 Fontes Primárias e Regulatórias (Documentos e Leis)
1. **[Resolução Normativa ANEEL nº 1.000/2021 (Texto Consolidado)](https://www2.aneel.gov.br/cedoc/ren20211000.pdf):** Norma central sobre as regras de prestação do serviço público de distribuição de energia elétrica, direitos, deveres e prazos operacionais.
2. **[Lei nº 14.300/2022 — Marco Legal da MMGD](https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2022/lei/l14300.htm):** Base legal do Sistema de Compensação de Energia Elétrica (SCEE), transição do Fio B e garantias de fiel cumprimento.
3. **[Módulo 3 do PRODIST / ANEEL — Acesso ao Sistema de Distribuição](https://www.gov.br/aneel/pt-br/assuntos/prodist):** Regula as condições operacionais, prazos e exigências técnicas para conexão de acessantes ao sistema.

### 🎥 Fontes Complementares e Aplicadas (Análises em Vídeo)
4. **[REN 1000, PRODIST e Lei 14.300 | Oficina do Conhecimento](https://www.youtube.com/watch?v=NCzoGhDt-tw):** Análise das interseções operacionais entre a norma, as diretrizes de distribuição e os impactos práticos na GD.
5. **[Entendendo a REN 1000 da ANEEL | Boteco da Engenharia Podcast](https://www.youtube.com/watch?v=oLGw0QNwCxU):** Discussão prática sobre as mudanças da REN 1000, prazos de ressarcimento por danos elétricos e direitos do consumidor.
6. **[Resolução 1000: Religação de Energia Elétrica | Canal ANEEL](https://www.youtube.com/watch?v=3zdlPpFmM8g):** Detalhamento sobre prazos de religação e direito a compensações financeiras automáticas por descumprimento de prazos.

---

## 🛠️ Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Abaixo documentamos a evolução dos testes iterativos com IAs/NotebookLM, evidenciando as falhas observadas em prompts genéricos e o refino necessário para extrair respostas regulatórias precisas:

### 🧪 Caso de Teste 1: Prazos e Penalidades de MMGD (Parecer de Acesso)
* **Prompt Genérico:** *"Qual é o prazo da concessionária para dar o parecer de acesso de geração distribuída?"*
* **Resultado:** Resposta rasa (30 dias), sem diferenciar faixas de potência e omitindo sanções por descumprimento.
* **A "Cicatriz":** Prompts abertos fazem a IA ignorar o enquadramento entre a REN 1000/2021 e a Lei 14.300/2022.
* **Prompt Estratégico:**
  > *"Atue como engenheiro especialista em regulação. Com base na REN 1000/2021 da ANEEL, quais são os prazos exatos para a distribuidora emitir o Orçamento de Conexão/Parecer de Acesso para MMGD (diferenciando por potência/obras)? O que acontece se o prazo for descumprido? Cite os artigos exatos."*
* **Resultado Otimizado:** Mapeamento correto dos prazos (15 dias sem obras, 30 dias com obras para microgeração e 45 dias para minigeração com obras na transmissão), citando os Art. 82 e Art. 158 e as devidas compensações.

### 🧪 Caso de Teste 2: Cobrança Indevida e Erros de Faturamento
* **Prompt Genérico:** *"A distribuidora cobrou a mais do meu cliente de energia, o que fazer?"*
* **Resultado:** Sugestões informais sem respaldo técnico (ex: "ir ao Procon").
* **A "Cicatriz":** A IA não aplicou a regra regulatória de devolução em dobro nem os prazos retroativos.
* **Prompt Estratégico:**
  > *"Com base no Capítulo X da REN 1000/2021 da ANEEL (Faturamento e Devolução de Valores), elabore uma minuta de contestação técnica por faturamento incorreto pela distribuidora. Exija a devolução do valor pago a mais em dobro conforme os critérios da norma e cite os artigos pertinentes."*
* **Resultado Otimizado:** Geração de minuta fundamentada no Art. 323 (Devolução em dobro) e no Art. 321, especificando atualização pelo IPCA.

### 🧪 Caso de Teste 3: Adequação para Mercado Livre (Grupo A) e Prazos
* **Prompt Genérico:** *"Quanto tempo a distribuidora tem para adequar a medição para o mercado livre?"*
* **Resultado:** Confusão entre adequação de medição no Grupo A e ligação nova no Grupo B.
* **A "Cicatriz":** Foi necessário restringir o escopo ao segmento do Grupo A e ao Sistema de Medição para Faturamento (SMF) no Ambiente de Contratação Livre (ACL).
* **Prompt Estratégico:**
  > *"Consulte os artigos da REN 1000/2021 relativos à adequação do Sistema de Medição para Faturamento (SMF) em Unidades Consumidoras do Grupo A que vão migrar para o Ambiente de Contratação Livre (ACL). Quais são os prazos máximos para a distribuidora realizar a adequação e vistoria?"*
* **Resultado Otimizado:** Respaldo exato dos artigos referentes às adequações de SMF e direitos do consumidor caso a concessionária descumpra o cronograma.

---

## 📘 Miniguia de Estudo (Entrega Final)

Consolidação regulatória pronta para consulta rápida na rotina da engenharia.

### 1. 📝 Resumos Estruturados do Assunto

#### 🅰️ Faturamento, Erros e Devolução de Valores
* **Inconsistências e Devolução (Art. 323):** Cobranças a maior por erro de medição ou faturamento exigem devolução em **dobro** sobre o valor pago em excesso, acrescido de atualização monetária (IPCA) e juros, salvo engano justificável.
* **Faturamento por Estimativa (Art. 255):** Permitido apenas por motivo de força maior ou impedimento de acesso. Se persistir por mais de 3 ciclos consecutivos, a distribuidora deve resolver o acesso ou aceitar a autoleitura.
* **Revisão Retroativa:** Cobranças a menor por falha da distribuidora limitam-se a no máximo **3 ciclos**, enquanto o consumidor tem até **10 anos** para reaver cobranças indevidas.

#### 🅱️ Prazos e Conexão de MMGD (Lei 14.300 / REN 1000)
* **Orçamento de Conexão / Parecer de Acesso:** 
  * Microgeração (até 75 kW) sem obras: **15 dias úteis**.
  * Microgeração com obras / Minigeração (> 75 kW): **30 dias úteis**.
  * Minigeração com necessidade de obras na transmissão: **45 dias úteis**.
* **Vistoria e Medição Bidirecional:** Prazo de até **7 dias úteis** após a solicitação para vistoria e adequação da medição.
* **Garantia de Fiel Cumpriremto:** Exigida para minigeração acima de 500 kW no protocolo do Orçamento de Conexão.

#### 🅲 Qualidade do Serviço e Prazos Operacionais
* **Indicadores Individuais (DIC, FIC, DMIC, DICRI):** A violação dos limites de duração e frequência de interrupção gera **compensação financeira automática na fatura** em até 2 ciclos.
* **Corte por Inadimplência:** Exige **notificação prévia por escrito com no mínimo 15 dias de antecedência**. É vedada a suspensão em sextas-feiras, sábados, domingos, feriados e vésperas.
* **Ressarcimento de Danos Elétricos (RDE):** Prazo de até **5 anos** para solicitação. A vistoria pela distribuidora deve ocorrer em até **1 dia útil** (equipamentos de alimentos/medicamentos) ou **10 dias úteis** (demais casos).

---

### 2. 📖 Glossário de Conceitos-Chave

| Sigla / Termo | Conceito Regulatório (REN 1000 / Lei 14.300) |
| :--- | :--- |
| **ACL** | **Ambiente de Contratação Livre:** Mercado onde geradores e consumidores negociam compra e venda de energia livremente. |
| **ACR** | **Ambiente de Contratação Regulada:** Mercado onde consumidores são atendidos pelas distribuidoras sob tarifas reguladas (Mercado Cativo). |
| **DIC / FIC** | **Duração / Frequência de Interrupção Individual:** Indicadores que medem horas (DIC) e vezes (FIC) que uma UC ficou sem energia. |
| **MMGD** | **Micro e Minigeração Distribuída:** Geradores de fonte renovável conectados na rede de distribuição (Micro até 75 kW; Mini acima de 75 kW). |
| **Parecer de Acesso** | Documento emitido pela distribuidora informando viabilidade técnica, ponto de conexão e obras necessárias. |
| **RDE** | **Ressarcimento de Danos Elétricos:** Procedimento regulado para ressarcimento de equipamentos danificados por distúrbios na rede. |
| **SCEE** | **Sistema de Compensação de Energia Elétrica:** Mecanismo em que a energia injetada é cedida para abater o consumo da unidade. |
| **SMF** | **Sistema de Medição para Faturamento:** Conjunto de medidores e comunicação utilizados para registrar o consumo/injeção. |

---

### 3. 🧰 Toolkit de Prompts Reutilizáveis

Coleção de prompts otimizados para rápida consulta regulatória e apoio à consultoria técnica no dia a dia:

#### 🟢 Prompt 1: Contestação de Erro de Faturamento / Devolução em Dobro
```text
Atue como engenheiro e especialista em regulação do setor elétrico. Analise a seguinte situação do meu cliente: [descreva o problema, ex: cobrança por estimativa incorreta / erro de alíquota].
Com base no Capítulo de Faturamento da REN 1000/2021 da ANEEL:
1. Identifique os artigos violados pela distribuidora.
2. Calcule/Explique a regra de devolução em dobro (Art. 323) e os prazos de atualização.
3. Elabore um parágrafo de contestação formal pronto para ser enviado à Ouvidoria.