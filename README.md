# 📊 Manual Pessoal de KPIs + Formas de Representação Visual

> Manual pessoal para nortear minhas análises em **Finanças, FP&A e Operações**.  
> A ideia é alimentar este material conforme eu tiver contato com novos indicadores, variáveis e análises.

## Sumário

- [Introdução aos KPIs](#introdução-aos-kpis)
- [Perguntas Iniciais](#Perguntas-Iniciais)
- [1. KPIs de Rentabilidade](#1-kpis-de-rentabilidade)
- [2. KPIs de Liquidez](#2-kpis-de-liquidez)
- [3. KPIs de Eficiência](#3-kpis-de-eficiência)
- [4. KPIs de Alavancagem](#4-kpis-de-alavancagem)
- [5. KPIs de Valuation](#5-kpis-de-valuation)
- [6. Como levar os KPIs para Power BI e Excel](#6-como-levar-os-kpis-para-power-bi-e-excel)
- [7. Conceitos importantes](#7-conceitos-importantes)
    7.1 [Book de resultados da companhia](#1-book-de-resultados-da-companhia)
    7.2 [Budget x Forecast x Realizado e plano orçamentário com rateio](#2-budget-x-forecast-x-realizado)
    7.3 [Real x Orçado x Ano Anterior](#3-real-x-orçado-x-ano-anterior)
    7.4 [P&L ou PnL — Profit and Loss Statement](#4-pl-ou-pnl--profit-and-loss-statement)
    7.5 [Fechamento mensal ou Closing](#5-fechamento-mensal-ou-closing)
    7.6 [Processo de validar a base do ERP](#6-processo-de-validar-a-base-do-erp)
    7.7 [Balancete x Base do ERP](#7-balancete-x-base-do-erp)
    7.8 [Como todos esses conceitos se conectam no dia a dia](#8-como-todos-esses-conceitos-se-conectam-no-dia-a-dia)

---
# Resumo dos KPIs desenvolvidos

| Nome do KPI | Grupo | Definição breve do KPI | Formas de visualização no Power BI |
|---|---|---|---|
| **Margem de Lucro Bruto** | Rentabilidade | Mostra quanto sobra da receita após os custos diretamente ligados aos produtos/serviços vendidos. | **Card**, linha de evolução, colunas por produto/segmento, **Waterfall** |
| **Margem de Lucro Líquido** | Rentabilidade | Mostra quanto da receita se transforma em lucro líquido depois de custos, despesas, resultado financeiro e impostos. | **Card**, linha, gráfico combinado Receita x Margem, **Waterfall** |
| **ROI** | Rentabilidade | Mede o retorno obtido em relação ao investimento realizado. | **Card**, barras por projeto, linha temporal, **Scatter** Investimento x Retorno |
| **Lucratividade** | Rentabilidade | Mostra quanto da receita se transforma em lucro líquido. | **Card**, linha temporal, colunas por período/segmento |
| **Margem de Contribuição** | Rentabilidade | Mostra quanto sobra da receita após custos e despesas variáveis para cobrir custos fixos e gerar lucro. | **Card**, barras por produto, **Waterfall**, Scatter Volume x Margem |
| **ROE** | Rentabilidade | Mede o retorno gerado sobre o patrimônio líquido da empresa. | **Card**, linha de evolução, colunas por período/empresa |
| **ROA** | Rentabilidade | Mede o retorno gerado em relação aos ativos da empresa. | **Card**, linha de evolução, colunas por período/empresa |
| **EBITDA** | Rentabilidade | Mede o resultado operacional antes de juros, impostos, depreciação e amortização. | **Card**, linha mensal, colunas por unidade/segmento, **Waterfall** |
| **Margem EBITDA** | Rentabilidade | Mostra quanto da receita representa o EBITDA. | **Card**, linha temporal, colunas por segmento, gráfico combinado |
| **Liquidez Corrente** | Liquidez | Mede a capacidade de cobrir obrigações de curto prazo com ativos de curto prazo. | **Card**, linha de evolução, colunas por empresa/unidade |
| **Liquidez Seca** | Liquidez | Mede a capacidade de pagamento de curto prazo desconsiderando os estoques. | **Card**, linha, colunas comparativas |
| **Liquidez Imediata** | Liquidez | Mede a capacidade de pagar obrigações de curto prazo utilizando disponibilidades imediatas. | **Card**, linha de evolução, colunas comparativas |
| **Liquidez Geral** | Liquidez | Avalia a capacidade de pagamento considerando ativos e obrigações de curto e longo prazo. | **Card**, linha, colunas comparativas |
| **Produtividade da Mão de Obra** | Eficiência | Mede a produção ou resultado gerado em relação aos recursos humanos utilizados. | **Card**, linha temporal, barras por equipe/unidade, **Scatter** |
| **Giro de Estoque** | Eficiência | Mede quantas vezes o estoque é renovado em determinado período. | **Card**, linha, barras por produto/categoria, **Heatmap** |
| **Dias de Estoque** | Eficiência | Estima por quantos dias o estoque atual consegue atender ao consumo/vendas. | **Card**, linha, barras por produto, **Heatmap** |
| **DSO / Prazo Médio de Recebimento** | Eficiência | Mede quantos dias, em média, a empresa leva para receber suas vendas a prazo. | **Card**, linha, barras por cliente, **Aging**, matriz |
| **Inadimplência** | Eficiência / Crédito | Mede o volume ou percentual de valores vencidos e não recebidos. | **Card**, linha, barras por cliente, **Aging**, matriz por faixa de atraso |
| **Taxa de Utilização da Capacidade** | Eficiência | Mede quanto da capacidade produtiva disponível está sendo utilizada. | **Gauge**, **Card**, linha, barras por unidade |
| **Índice de Endividamento** | Alavancagem | Mede o nível de capital de terceiros em relação ao capital próprio. | **Card**, linha de evolução, colunas, **Waterfall** da dívida |
| **Dívida Líquida / EBITDA** | Alavancagem | Relaciona a dívida líquida com o EBITDA, ajudando a acompanhar o nível de alavancagem. | **Card**, linha temporal, colunas comparativas |
| **Lucro por Ação (LPA/EPS)** | Valuation | Mostra quanto do lucro corresponde a cada ação. | **Card**, linha temporal, colunas |
| **P/L (Preço/Lucro)** | Valuation | Compara o preço da ação com o lucro gerado por ação. | **Card**, linha temporal, Scatter |
| **Dividend Yield** | Valuation | Mostra o dividendo distribuído em relação ao preço da ação. | **Card**, linha, colunas comparativas |
| **Dividendos por Ação (DPA)** | Valuation | Mostra quanto foi distribuído em dividendos para cada ação. | **Card**, linha, colunas |
| **Free Cash Flow (FCF)** | Valuation / Caixa | Mede o caixa livre gerado após os investimentos necessários, conforme a metodologia utilizada. | **Card**, linha temporal, **Waterfall**, Orçado x Realizado |
| **MVA** | Valuation | Mede a diferença entre o valor de mercado da empresa e o capital investido. | **Card**, linha temporal, colunas comparativas |

---
# Introdução aos KPIs

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

# Perguntas iniciais

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
# 7. Conceitos importantes

## 7.1. Book de resultados da companhia

### O que é?

O *book de resultados* é uma apresentação gerencial que reúne os principais números da empresa em determinado período, geralmente um mês, trimestre ou acumulado do ano.

Na prática, é uma forma de transformar uma grande quantidade de dados financeiros em uma história que a diretoria consiga entender: **quanto vendemos, quanto gastamos, quanto ganhamos, onde ficamos acima ou abaixo do esperado e por que isso aconteceu?**

Não basta colocar tabelas e gráficos em um PowerPoint. O objetivo é explicar o resultado e ajudar a gestão a decidir o que fazer a seguir.

### Exemplo prático

Imagine que você trabalha no FP&A de uma empresa de relógios e acabou de receber os resultados de setembro. A diretoria quer saber:

- A receita ficou dentro do orçamento?
- O custo dos produtos vendidos aumentou proporcionalmente às vendas?
- As despesas comerciais cresceram?
- A margem de lucro melhorou ou piorou?
- O que explica a diferença entre o resultado esperado e o realizado?

O assistente ou estagiário pode ajudar a atualizar as bases, conferir os números, calcular as variações, atualizar os gráficos e preparar comentários preliminares. A análise final costuma ser revisada pelo analista ou gestor.

### Como um book pode ser estruturado?

1. **Resumo executivo:** principais destaques do mês, como receita, margem, EBITDA, despesas e maiores desvios.
2. **Receita e vendas:** comparação entre realizado, orçamento e ano anterior, com explicações sobre volume, preço, mix de produtos e canais.
3. **DRE gerencial e margens:** receita líquida, custos, lucro bruto, despesas operacionais, EBITDA e resultado final, conforme o modelo de reporte.
4. **Despesas e análise de desvios:** quais áreas gastaram mais ou menos que o previsto e quais explicações foram identificadas.
5. **Próximos passos:** pontos de atenção, perguntas em aberto e ações a acompanhar.

### Exemplo numérico: comentário do resultado

Imagine os seguintes dados de receita líquida:

| Indicador | Valor |
|---|---:|
| Orçamento de setembro | R$ 10 milhões |
| Realizado de setembro | R$ 9 milhões |
| Realizado em setembro do ano anterior | R$ 8,5 milhões |

O realizado ficou R$ 1 milhão abaixo do orçamento, uma variação desfavorável de 10%.

`(9 - 10) / 10 × 100 = -10%`

Por outro lado, a receita cresceu aproximadamente 5,9% em relação ao ano anterior.

`(9 - 8,5) / 8,5 × 100 ≈ 5,9%`

Esses números contam duas histórias diferentes: a empresa cresceu em relação ao ano passado, mas não atingiu o que havia planejado para setembro.

**Exemplo de comentário gerencial:**

> A receita líquida de setembro totalizou R$ 9 milhões, ficando 10% abaixo do orçamento. Apesar do desvio negativo em relação ao planejado, houve crescimento de aproximadamente 5,9% na comparação com setembro do ano anterior. Para explicar o resultado, é necessário aprofundar a análise de volume de vendas, preço médio, mix de produtos e desempenho dos canais comerciais.

O comentário não inventa uma causa para a diferença. Ele apresenta o fato e indica o que precisa ser investigado.

### O que o estagiário ou assistente precisa saber fazer?

- Atualizar as bases e os gráficos do book.
- Conferir se os números apresentados batem com a base financeira oficial.
- Calcular variações em reais e percentuais.
- Comparar o mês, o acumulado do ano e, quando solicitado, os trimestres.
- Identificar os maiores desvios e pedir esclarecimentos às áreas responsáveis.
- Escrever comentários objetivos, separando fatos confirmados de hipóteses.

**Aprendizado principal:** o book não é apenas uma apresentação de números. É uma ferramenta para explicar o desempenho financeiro da empresa.

---
## 7.2. Budget x Forecast x Realizado

Esses três conceitos estão conectados e formam uma das bases do trabalho de FP&A. Cada um responde a uma pergunta diferente.

| Conceito | Pergunta principal | Significado |
|---|---|---|
| **Budget (orçamento)** | O que planejamos gastar ou receber? | Plano financeiro aprovado para determinado período, construído a partir de premissas de receita, custos, despesas, investimentos e metas. |
| **Forecast (previsão atualizada)** | Considerando o que já aconteceu, quanto esperamos gastar ou receber? | Projeção revisada com base nos resultados realizados, nas novas informações e nas premissas atualizadas. Pode mudar durante o ano. |
| **Realizado** | Quanto efetivamente foi registrado no período? | Resultado apurado a partir dos registros financeiros e contábeis validados. Para o reporte, deve-se utilizar a versão oficial do fechamento. |

### Exemplo prático: orçamento de despesas de marketing

Imagine que a área de Marketing tenha planejado investir R$ 120 mil em campanhas durante o ano. No planejamento, a despesa foi distribuída entre os meses. Em março, houve uma campanha adicional e, em abril, uma renegociação com a agência.

| Mês | Budget | Forecast atualizado | Realizado |
|---|---:|---:|---:|
| Janeiro | R$ 10 mil | R$ 10 mil | R$ 9 mil |
| Fevereiro | R$ 10 mil | R$ 10 mil | R$ 11 mil |
| Março | R$ 10 mil | R$ 15 mil | R$ 16 mil |
| Abril | R$ 10 mil | R$ 8 mil | Ainda não fechado |

Os valores são ilustrativos.

Em janeiro, a empresa gastou R$ 9 mil, embora tivesse planejado R$ 10 mil. Em fevereiro, gastou R$ 11 mil, ultrapassando o orçamento mensal em R$ 1 mil.

Em março, a equipe revisou a previsão para R$ 15 mil devido à campanha adicional, mas o gasto final chegou a R$ 16 mil.

Em abril, a previsão foi reduzida para R$ 8 mil por conta da renegociação. Como abril ainda não foi fechado, esse valor é uma expectativa, não um resultado realizado.

**O ponto central:** o Budget registra o plano aprovado; o Forecast registra a expectativa mais atual; e o Realizado mostra o que aconteceu.

O Budget não deve ser sobrescrito para fazer os números parecerem alinhados ao resultado. Ele precisa permanecer disponível como referência de comparação.

### O que é o plano orçamentário com rateio?

O plano orçamentário é mais do que uma lista de despesas. É a distribuição do planejamento financeiro entre períodos, áreas, contas contábeis, centros de custo e, conforme a estrutura da empresa, projetos ou unidades de negócio.

O **rateio** é a distribuição de um valor entre diferentes áreas ou objetos de custo, seguindo um critério definido.

Imagine que a empresa tenha uma despesa anual de R$ 120 mil com uma ferramenta de software utilizada por três departamentos:

| Área | Critério de rateio | Participação | Valor mensal |
|---|---|---:|---:|
| Comercial | Quantidade de usuários | 50% | R$ 5.000 |
| Marketing | Quantidade de usuários | 30% | R$ 3.000 |
| Financeiro | Quantidade de usuários | 20% | R$ 2.000 |
| **Total** | | **100%** | **R$ 10.000** |

Nesse exemplo, o rateio é feito conforme a quantidade de usuários de cada departamento. Em uma empresa real, o critério pode ser quantidade de funcionários, utilização efetiva, área ocupada, receita, transações ou outro direcionador apropriado.

A escolha precisa fazer sentido para a despesa. Não seria adequado, por exemplo, distribuir automaticamente todos os custos de tecnologia proporcionalmente à receita se o consumo do serviço for muito diferente entre os departamentos.

### Como isso aparece na rotina do assistente ou estagiário?

Você pode receber uma planilha de orçamento com as seguintes colunas:

- Conta contábil;
- Centro de custo;
- Departamento;
- Mês;
- Valor orçado;
- Responsável pela despesa.

Sua tarefa pode ser conferir se os valores foram distribuídos corretamente, verificar se o rateio totaliza 100%, validar se os centros de custo existem e comparar o orçamento com o que foi registrado no ERP.

Se o orçamento de Marketing prevê R$ 3 mil por mês para a ferramenta, mas o ERP apresenta R$ 5 mil como despesa de Marketing, você precisa investigar. Pode ter ocorrido uma mudança no rateio, um lançamento no centro de custo errado, uma cobrança adicional ou uma diferença de competência.

Não se deve simplesmente alterar a planilha para fazê-la bater com o ERP. Primeiro é preciso identificar a causa da diferença e validar o tratamento correto com o responsável.

**Importante:** rateio não é necessariamente pagamento. Se uma despesa de R$ 10 mil for redistribuída entre três departamentos, o custo total da companhia continua sendo R$ 10 mil. O que muda é a distribuição gerencial desse custo.

**Aprendizado principal:** o Budget organiza o plano financeiro; o Forecast atualiza a expectativa; o Realizado mostra o resultado; e o rateio permite visualizar a responsabilidade por custos e despesas.

---

## 7.3. Real x Orçado x Ano Anterior

Essa comparação é uma das formas mais comuns de analisar o desempenho financeiro. Embora pareça semelhante à comparação entre Budget, Forecast e Realizado, aqui o foco é entender as diferenças entre o que aconteceu, o que havia sido planejado e o que aconteceu no passado.

- **Realizado:** o que aconteceu no período atual?
- **Orçado:** o que a empresa esperava que acontecesse?
- **Ano anterior:** o que aconteceu no período equivalente do ano passado?

### Exemplo prático: receita líquida

Imagine que você esteja preparando o relatório de setembro.

| Indicador | Valor |
|---|---:|
| Realizado em setembro | R$ 9 milhões |
| Orçado para setembro | R$ 10 milhões |
| Realizado em setembro do ano anterior | R$ 8,5 milhões |

A primeira comparação mostra que a empresa ficou abaixo do plano. A segunda mostra que, apesar de não atingir a meta, houve crescimento em relação ao ano anterior.

| Comparação | Variação em R$ | Variação em % |
|---|---:|---:|
| Realizado x Orçado | -R$ 1 milhão | -10,0% |
| Realizado x Ano anterior | +R$ 500 mil | +5,9% |

A fórmula geral para calcular a variação percentual é:

`Variação % = (Realizado - Referência) / Referência × 100`

A referência pode ser o orçamento ou o resultado do ano anterior, dependendo da comparação que você deseja fazer.

### Como interpretar o resultado?

Se a receita cresceu 5,9% em relação ao ano anterior, isso não significa necessariamente que a empresa está indo bem. Ela pode ter planejado crescer 20%, por exemplo.

Da mesma forma, ficar abaixo do orçamento não significa automaticamente que o desempenho foi ruim em todos os aspectos. A empresa pode ter vendido menos, mas melhorado sua margem ou reduzido despesas de forma relevante.

É por isso que a comparação precisa ser acompanhada de uma análise das causas.

Em uma companhia de relógios, você poderia investigar:

- Volume de unidades vendidas;
- Preço médio;
- Mix de marcas e produtos;
- Desempenho dos canais de venda;
- Descontos comerciais;
- Sazonalidade;
- Lançamentos ou campanhas;
- Eventuais mudanças no calendário de vendas.

### Variação percentual x pontos percentuais

Esse cuidado é importante quando você estiver analisando margens.

Imagine que a margem bruta tenha sido de 40% no ano anterior e 36% no ano atual.

A redução foi de **4 pontos percentuais (p.p.)**, porque `36% - 40% = -4 p.p.`.

Já a queda relativa da margem foi de 10%:

`(36% - 40%) / 40% × 100 = -10%`

Os dois números estão corretos, mas representam coisas diferentes.

### Como registrar esse aprendizado

Na análise de resultados, não devo olhar apenas para o valor realizado. Preciso compará-lo com o orçamento e com o mesmo período do ano anterior, pois cada referência mostra uma informação diferente. O orçamento indica se a empresa cumpriu o que havia planejado; o ano anterior ajuda a entender a evolução do negócio.

Depois de calcular a variação em reais e em percentual, devo investigar as causas dos desvios relevantes. O objetivo não é apenas dizer que a receita caiu ou que a despesa aumentou, mas entender o que provocou essa mudança e qual foi o impacto no resultado financeiro.

**Aprendizado principal:** comparar números identifica o desvio; analisar as causas transforma esse desvio em informação útil para a gestão.

---

## 7.4. P&L ou PnL — Profit and Loss Statement

### O que é?

P&L é a abreviação de *Profit and Loss Statement*, equivalente, em termos gerais, à demonstração de resultados. No Brasil, é comum usar a sigla **DRE (Demonstração do Resultado do Exercício)**.

Em FP&A, o termo também pode se referir à visão gerencial de receitas, custos e despesas utilizada para analisar o desempenho de um mês, de uma unidade de negócio, de uma marca ou da companhia como um todo.

A P&L gerencial pode ter agrupamentos e indicadores adicionais aos da DRE contábil. Por isso, é importante conhecer as regras de classificação e reconciliação da empresa.

### Como ler uma P&L na prática?

Imagine que uma companhia tenha apresentado o seguinte resultado mensal:

| Linha da P&L | Valor ilustrativo |
|---|---:|
| Receita bruta | R$ 12.000.000 |
| (-) Deduções e impostos sobre vendas | R$ 3.000.000 |
| **Receita líquida** | **R$ 9.000.000** |
| (-) Custo dos produtos vendidos | R$ 4.950.000 |
| **Lucro bruto** | **R$ 4.050.000** |
| (-) Despesas operacionais | R$ 2.700.000 |
| **Resultado operacional antes de outros itens** | **R$ 1.350.000** |

Os valores são hipotéticos, e a estrutura exata depende do modelo gerencial utilizado.

O primeiro cuidado é entender que **receita bruta não é a mesma coisa que receita líquida**, e que faturamento não representa necessariamente dinheiro recebido no caixa.

As deduções e os impostos aplicáveis reduzem a receita bruta até chegar à receita líquida. Depois, os custos associados aos produtos vendidos são deduzidos para calcular o lucro bruto.

As despesas operacionais, por sua vez, podem incluir despesas comerciais, administrativas, marketing, tecnologia, pessoal e outras despesas da operação.

### Como o FP&A usa a P&L?

A P&L permite responder perguntas como:

- A empresa vendeu mais, mas também gastou mais?
- A margem bruta melhorou?
- O crescimento das despesas operacionais foi maior que o crescimento da receita?
- Qual área está pressionando o resultado?
- Qual marca ou canal apresenta melhor rentabilidade?

Considere que a receita líquida seja de R$ 9 milhões e o lucro bruto de R$ 4,05 milhões.

A margem bruta é:

`Margem Bruta = Lucro Bruto / Receita Líquida × 100`

`4,05 / 9 × 100 = 45%`

Isso significa que, a cada R$ 100 de receita líquida, restam R$ 45 após a dedução do custo dos produtos vendidos, antes das despesas operacionais e dos demais itens posteriores da demonstração.

### Exemplo: a receita cresceu, mas a margem bruta caiu

Imagine que no mês anterior a receita líquida fosse de R$ 8 milhões e o lucro bruto de R$ 3,76 milhões. A margem bruta era de 47%.

No mês atual, a receita líquida aumentou para R$ 9 milhões, mas a margem bruta caiu para 45%.

A empresa cresceu em receita, porém reteve uma parcela menor dessa receita após os custos dos produtos vendidos.

O assistente pode organizar a comparação por marca, produto ou canal e destacar as linhas que mais contribuíram para a variação. O analista pode aprofundar a investigação em descontos, preço de compra, frete, mix de produtos e outros fatores relevantes.

A causa, entretanto, precisa ser confirmada pelos dados. Não é correto concluir que a margem caiu por causa de descontos apenas porque essa é uma hipótese plausível.

### EBITDA: onde entra?

O EBITDA é um indicador de desempenho operacional que, em termos gerais, parte do resultado operacional e exclui juros, tributos sobre o lucro e depreciação e amortização, conforme a metodologia adotada.

Em uma P&L gerencial, ele costuma aparecer depois das despesas operacionais e antes de itens financeiros, tributos sobre o lucro e depreciação e amortização, mas a apresentação exata varia.

Não confunda EBITDA com lucro líquido ou fluxo de caixa. Ele não representa, sozinho, o dinheiro efetivamente disponível na conta bancária.

**Aprendizado principal:** a P&L organiza a formação do resultado. Para trabalhar bem com ela, é preciso entender cada linha, sua classificação e como as mudanças em receitas, custos e despesas afetam as margens.

---

## 7.5. Fechamento mensal ou Closing

### O que é o closing?

O *closing* é o processo de fechamento contábil e financeiro de um período, geralmente mensal. É quando a empresa organiza, registra e valida as informações referentes ao mês para conseguir apresentar um resultado confiável.

Em termos simples, a empresa precisa garantir que os acontecimentos de setembro estejam corretamente registrados em setembro, que as despesas e receitas estejam classificadas de forma adequada e que os relatórios financeiros reflitam o que realmente aconteceu.

O fechamento normalmente envolve Contabilidade, Controladoria, Financeiro, Fiscal, áreas operacionais e FP&A. As responsabilidades variam conforme a estrutura da companhia.

Uma distinção importante: a Contabilidade é responsável pelos registros contábeis e pelos procedimentos de fechamento sob sua alçada; FP&A utiliza os números validados para analisar o desempenho, explicar desvios e atualizar as projeções.

### Como funciona o closing na prática?

Imagine que estamos no início de outubro e a empresa precisa fechar o resultado de setembro.

1. **Coleta dos dados do período:** a equipe reúne lançamentos de receitas, despesas, custos, notas fiscais, folha de pagamento, movimentações de estoque e demais informações relevantes.
2. **Conferência dos registros:** a Contabilidade e as áreas responsáveis verificam se os lançamentos foram registrados corretamente, se pertencem ao período adequado e se existem documentos ou informações pendentes.
3. **Ajustes e conciliações:** são avaliados itens como despesas incorridas ainda não faturadas, provisões, despesas antecipadas e saldos contábeis. Os ajustes necessários são realizados pelos responsáveis autorizados.
4. **Validação do resultado:** são gerados relatórios contábeis, incluindo o balancete e a DRE, e feitas verificações de consistência dos saldos e movimentações.
5. **Análise de resultados pelo FP&A:** com os dados oficiais disponíveis, FP&A compara o realizado com o orçamento, o forecast e o ano anterior, investigando os desvios relevantes.
6. **Reporte gerencial:** os resultados são consolidados em planilhas, dashboards e no book de resultados para apresentação à liderança.

### Exemplo: despesa de setembro paga em outubro

Imagine que a empresa contratou uma agência de marketing para prestar serviços durante setembro, no valor de R$ 20 mil. A nota fiscal só será recebida em outubro, e o pagamento ocorrerá posteriormente.

Se o serviço foi efetivamente prestado em setembro e os critérios contábeis aplicáveis forem atendidos, a despesa deverá ser reconhecida no período correto, mesmo que o pagamento aconteça depois.

Esse é o conceito de **competência contábil**: reconhecer receitas e despesas no período a que se referem, em vez de considerar apenas a data em que o dinheiro entra ou sai do caixa.

Se essa despesa não for reconhecida no mês adequado, o resultado de setembro poderá ficar artificialmente melhor, enquanto o de outubro poderá ficar artificialmente pior.

O tratamento exato depende dos documentos, das condições contratuais e das regras contábeis aplicáveis.

### O que o estagiário ou assistente pode fazer durante o closing?

- Atualizar controles de fechamento e acompanhar prazos.
- Organizar as bases extraídas do ERP.
- Conferir lançamentos, classificações e centros de custo.
- Identificar despesas com valores incomuns ou movimentos fora do padrão.
- Comparar saldos com o mês anterior e com o orçamento.
- Documentar diferenças e solicitar esclarecimentos às áreas responsáveis.
- Preparar relatórios preliminares para revisão do analista.

O profissional júnior não precisa tomar sozinho decisões sobre ajustes contábeis. O importante é identificar inconsistências, reunir evidências, entender a causa e encaminhar o problema ao responsável.

**Aprendizado principal:** o closing transforma os registros do período em números oficiais e confiáveis. O trabalho de FP&A depende dessa qualidade para que as análises e projeções façam sentido.

---

## 7.6. Processo de validar a base do ERP

### O que significa validar uma base?

O ERP (*Enterprise Resource Planning*) é o sistema integrado que registra e organiza diferentes processos da empresa. No contexto financeiro, pode conter lançamentos contábeis, fornecedores, notas fiscais, centros de custo, pagamentos, compras e outras informações.

Uma base extraída do ERP não deve ser considerada automaticamente correta só porque veio do sistema. Ela pode estar incompleta, conter filtros inadequados, apresentar classificações incorretas ou ter sido extraída antes da conclusão do fechamento.

**Validar a base significa verificar se os dados estão completos, coerentes, corretamente classificados e reconciliados com as fontes oficiais antes de utilizá-los em relatórios e análises.**

### Exemplo prático

Imagine que você precise atualizar a planilha de despesas administrativas de setembro. Você extrai do ERP uma base com as seguintes informações:

| Conta | Centro de custo | Histórico | Valor |
|---|---|---|---:|
| 6101 | Marketing | Agência digital | R$ 15.000 |
| 6205 | Financeiro | Licença de software | R$ 4.000 |
| 6101 | Marketing | Agência digital | R$ 15.000 |
| 6302 | Administrativo | Material de escritório | R$ 2.500 |

O total extraído é de R$ 36.500. Porém, você percebe que duas linhas parecem representar a mesma despesa de R$ 15 mil.

É tentador excluir uma delas imediatamente. Mas esse seria um erro de procedimento: elas podem ser dois lançamentos legítimos ou duas linhas da mesma transação detalhada na extração.

A primeira tarefa é investigar se existe duplicidade real, conferindo identificadores do lançamento, documento fiscal, fornecedor, data, valor e histórico.

Depois, você deve validar o restante da base.

### Checklist de validação

- [ ] **Período correto:** a extração contém somente o mês e o intervalo de datas desejados?
- [ ] **Escopo completo:** foram incluídas todas as empresas, filiais, contas e centros de custo necessários?
- [ ] **Integridade dos dados:** existem linhas duplicadas, campos vazios, valores com formato incorreto ou registros inesperados?
- [ ] **Classificação:** as contas contábeis e os centros de custo estão mapeados corretamente para a visão gerencial?
- [ ] **Conciliação de valores:** os totais batem com o relatório de controle ou com o balancete oficial do mesmo período e escopo?
- [ ] **Versão da base:** a extração corresponde à versão validada do fechamento, e não a uma base preliminar?
- [ ] **Rastreabilidade:** consigo localizar a origem de cada valor e explicar eventuais diferenças?

### Outro exemplo: erro de classificação

Imagine que a conta contábil de uma despesa com software esteja associada ao centro de custo de Marketing, mas o orçamento prevê esse gasto no Financeiro.

Ao comparar o realizado com o orçamento, Marketing parecerá ter gasto mais do que deveria e Financeiro parecerá ter gasto menos.

O total da companhia pode estar correto, mas a análise por departamento estará distorcida.

Nesse caso, é preciso conferir o documento, o responsável pelo serviço e as regras de classificação. Se houver um erro, a correção deve ser tratada com a área responsável, conforme o procedimento interno.

Não se deve mudar o centro de custo apenas para eliminar uma variação orçamentária.

### Como validar tecnicamente no Excel?

- **SOMASES:** consolidar despesas por conta, centro de custo e mês.
- **CONT.SES:** identificar possíveis duplicidades usando combinações de campos.
- **PROCV:** buscar a descrição de contas ou centros de custo em uma tabela de referência.
- **Tabela dinâmica:** comparar totais por departamento, conta e período.
- **Power Query:** padronizar formatos, combinar arquivos e automatizar etapas repetitivas.

Um controle adicional é comparar o total da base com o total do relatório oficial do ERP ou do balancete, respeitando exatamente o mesmo período, as mesmas entidades, a mesma moeda e o mesmo escopo.

Se houver diferença, você deve procurar a causa antes de utilizar os números.

**Aprendizado principal:** uma análise financeira só é confiável quando a base de dados é confiável. A validação evita que erros de extração, classificação ou consolidação sejam reproduzidos em dashboards e apresentações.

---

## 7.7. Balancete x Base do ERP

Esse é um dos pontos mais importantes para quem está começando em FP&A.

### Primeiro, entenda a diferença

O **balancete** é um relatório contábil que apresenta os saldos das contas contábeis em determinado período, geralmente com saldos anteriores, movimentações de débito e crédito e saldos finais, conforme o modelo do relatório.

Já a **base do ERP** é um conjunto de registros extraídos do sistema. Pode conter lançamentos detalhados, documentos, centros de custo, fornecedores, datas, valores e outras dimensões analíticas.

Portanto, não são necessariamente dois relatórios equivalentes. Uma base do ERP pode conter os lançamentos que alimentam os saldos do balancete, mas também pode incluir informações operacionais que não aparecem diretamente nele.

| Fonte | O que mostra | Pergunta principal |
|---|---|---|
| **Balancete** | Visão contábil consolidada por conta, com saldos e movimentações do período. | Os saldos contábeis estão corretos e conciliados? |
| **Base detalhada do ERP** | Registros que permitem investigar documentos, lançamentos, datas, departamentos e outras dimensões. | Quais registros explicam o saldo e como eles estão classificados? |

### Exemplo numérico: despesas administrativas

Imagine que o balancete de setembro apresente um saldo de R$ 100 mil na conta contábil de despesas administrativas, considerando o mesmo critério de movimentação e o mesmo escopo da análise.

Você extrai a base do ERP e consolida os lançamentos que deveriam compor essa conta. O resultado da planilha é R$ 96 mil.

Existe uma diferença de R$ 4 mil.

| Verificação | Valor |
|---|---:|
| Saldo conforme balancete | R$ 100.000 |
| Total conforme base extraída | R$ 96.000 |
| **Diferença a investigar** | **R$ 4.000** |

Não significa automaticamente que a Contabilidade errou ou que a base do ERP está errada. Significa que a conciliação ainda não está explicada.

Você precisa investigar, por exemplo:

- A base foi extraída com todas as contas necessárias?
- O período está correto?
- Há lançamentos feitos diretamente na contabilidade que não aparecem no relatório operacional?
- Existem ajustes manuais ou reclassificações?
- A base contempla todas as empresas e filiais?
- O balancete mostra o saldo acumulado, enquanto a base mostra apenas a movimentação do mês?
- Foram utilizados os mesmos critérios de sinal, moeda e classificação?

Essa última questão é especialmente importante: saldo contábil, saldo acumulado e movimentação mensal não são necessariamente a mesma coisa.

### Como fazer a conciliação corretamente

1. **Defina o escopo:** mês, empresa, contas contábeis, centros de custo e tipo de saldo que será comparado.
2. **Extraia as fontes oficiais:** balancete e base detalhada do ERP, preferencialmente após a validação do fechamento.
3. **Padronize as informações:** códigos de conta, datas, sinais dos valores e demais campos utilizados na comparação.
4. **Consolide a base:** some os lançamentos por conta e, quando necessário, por centro de custo ou outra dimensão.
5. **Compare os totais:** identifique quais contas apresentam diferenças e priorize as materialmente relevantes.
6. **Investigue e documente:** procure os registros que explicam cada diferença, registre a causa e encaminhe eventuais ajustes ao responsável.

### O que é materialidade nessa rotina?

Materialidade é a importância de uma diferença para a análise ou para a decisão. Um desvio de R$ 50 pode não exigir a mesma investigação que um desvio de R$ 50 mil, dependendo do porte da empresa, da natureza da conta e dos critérios internos de controle.

Porém, valor pequeno não significa que uma diferença possa ser ignorada automaticamente. Um erro recorrente, uma classificação inadequada ou um problema de integridade pode ser relevante mesmo quando o valor individual é baixo.

O profissional deve seguir os limites e os procedimentos definidos pela empresa, sem inventar um limite de tolerância por conta própria.

### Uma observação contábil importante

O fato de o balancete estar correto não garante, por si só, que todas as dimensões gerenciais estejam corretas. Uma despesa pode estar registrada na conta contábil certa, mas vinculada ao centro de custo errado.

Da mesma forma, uma base operacional pode estar correta para determinada finalidade e não conter todos os registros necessários para reconciliar o balancete.

Por isso, a conciliação precisa considerar a finalidade de cada fonte, a abrangência do relatório e as regras de contabilização e classificação.

**Aprendizado principal:** o balancete ajuda a validar os saldos contábeis; a base do ERP ajuda a entender a composição desses saldos. A conciliação conecta as duas visões e permite utilizar os dados com segurança no FP&A.

---

## 7.8. Como todos esses conceitos se conectam no dia a dia

Para fixar o aprendizado, imagine um único ciclo mensal de FP&A em uma empresa como o Grupo Technos.

1. **Closing:** a Contabilidade conclui o fechamento e valida os registros do período.
2. **Validação das bases:** o time confere a extração do ERP e concilia os totais com o balancete.
3. **Atualização da P&L:** o realizado é organizado nas linhas gerenciais de receitas, custos e despesas.
4. **Análise de variações:** o realizado é comparado com Budget, Forecast e ano anterior.
5. **Book de resultados:** os números e suas explicações são organizados para apoiar decisões da liderança.
6. **Revisão do Forecast:** os resultados e as novas informações são usados para revisar as projeções dos meses futuros.

Esse ciclo é recorrente: o fechamento fornece os números efetivos; a análise mostra o que mudou; e o forecast utiliza essas informações para atualizar a expectativa de resultado.


---
# 8. Estrutura mental para qualquer KPI

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

# 9. Fontes de dados que quero conhecer melhor

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

# 10. Modelo de análise que quero aplicar

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





