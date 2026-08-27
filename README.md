# 🧱 Databricks — Ambiente Oficial do Curso

[← Voltar ao Portfólio de Engenharia de Dados](https://github.com/joycequoos/Data_Enginer/blob/main/README.md)

Repositório de apoio para o curso oficial de **Databricks**, reunindo notebooks, exemplos práticos e anotações sobre a criação e manipulação do ambiente Lakehouse: Catalogs, Schemas, Volumes, DataFrames, Delta Lake e tabelas.

---

## 📑 Sumário

- [Sobre o Projeto](#-sobre-o-projeto)
- [Estrutura do Ambiente](#1-estrutura-do-ambiente-catalog-schema-e-volume)
- [Importando Arquivos para Volumes](#2-importando-arquivos-para-volumes)
- [Manipulando DataFrames no Databricks](#3-manipulando-dataframes-no-databricks)
- [Dados Públicos para Treino](#4-dados-públicos-para-treino)
- [Criando Tabelas](#5-criando-tabelas)
- [Notebooks do Repositório](#-notebooks-do-repositório)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)

---

## 📌 Sobre o Projeto

Este repositório documenta, passo a passo, a configuração de um ambiente oficial do Databricks para fins de estudo, cobrindo desde a criação da estrutura de dados (Catalog → Schema → Volume) até a criação de tabelas Delta, leitura/escrita de arquivos e manipulação de DataFrames via **PySpark** e **SQL**.

### O que é Lakehouse?

O **Lakehouse** é uma arquitetura de dados que une o melhor de dois mundos:

- O **baixo custo e a flexibilidade** de um Data Lake (armazenamento de qualquer tipo de dado — estruturado, semiestruturado ou não estruturado — em larga escala e a baixo custo);
- Com a **confiabilidade, governança e performance** de um Data Warehouse (transações ACID, schema enforcement, indexação e consultas SQL otimizadas).

Na prática, isso é possível graças ao **Delta Lake**, camada que adiciona um log de transações sobre arquivos Parquet, permitindo que o mesmo repositório de dados seja usado tanto para engenharia de dados e Machine Learning quanto para BI e relatórios — sem a necessidade de duplicar dados entre um Data Lake e um Data Warehouse separados.

O Databricks é a plataforma que implementa essa arquitetura, unificando em um único ambiente o armazenamento, o processamento (via Apache Spark) e o consumo dos dados.

---

## 1. Estrutura do Ambiente: Catalog, Schema e Volume

Primeiro passo do curso: criar a hierarquia de organização de dados no Unity Catalog.

| Etapa | Objeto criado |
|-------|----------------|
| 1 | Catalog: `curso_databricks` |
| 2 | Schema: `curso_databricks.aula` |
| 3 | Volume: `curso_databricks.aula.aula_volume` |

📓 Notebook: [`01.Criando Schema e Volume.py`](./01.Criando%20Schema%20e%20Volume.py)

---

## 2. Importando Arquivos para Volumes

Como carregar arquivos diretamente para dentro de um Volume do Databricks.

- Seleção e arraste (drag-and-drop) de arquivos direto para o Volume.
- Verificação dos Volumes criados na interface do Catalog.

📓 Notebook: [`01.Primeiros comandos.py`](./01.Primeiros%20comandos.py)

Nessa etapa também são explorados:

- Execução de comandos `dbutils` (utilitários do Databricks para manipulação de arquivos e segredos).
- Uso do comando `display()` para visualização amigável dos dados.
- Navegação em diretórios (ex.: pasta *Bike Store*).
- Leitura direta de arquivos a partir do diretório.
- Uso do modo `display` para inspeção dos dados carregados.

---

## 3. Manipulando DataFrames no Databricks

Um **DataFrame** no Databricks é uma estrutura de dados bidimensional e distribuída, organizada em colunas nomeadas e tipadas — semelhante a uma tabela relacional ou a uma planilha do Excel.

No ecossistema Databricks, construído sobre o **Apache Spark**, os DataFrames são a principal abstração para processamento de dados em larga escala (*Big Data*).

### Exemplo de uso (PySpark vs. SQL)

O mesmo DataFrame pode ser criado e consultado tanto em **Python (PySpark)** quanto em **SQL**, diretamente nos Notebooks — o que reforça a flexibilidade do ambiente para times com diferentes perfis técnicos.

- Criação e filtragem em **PySpark**.
- Consulta equivalente do mesmo DataFrame em **SQL**.
- Leitura de dados utilizando a arquitetura do **Spark**.

---

## 4. Dados Públicos para Treino

Fontes de dados públicos recomendadas para praticar os conceitos do curso:

- **Kaggle** — [kaggle.com](https://www.kaggle.com)
- **Datasets nativos do Databricks** — conjuntos de dados de exemplo disponibilizados pela própria plataforma, prontos para uso sem necessidade de upload manual.

Tópicos abordados:

- Onde encontrar e listar os datasets disponíveis.
- Leitura de um dataset de exemplo.
- Leitura de arquivos a partir de um Dataset nativo do Databricks.
- Leitura e escrita de arquivos em um diretório.

---

## 5. Criando Tabelas

📓 Notebook: [`02. Criando primeiras tabelas.py`](./02.%20Criando%20primeiras%20tabelas.py)

### Tratamento de Dados

Etapa de limpeza e preparação dos dados antes da criação das tabelas.

### 🔺 Delta Lake

O formato **Delta (Delta Lake)** é uma camada de armazenamento open source construída sobre arquivos **Parquet**.

> Em resumo: se o Parquet é um formato colunar altamente eficiente, o Delta é o Parquet combinado com um **Log de Transações em JSON** (`_delta_log`). É essa camada de log que transforma pastas de arquivos soltos na nuvem em **tabelas estruturadas, transacionais e inteligentes**.

Antes do Delta, os Data Lakes tradicionais sofriam com:

- Arquivos corrompidos por falhas de escrita;
- Leituras inconsistentes durante a chegada de novos dados;
- Incapacidade de atualizar ou deletar registros individuais.

O Delta Lake resolveu esses problemas e popularizou a arquitetura **Data Lakehouse**.

### Operações abordadas

- Leitura de tabelas via **SQL**.
- Criação e remoção (`DROP`) de Schemas.
- Remoção (`DROP`) de Tabelas.

---

## 📂 Notebooks do Repositório

| Notebook | Descrição |
|----------|-----------|
| [`01.Criando Schema e Volume.py`](./01.Criando%20Schema%20e%20Volume.py) | Criação do Catalog, Schema e Volume |
| [`01.Primeiros comandos.py`](./01.Primeiros%20comandos.py) | Primeiros comandos, `dbutils`, `display()` e leitura de arquivos |
| [`02. Criando primeiras tabelas.py`](./02.%20Criando%20primeiras%20tabelas.py) | Criação de tabelas, tratamento de dados e Delta Lake |

---

## 🛠️ Tecnologias Utilizadas

- **Databricks** (Unity Catalog, Volumes, Notebooks)
- **Apache Spark** / **PySpark**
- **SQL**
- **Delta Lake**
- **Kaggle Datasets**

---

## 👩‍💻 Autoria

Repositório mantido por [**joycequoos**](https://github.com/joycequoos) como material de apoio ao curso oficial de Databricks.
