# 📊 Manual Pessoal de KPIs + Formas de Representação Visual

> Manual pessoal para nortear minhas análises em **Finanças, FP&A e Operações**.  
> A ideia é alimentar este material conforme eu tiver contato com novos indicadores, variáveis e análises.

## Sumário

- [0. Introdução aos KPIs](#0-introdução-aos-kpis)
- [00. Perguntas Norteadoras](#00-perguntas-norteadoras)
- [1. KPIs de Rentabilidade](#1-kpis-de-rentabilidade)
- [2. KPIs de Liquidez](#2-kpis-de-liquidez)
- [3. KPIs de Eficiência](#3-kpis-de-eficiência)
- [4. KPIs de Alavancagem](#4-kpis-de-alavancagem)
- [5. KPIs de Valuation](#5-kpis-de-valuation)
- [6. Como levar os KPIs para Power BI e Excel](#6-como-levar-os-kpis-para-power-bi-e-excel)

---

# 0. Introdução aos KPIs

**KPI — Key Performance Indicator (Indicador-Chave de Desempenho)**

São indicadores utilizados para **medir, avaliar e apoiar decisões**.

Um KPI ajuda a responder:

> **O que está acontecendo? Por quê? E o que precisamos fazer?**

Pode ser utilizado em praticamente qualquer área:

- **Finanças / FP&A**
- **Controladoria**
- **Vendas**
- **Marketing**
- **Recursos Humanos**
- **Logística**
- **Produção / Operações**

Neste manual, o foco será principalmente em **Finanças e Operações**.

---

# 00. Perguntas Norteadoras

## O que são KPIs Financeiros?

São indicadores construídos a partir de dados financeiros e operacionais para acompanhar o **resultado econômico-financeiro e a utilização dos recursos da empresa**.

A ideia é transformar números em informação para apoiar decisões.

### Visão Data-Driven

O profissional de Finanças pode trabalhar com:

**Dados → ETL → Tratamento → Indicadores → Análise → Decisão**

Exemplo:

`ERP / Excel / Banco de Dados → Power Query → Tratamento → Power BI → KPI → Análise`

> O KPI não é simplesmente o número. É o número **organizado dentro de um contexto** para responder uma pergunta de negócio.

---

## Perguntas que quero saber responder

### 📕 Book de Resultados da Companhia

É uma visão consolidada dos principais resultados da empresa em determinado período.

Normalmente pode apresentar:

- Receita;
- Custos;
- Despesas;
- EBITDA;
- Margens;
- Fluxo de caixa;
- Orçamento x realizado;
- Principais desvios;
- KPIs operacionais;
- Comentários sobre os resultados.

**Objetivo:** entender o que aconteceu e explicar os principais desvios.

---

### 💰 Orçamento Anual

Envolve definir uma expectativa para o próximo período.

Pode envolver:

- Receita;
- Custos;
- Despesas;
- CAPEX;
- Headcount;
- Fluxo de caixa;
- Investimentos;
- Premissas de negócio.

Depois:

**Orçado → Realizado → Desvio → Explicação → Plano de ação**

---

### 📢 Divulgação de Resultados

Processo de consolidar e revisar informações financeiras e operacionais para comunicação aos stakeholders e, quando aplicável, ao mercado.

Envolve áreas como:

- Contabilidade;
- Controladoria;
- FP&A;
- Relações com Investidores;
- Tesouraria;
- Jurídico;
- Auditoria.

---

## Como calcular um KPI?

Cada KPI possui uma fórmula ou metodologia própria.

Mas não basta saber calcular.

Preciso entender:

**Fórmula → Fonte do dado → Periodicidade → Meta → Comparação → Causa → Ação**

---

## Como interpretar?

Sempre comparar o indicador com alguma referência:

- Período anterior;
- Orçamento;
- Forecast;
- Meta;
- Benchmark;
- Mesmo período do ano anterior.

Exemplo:

> Receita cresceu 10%, mas margem caiu 3 p.p.

O crescimento da receita, sozinho, não explica o resultado.

---

## Qual periodicidade?

Depende do KPI.

| Periodicidade | Exemplos |
|---|---|
| Diário | Caixa, vendas, contas a pagar |
| Semanal | Inadimplência, vendas, estoque |
| Mensal | DRE, EBITDA, margem, orçamento |
| Trimestral | Resultados corporativos |
| Anual | ROE, orçamento, planejamento estratégico |

---

# 1. KPIs de Rentabilidade

Indicadores utilizados para entender **quanto a empresa consegue gerar de resultado em relação à sua receita, investimentos ou recursos**.

---

## 1.1 Margem de Lucro Bruto

### O que é?

Mostra quanto sobra da receita depois de descontar o **CPV/CSP/CMV**, dependendo do tipo de empresa.

**Lucro Bruto = Receita Líquida − Custo dos Produtos/Serviços Vendidos**

**Margem Bruta = Lucro Bruto ÷ Receita Líquida × 100**

### Implicação prática

Ajuda a entender a **rentabilidade da operação antes das despesas operacionais**.

Se a margem cair, investigar:

- Aumento de custos;
- Preço de venda;
- Mix de produtos;
- Descontos;
- Eficiência operacional.

### Onde obter?

- DRE;
- Contabilidade;
- Controladoria;
- ERP;
- FP&A.

### Visualização

**Power BI:**
- KPI Card → Margem Bruta;
- Linha → evolução mensal;
- Colunas → margem por produto/segmento;
- Waterfall → Receita → Custos → Lucro Bruto.

**Excel:**
- Tabela dinâmica;
- Gráfico de linha;
- Gráfico de colunas;
- Formatação condicional.

---

# 1.2 Margem de Lucro Líquido

### O que é?

Mostra quanto da receita realmente virou **lucro líquido** depois de todos os custos, despesas, resultado financeiro e impostos.

**Lucro Líquido = Receita − Custos − Despesas − Resultado Financeiro − Impostos**

**Margem Líquida = Lucro Líquido ÷ Receita Líquida × 100**

O lucro líquido é importante porque representa o resultado final da companhia após os principais efeitos econômicos e financeiros.

### Implicação prática

Exemplo:

A empresa aumenta a margem de lucro, mas também aumenta a **inadimplência**.

Isso pode indicar que parte das vendas está sendo reconhecida na receita, mas o dinheiro ainda não entrou.

Clientes que não pagam podem aumentar:

- Contas a Receber;
- Aging/Overdue;
- Necessidade de capital de giro;
- PDD/perdas esperadas.

**Resultado contábil ≠ necessariamente dinheiro no caixa.**

### Onde obter?

- DRE;
- Contabilidade;
- Controladoria;
- Contas a Receber;
- Tesouraria.

### Visualização

**Power BI:**
- Card → Margem Líquida;
- Linha → evolução mensal;
- Combo → Receita + Margem;
- Waterfall → Receita até Lucro Líquido.

---

# 1.3 ROI — Return on Investment

### O que é?

Avalia o retorno obtido em relação ao investimento realizado.

**ROI = (Retorno do Investimento − Investimento Inicial) ÷ Investimento Inicial × 100**

Exemplo:

Investimento: R$ 100 mil  
Retorno: R$ 130 mil

ROI:

`(130 − 100) ÷ 100 = 30%`

### Implicação prática

Pode ser utilizado para avaliar:

- Projetos;
- CAPEX;
- Campanhas de marketing;
- Novas iniciativas;
- Investimentos em tecnologia.

Pergunta principal:

> **O retorno gerado justificou o capital investido?**

### Onde obter?

- FP&A;
- Controladoria;
- Marketing;
- Projetos;
- Engenharia;
- Tesouraria.

### Visualização

**Power BI:**
- Card → ROI;
- Barras → ROI por projeto;
- Linha → ROI ao longo do tempo;
- Scatter → Investimento x Retorno.

**Excel:**
- Tabela de projetos;
- ROI calculado;
- Ranking visual por projeto;
- Gráfico de barras.

---

# 1.3.1 Lucratividade

**Lucratividade = Lucro Líquido ÷ Receita Líquida × 100**

Mostra quanto da receita se transforma em lucro líquido.

> É semelhante à margem líquida.

---

# 1.4 Margem de Contribuição

### O que é?

Mostra quanto sobra da receita depois dos **custos e despesas variáveis** para contribuir com os custos fixos e gerar lucro.

**Margem de Contribuição = Receita − Custos Variáveis − Despesas Variáveis**

**MC % = Margem de Contribuição ÷ Receita × 100**

### Implicação prática

Ajuda a analisar:

- Produtos;
- Clientes;
- Serviços;
- Preços;
- Mix de vendas;
- Ponto de equilíbrio.

### Onde obter?

- Contabilidade;
- Controladoria;
- Comercial;
- FP&A;
- Custos.

### Visualização

**Power BI:**
- Barras → MC por produto;
- Waterfall → Receita → Variáveis → MC;
- Scatter → Volume x Margem.

---

# 1.5 ROE e ROA

## ROE — Return on Equity

Mede o retorno gerado sobre o patrimônio dos acionistas/sócios.

**ROE = Lucro Líquido ÷ Patrimônio Líquido × 100**

### Pergunta:

> Quanto a empresa está gerando de resultado para o capital próprio?

---

## ROA — Return on Assets

Mede o retorno gerado em relação aos ativos da empresa.

**ROA = Lucro Líquido ÷ Ativo Total × 100**

### Pergunta:

> Quanto de resultado a empresa consegue gerar utilizando seus ativos?

### Fontes

- Balanço Patrimonial;
- DRE;
- Contabilidade;
- Controladoria.

### Visualização

**Power BI:**
- Cards → ROE / ROA;
- Linha → evolução;
- Colunas → comparação entre períodos/empresas.

---

# 1.6 EBITDA

**EBITDA — Earnings Before Interest, Taxes, Depreciation and Amortization**

No Brasil, também chamado de **LAJIDA**:

> Lucro antes de Juros, Impostos, Depreciação e Amortização.

Uma forma simplificada:

**EBITDA = EBIT + Depreciação + Amortização**

### Para que serve?

Ajuda a analisar o desempenho operacional antes dos efeitos de:

- Juros;
- Impostos;
- Depreciação;
- Amortização.

É muito utilizado em análises de desempenho, comparações e valuation.

### Visualização

**Power BI:**
- Card → EBITDA;
- Card → Margem EBITDA;
- Linha → EBITDA mensal;
- Waterfall → EBITDA Orçado x Realizado;
- Colunas → EBITDA por unidade/segmento.

---

# 2. KPIs de Liquidez

Avaliam a capacidade da empresa de **cumprir suas obrigações financeiras**, principalmente no curto prazo.

---

## 2.1 Liquidez Corrente

**Liquidez Corrente = Ativo Circulante ÷ Passivo Circulante**

### O que mostra?

Capacidade de cobrir obrigações de curto prazo utilizando ativos de curto prazo.

Exemplo:

`Ativo Circulante = R$ 200 mil`  
`Passivo Circulante = R$ 100 mil`

**Liquidez Corrente = 2,0**

### Implicação prática

Um índice acima de 1 indica, em termos contábeis, que o ativo circulante é superior ao passivo circulante.

Mas **não significa automaticamente que a empresa possui caixa disponível**, pois o ativo circulante também pode conter:

- Estoques;
- Contas a Receber;
- Outros ativos.

### Fontes

- Balanço Patrimonial;
- Contabilidade;
- Controladoria.

### Visualização

**Power BI:**
- Card → índice atual;
- Linha → evolução;
- Colunas → comparação entre empresas/unidades.

---

## 2.2 Liquidez Seca

Exclui os estoques do cálculo.

**Liquidez Seca = (Ativo Circulante − Estoques) ÷ Passivo Circulante**

Ajuda a analisar a capacidade de pagamento sem depender da venda dos estoques.

---

## 2.3 Liquidez Imediata

Considera recursos de disponibilidade imediata.

**Liquidez Imediata = Disponibilidades ÷ Passivo Circulante**

Disponibilidades:

- Caixa;
- Bancos;
- Aplicações de liquidez imediata, conforme critério adotado.

---

## 2.4 Liquidez Geral

Considera ativos e obrigações de curto e longo prazo.

**Liquidez Geral = (Ativo Circulante + Realizável a Longo Prazo) ÷ (Passivo Circulante + Passivo Não Circulante)**

---

# 3. KPIs de Eficiência

Medem **como os recursos da empresa estão sendo utilizados**.

---

## 3.1 Produtividade da Mão de Obra

Pode ser adaptada conforme a operação.

Exemplo:

**Produtividade = Produção ÷ Horas Trabalhadas**

Ou:

**Receita ÷ Nº de Funcionários**

### Importante

A fórmula deve ser definida de acordo com o negócio.

### Fontes

- RH;
- Produção;
- Operações;
- Financeiro;
- ERP.

### Visualização

**Power BI:**
- Linha → produtividade mensal;
- Barras → produtividade por equipe/unidade;
- Scatter → Headcount x Receita.

---

# 3.2 Giro de Estoque

Mede quantas vezes o estoque é renovado em determinado período.

**Giro de Estoque = CMV ÷ Estoque Médio**

Também posso acompanhar em dias:

**Dias de Estoque = Estoque Médio ÷ CMV × Nº de dias**

### Implicação prática

Estoque parado pode representar:

- Capital imobilizado;
- Custo de armazenagem;
- Risco de obsolescência.

Estoque muito baixo pode aumentar:

- Rupturas;
- Perda de vendas;
- Problemas operacionais.

### Fontes

- ERP;
- Almoxarifado;
- Logística;
- Compras;
- Contabilidade.

### Visualização

**Power BI:**
- Card → dias de estoque;
- Linha → evolução;
- Heatmap → estoque por categoria;
- Barras → produtos com maior estoque parado.

---

# 3.3 Contas a Receber — Giro / DSO

O giro mostra quantas vezes o contas a receber é convertido em receita/recebimento durante o período.

Para acompanhamento gerencial, também é muito útil utilizar o **DSO — Days Sales Outstanding**:

**DSO = Contas a Receber Médio ÷ Receita a Prazo × Nº de dias**

### Pergunta prática

> Depois que eu faturo, quantos dias normalmente levo para receber?

### Acompanhar junto:

- Aging List;
- Overdue;
- Inadimplência;
- PDD;
- Prazo médio de recebimento.

### Fontes

- Contas a Receber;
- Financeiro;
- Comercial;
- ERP;
- Tesouraria.

### Visualização

**Power BI:**
- Card → DSO;
- Linha → evolução;
- Aging por faixa de atraso;
- Barras → clientes em atraso;
- Matriz → cliente x faixa de vencimento.

---

# 3.4 Taxa de Aproveitamento da Capacidade

Mede quanto da capacidade produtiva disponível está sendo utilizada.

**Utilização da Capacidade = Produção Real ÷ Capacidade Máxima × 100**

### Exemplo

Capacidade máxima: 10.000 unidades  
Produção: 8.000

**Utilização = 80%**

### Fontes

- Produção;
- Operações;
- Engenharia;
- PCP.

### Visualização

**Power BI:**
- Gauge;
- Card;
- Linha;
- Barras → capacidade por unidade.

---

# 4. KPIs de Alavancagem

Medem o grau de utilização de **capital de terceiros/dívida** e ajudam a entender a estrutura financeira da companhia.

---

## 4.1 Índice de Endividamento

Uma forma simples:

**Endividamento = Passivo Total ÷ Patrimônio Líquido**

### Pergunta prática

> Quanto de capital de terceiros existe em relação ao capital próprio?

### Implicação

A análise deve considerar também:

- Custo da dívida;
- Prazo;
- Geração de caixa;
- EBITDA;
- Covenants;
- Perfil da dívida.

### Fontes

- Balanço Patrimonial;
- Tesouraria;
- Contabilidade;
- Controladoria.

### Visualização

**Power BI:**
- Card → índice;
- Linha → evolução;
- Colunas → Dívida x EBITDA;
- Waterfall → evolução da dívida líquida.

---

# 5. KPIs de Valuation

Indicadores utilizados para analisar o **valor de empresas ou ativos**, principalmente em análises de investimento.

---

## 5.1 Lucro por Ação — LPA / EPS

**LPA = Lucro atribuível aos acionistas ÷ Nº de ações**

Mostra quanto de lucro corresponde a cada ação.

---

## 5.2 P/L — Preço sobre Lucro

**P/L = Preço da Ação ÷ Lucro por Ação**

Mostra quanto o mercado está pagando em relação ao lucro por ação.

---

## 5.3 Dividend Yield

**Dividend Yield = Dividendos por Ação ÷ Preço da Ação × 100**

Mostra o dividendo distribuído em relação ao preço da ação.

---

## 5.4 Dividendos por Ação

**DPA = Dividendos Totais ÷ Nº de Ações**

Ajuda a acompanhar quanto foi distribuído por ação.

---

## 5.5 FCF — Free Cash Flow

Fluxo de caixa livre representa o caixa gerado que permanece após os investimentos necessários, conforme a definição adotada na análise.

Uma forma simplificada para FCF operacional:

**FCF = Fluxo de Caixa Operacional − CAPEX**

### Implicação prática

Ajuda a entender a capacidade de geração de caixa depois dos investimentos necessários para manter/desenvolver a operação.

### Fontes

- DFC;
- Contabilidade;
- Tesouraria;
- FP&A;
- CAPEX/Projetos.

### Visualização

**Power BI:**
- Linha → FCF ao longo do tempo;
- Waterfall → EBITDA → Capital de Giro → CAPEX → FCF;
- Card → FCF;
- Colunas → FCF Orçado x Realizado.

---

## 5.6 MVA — Market Value Added

O MVA busca medir o valor criado pela empresa acima do capital investido, dependendo da metodologia utilizada.

Uma forma simplificada:

**MVA = Valor de Mercado − Capital Investido**

### Pergunta

> A empresa criou valor acima do capital que foi investido nela?

---

# 6. Como levar os KPIs para Power BI e Excel

## 🟡 Power BI

Minha lógica:

**Fonte → Power Query → Modelo → DAX → KPI → Visual → Análise**

### Visual adequado para cada situação

| Objetivo | Visual |
|---|---|
| Número principal | Card |
| Evolução no tempo | Linha |
| Comparar categorias | Barras |
| Participação | Barras empilhadas |
| Orçado x Realizado | Colunas / Waterfall |
| Composição do resultado | Waterfall |
| Relação entre duas variáveis | Scatter |
| Acompanhamento de meta | Gauge / KPI |
| Aging | Matriz / Barras |
| Distribuição | Histograma |
| Detalhamento | Tabela / Matriz |

---

## 🟢 Excel

Ferramentas principais:

- Tabela;
- Tabela Dinâmica;
- Gráfico Dinâmico;
- Formatação Condicional;
- SOMASE/SOMASES;
- CONT.SE/CONT.SES;
- SE;
- PROCV/PROCH;
- PROCX, quando disponível;
- Power Query;
- Power Pivot.

### Estrutura que quero praticar

**Base de dados → Tratamento → Cálculo → Tabela dinâmica → Dashboard**

---

# 7. Estrutura mental para qualquer KPI

Quando encontrar um novo indicador, quero responder:

### 1. O que ele mede?
Qual pergunta de negócio responde?

### 2. Qual a fórmula?
Quais variáveis entram no cálculo?

### 3. De onde vêm os dados?
ERP? DRE? Balanço? CRM? RH? Operações?

### 4. Quem é o responsável pelo dado?
Financeiro? Contabilidade? Comercial? Logística? Produção?

### 5. Qual a periodicidade?
Diária? Semanal? Mensal? Trimestral?

### 6. Qual é a referência?
Meta? Orçamento? Forecast? Ano anterior?

### 7. O que significa quando sobe ou cai?
Qual possível causa?

### 8. Qual ação pode ser tomada?
O KPI precisa levar a uma decisão.

### 9. Como representar?
**Card → tendência → comparação → detalhamento**

> **KPI bom não é apenas um número bonito no dashboard. É um indicador que ajuda a enxergar um problema, explicar uma causa e apoiar uma decisão.**

---

# 8. Fontes de dados que quero conhecer melhor

| Informação | Área/Fonte |
|---|---|
| DRE | Contabilidade / Controladoria |
| Balanço | Contabilidade |
| Fluxo de Caixa | Tesouraria |
| Contas a Pagar | Financeiro |
| Contas a Receber | Financeiro / Comercial |
| Inadimplência | Financeiro / Crédito |
| Estoque | Logística / Supply Chain |
| Compras | Compras / Suprimentos |
| Vendas | Comercial |
| Headcount | RH |
| Produção | Operações / PCP |
| CAPEX | Engenharia / Projetos / FP&A |
| Orçamento | FP&A / Controladoria |
| Forecast | FP&A |
| Indicadores corporativos | FP&A / Controladoria |

---

# 9. Modelo de análise que quero aplicar

**Dado**

↓  

**Tratamento**

↓  

**KPI**

↓  

**Comparação**

`Realizado x Orçado`

`Atual x Anterior`

`Atual x Forecast`

↓  

**Análise do desvio**

↓  

**Causa**

↓  

**Plano de ação**

---

## 🎯 Objetivo do manual

Construir uma visão cada vez mais prática de **Finanças + Dados + Negócios**, conectando:

**Contabilidade → Finanças → Operações → Dados → BI → Decisão**

Não quero apenas saber calcular um indicador.

Quero entender **de onde vem o dado, o que ele significa para o negócio, como visualizá-lo e qual decisão ele pode apoiar.**




























(chat organize para formato de README dde forma sucinta (sen estender os conceitos) como se fossem anotações e com palavras simples (como eu escrevi em alguns) com eu escreveria: O que o kpi e suas implicações práticas, como obter (fontes ou departamentos dentro da empresa), e o mais importantes como representá-lo visualemente no powerbi e execel) 


# Manual Pessoal de KPIs + Formas de representação Vizual

Criei esse manual para nortear minhas análises em finanças, aqui pretendo ir alimentando a medida que eu for tendo contato com varáveis e etttc

Sumário:

Introdução aos KPIs
Perguntas Norteadoras
 KPI’s de RENTABILIDADE
KPI’s de LIQUIDEZ (Geral, Corrente, Seca, Imediata)
 KPI’s de Eficiencia 
 KPI’s de Alavancagem
 KPIs de Valuation

0. Introdução aos KPIs

KPI - Indicadores Chave de Perfomance (Key Performance Indicators)

São indicadores para Medir, Avaliar, Decidir, Alterar planos de ação para melhor tomada de decisão.

Ele pode ser usado em vários contextos dentro de uma empresa, esse manual será Focado em Finanças e Operacional, mas inteligente pode ser gerada em todos os processos em uma empresa como em existem  recursoso humanos, Logistica, (chat: citar mais 3)


00. Perguntas Norteadoras

### Oque são KPIS Financeiros?
Olhar para analise quantitativa, dos númeirs, que vão refletiro resultado financeiro de uma empresa. São usados paar medir eficácian a gestã odos recursos.

Servem para tronar a decisão mais rápida baseado em dados.

É desenvovida pelo profissional definanças quw tem uma visão Data-Driven, que engloba BI, visão ETL (Extrair, transofmrar e carregar dados), comnhecimentos em Power Query. daqui extra-se a informação lapidada.

É KPI é aquel infomração lapidada

- O que é elaborar um "Book de resultados da Companhia"?
- O que está envolvidos na constrção do "Orçamento Anual da companhia"
- Como é o processo d e PROCESSO DE DIVULGAÇÃO DE RESULTADOS DA COMPANHIA AO MERCADO?

### Como calcular os KPIs Fonceniro

Cada KPI tem uma forma decalcular ou por meio de uma formula ou (...)

### Como interpretar os resultados do KPIs

### Qual periodicidade para controlar os KPIs em finanaças?


1. KPI’s de RENTABILIDADE

(chat descreva de forma sucinta como em uma bloco de anotações e com palavras simples com eu escreveria: O que o indicador e suas implicações práticas, como obter (fontes ou departamentos dentro da empresa), e o mais importantes como representá-lo visualemente no powerbi e execel) 

1.1  Margem de Lucro Bruto
Ele será a receita - o custo do produto vendido (ou custo de produto custo do produto vendidoo

LB = Rceita - CPV

OU pela pocentagem, pegando LB dividindp pela receita total e multiplicando por 1000
(LB * REC) x100 --> Margem Liquida

1.2 Margem de Lucro Líquidp
Lucro Líquido, é a ultima linha da DRE, é o que mais interessa ao dono (porque e de exemplos do porque)

LL = Rceita - todos os custos e despesas. 

A magem Liquida será o lucro liquid dividido pela Receita Total x100

Exemplo do dia a dia: Aumento na margem de lucro em contra partida aumento na taxa de indimplencia (Contas a receber) 
(Chat explique essa implicação citando clientes que não pagam)

1.3 ROI (Return on Investment)

Para avaliar o suceosso de projetos ou iniciativas invest (capex), campanhas de marketing. Teve retorno de investimento ou não teve?

Lucro Liquido - Investimento Inicial / Pelo proprio invetsimento inical x100
(Chat: reflita a formula)

1.3.1 Lucratividade

(Lucro Liquido / receita) x100

1.4 Margem de Contribuição

1.5 ROE (Equity) / ROA (Asset)

ROE = (lUCRO LIQUIDO / PATRIMONIO LIQUDO ) X100

ROA = (lUCROLIQUIDO / Stivo Total) x 100

1.6 EBITDA
  Também chamdo de LAJIDA (Lucro Anttes de Jueros Impostos Depreciação e Amortização).
  Com ele se mede o resulatdo operacional da empresa



2. KPI’s de LIQUIDEZ (Geral, Corrente, Seca, Imediata)

Liquidez Corrente

Ativo Circulante / Passivo Circulante


3. KPI’s de Eficiencia

3.1 Produtividade de Mão de cobra (Vinculada ao operacional)
3.2 Giro de Estoque (Rotatividade) - Quando tempo leva para entrar produtos novos e oque que estão ali saírsm.
3.3 Giro de Contas a Receber (Quanto tempo depois de faturar entra dinehiro no caixa (Contas a receber), evitando atrasos aging list/Overdue  ou  aquelies recebiveis que pode acabar virando um PDD e nunca mais recuperar o dinheiro)
3.4 Taxa de Aproveitamento de Capacidade  - Mdir se acapcidade de produção.
(Produção Real / Capacidade Máxima de Produção)


4. KPI’s de Alavancagem

Mede o Gradu de individdamento da companhia gerenciar suas dívidas.
ENDIVIDAMENTTO
Passivo total / Patromoni liquido

5. KPIs de Valuation (Avaliação) (De investimento ou Empresas)

5.1 Lucro por Ação
5.2 Relação Preço/Lucro
5.3 Dividendo YIELD
5.4 (Dividendo / Ação) - Dividendo anual dividido pelo preço da ação.
5.5 CFC (Free Chash Flow) - Fluxo de Caixa livre para Acionista
5.6 MVA (Market Value Market)




- O que é elaborar um "Book de resultados da Companhia"?
- O que está envolvidos na constrção do "Orçamento Anual da companhia"
- Como é o processo d e PROCESSO DE DIVULGAÇÃO DE RESULTADOS DA COMPANHIA AO MERCADO?





