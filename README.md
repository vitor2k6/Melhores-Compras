# 📊 Análise de Dados de Vendas — Linha Petshop (2019–2022)

Projeto de **Análise Exploratória de Dados (EDA)** e **Estatística Aplicada** utilizando dados de vendas de uma rede de petshops entre **2019 e 2022**.

O objetivo do projeto é **identificar padrões de vendas, detectar anomalias nos dados e validar hipóteses estatísticas** relacionadas a preços, regiões e formas de pagamento.

A análise foi desenvolvida em **Python** utilizando **Google Colab**, com foco em **limpeza de dados, detecção de outliers, análise de correlação e testes estatísticos**.

---

# 🎯 Problema de Negócio

Empresas de varejo frequentemente enfrentam problemas como:

- **Registros inconsistentes de vendas**
- **Valores extremos que distorcem análises**
- **Dificuldade em identificar padrões de consumo**

Este projeto busca responder às seguintes perguntas:

- Existem **anomalias ou erros nos registros de vendas**?
- **Regiões diferentes possuem preços médios diferentes?**
- **A forma de pagamento influencia o ticket médio?**
- **Quais variáveis possuem maior relação com o lucro da empresa?**

Responder essas perguntas ajuda a empresa a:

- Melhorar a **qualidade dos dados**
- Identificar **possíveis erros operacionais**
- Entender **fatores que impactam o lucro**

---

# 📊 Dataset

O dataset contém registros de vendas da linha petshop entre **2019 e 2022**.

Arquivos utilizados:
vendas_linha_petshop_2019.csv
vendas_linha_petshop_2020.csv
vendas_linha_petshop_2021.csv
vendas_linha_petshop_2022.csv

### Principais variáveis analisadas

- `quantidade`
- `valor_unitario`
- `valor_total_bruto`
- `comissao`
- `lucro_liquido`
- `regiao`
- `forma_pagamento`

Essas variáveis permitem analisar **comportamento de vendas, rentabilidade e padrões comerciais**.

---

# 🧹 Tratamento e Preparação dos Dados

Antes da análise, foram realizadas etapas de **data cleaning**:

- Remoção de inconsistências
- Identificação de **outliers com Z-Score**
- Tratamento de valores extremos com **Winsorização**
- Padronização de variáveis numéricas

Critério utilizado para detectar outliers:
|Z-score| > 3

Para reduzir impacto de valores extremos foi aplicada **winsorização nos percentis 5% e 95%**.

---

# 📉 Visualizações Principais

Durante a análise foram utilizadas visualizações para identificar padrões e inconsistências:

### 📦 Boxplots
Utilizados para identificar **outliers nas variáveis de vendas**.

### 📊 Scatter Plot
Relação entre:

- `quantidade`
- `valor_total_bruto`

Essa visualização permitiu identificar **transações com valores extremamente altos para pequenas quantidades**.

### 🔗 Matriz de Correlação
Aplicação do **coeficiente de correlação de Pearson** para medir relações entre variáveis financeiras.

---

# 🧪 Testes Estatísticos

Foram realizados **Testes T de uma amostra** para verificar diferenças na média de preços.

### Comparações realizadas

**Por Região**

- Norte
- Nordeste
- Centro-Oeste
- Sudeste
- Sul

**Por Forma de Pagamento**

- Pix
- Cartão
- Boleto

Objetivo: verificar se existe **diferença estatisticamente significativa no ticket médio**.

---

# 📈 Principais Resultados

## 🔎 Detecção de Outliers

Foram identificados:

**4.762 outliers** na variável `quantidade`.

Observações relevantes:

- Quantidade máxima registrada: **110 unidades**
- Mediana de vendas: **1 unidade**

Também foram encontrados registros como:
valor_total_bruto > 3.000.000

em transações com **apenas 1 item**, indicando **possíveis erros de lançamento no sistema**.

---

## 🧪 Testes de Hipóteses

### Região

Não foram encontradas diferenças estatisticamente significativas entre regiões.

Valores de **p-value**:
0.87 – 0.99

Isso indica que **os preços médios são relativamente homogêneos entre regiões**.

---

### Forma de Pagamento

Também **não houve diferença significativa no ticket médio** entre:

- Pix
- Cartão
- Boleto

Ou seja, **o método de pagamento não influencia o valor médio das compras**.

---

# 🔗 Análise de Correlação

A única correlação forte identificada foi entre:

**Comissão e Lucro Líquido**

Coeficiente de Pearson:
r = 0.888694

Isso sugere que **estruturas de comissão estão fortemente associadas ao desempenho de lucro das vendas**.

---

# 💡 Insights Estratégicos

A análise permitiu identificar alguns pontos importantes:

✔ Existência de **inconsistências em registros de vendas**  
✔ Necessidade de **melhoria na validação de dados no sistema de vendas**  
✔ **Estrutura de preços consistente entre regiões**  
✔ **Forma de pagamento não impacta o ticket médio**  
✔ **Comissões estão fortemente associadas ao lucro da operação**

Esses insights podem ajudar a empresa a:

- Melhorar **governança de dados**
- Reduzir **erros operacionais**
- Ajustar **estratégias de incentivo comercial**

---

# 🛠 Tecnologias Utilizadas

- **Python 3.12**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **SciPy**
- **Pingouin**
- **Scikit-learn**
- **Google Colab**

---

# 🚀 Como Executar o Projeto

1️⃣ Clone o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git

2️⃣ Instale as dependências

pip install pandas numpy matplotlib seaborn scikit-learn scipy pingouin

3️⃣ Abra os notebooks no Jupyter Notebook ou Google Colab

4️⃣ Execute as células para reproduzir a análise.
