# 🚀 Projeto: Imersão Databricks — Jornada de Dados  

Este repositório reúne as atividades práticas que desenvolvi durante a Imersão Databricks promovida pela Jornada de Dados, com foco em engenharia de dados moderna usando Databricks, Spark, Delta Lake e a arquitetura Lakehouse.


<p align="center">
  <img src="https://img.shields.io/badge/Databricks-%23FF3621.svg?style=for-the-badge&logo=databricks&logoColor=white" alt="Databricks"/>
  <img src="https://img.shields.io/badge/Apache_Spark-%23E25A1C.svg?style=for-the-badge&logo=apachespark&logoColor=white" alt="Apache Spark"/>
  <img src="https://img.shields.io/badge/Delta_Lake-%23007ACC.svg?style=for-the-badge&logo=databricks&logoColor=white" alt="Delta Lake"/>
  <img src="https://img.shields.io/badge/Python-%233776AB.svg?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/SQL-%23007ACC.svg?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL"/>
  <img src="https://img.shields.io/badge/GitHub-%23181717.svg?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
</p>

---

## 🎯 Objetivo do Projeto

Aplicar na prática os conceitos aprendidos na imersão, construindo pipelines de dados completos (Raw → Bronze → Silver → Gold), com ingestão via APIs, transformações PySpark/SQL, modelagem Delta Lake e governança com Unity Catalog.

Durante o projeto, foram realizadas as seguintes etapas:
- Criação e configuração do ambiente Databricks Free Edition
- Integração com GitHub para versionamento e controle de código
- Ingestão de dados de APIs públicas (Bitcoin, Petróleo, Ouro, Prata)
- Criação de camadas Bronze, Silver e Gold seguindo o padrão Lakehouse
- Implementação de transformações, qualidade de dados e partições
- Construção de tabelas analíticas e KPIs
- Exploração de integração com Fivetran para ingestão de bancos relacionais
- Desenvolvimento de um Agente de IA consumindo dados da camada Gold

---

## 🧱 Arquitetura de Dados

O projeto segue o padrão **Medallion Architecture (Lakehouse)**, com as seguintes camadas:

```text
Fonte de Dados (APIs / Bancos)
        ↓
Camada Raw (Landing)
        ↓
Camada Bronze (Ingestão)
        ↓
Camada Silver (Refino e Padronização)
        ↓
Camada Gold (Curadoria e Consumo)
        ↓
Agente de IA / Visualização

```

Essa estrutura garante organização, qualidade, rastreabilidade e governança dos dados.

---

## 🗓️ Estrutura do Treinamento

### Aula 01: Ingestão e Lakehouse (Raw→Bronze)
- Ingerir dados de 2 APIs (Bitcoin e commodities) com scripts Python.
- Agendar execuções recorrentes (cron/Jobs) a cada 10 minutos.
- Persistir dados na camada **raw** e promover para **bronze** com DLT.
- Referência: `docs/AULA_01.md`.

### Aula 02: KPIs e Modelagem (Silver→Gold)
- Definir KPIs e métricas de negócio a partir da bronze.
- Criar camadas **Silver** (refino e padronização) e **Gold** (curadoria e consumo).
- Implementar transformações SQL/PySpark, qualidade de dados e partições.
- Gerar tabelas agregadas para visualização e consumo analítico.

### Aula 03: Agente de Inteligência Artificial
- Construir um agente de IA que consome dados da **Gold**.
- Expor consultas/insights com linguagem natural (LLM) e prompts guiados.
- Integrar o agente ao pipeline (monitoramento básico e tracing).

---

## 🧩 Tecnologias e Ferramentas Utilizadas

| Categoria               | Ferramenta / Tecnologia      |
| ----------------------- | ---------------------------- |
| Plataforma              | Databricks Free Edition |
| Engine de Processamento | Apache Spark                 |
| Armazenamento           | Delta Lake                   |
| Governança              | Unity Catalog                |
| Linguagens              | Python, SQL                  |
| Orquestração            | Databricks Jobs / Cron       |
| Versionamento           | Git e GitHub                 |
| Ingestão                | Fivetran                     |
| Armazenamento simulado  | Amazon S3                    |

---

## ⚙️ Pré-Requisitos

* Conta gratuita no [Databricks Free Edition](https://www.databricks.com/learn/free-edition)
* Conta no [GitHub](https://github.com)
* Conta no [Fivetran](https://www.fivetran.com/) para ingestão de bancos

---

## 🗓️ Estrutura do Projeto

| Etapa                               | Descrição                                                                                       | Arquivo                                 |
| ----------------------------------- | ----------------------------------------------------------------------------------------------- | --------------------------------------- |
| 01 - Ingestão (Raw → Bronze)        | Coleta de dados de APIs públicas (Bitcoin, Ouro, Petróleo, Prata) e armazenamento no Lakehouse. | `notebooks/aula01_ingestao.ipynb`       |
| 02 - Transformações (Silver → Gold) | Limpeza, padronização, cálculo de métricas e criação de KPIs.                                   | `notebooks/aula02_transformacoes.ipynb` |
| 03 - Agente de IA                   | Consulta e análise dos dados da camada Gold via modelo LLM.                                     | `notebooks/aula03_agente_ia.ipynb`      |


---

## 🧠 Habilidades Desenvolvidas

- Criação e automação de pipelines de dados com Apache Spark
- Aplicação da arquitetura Lakehouse (Bronze, Silver, Gold)
- Utilização do Delta Lake com controle de versões e ACID transactions
- Criação de scripts Python para ingestão de APIs
- Transformações analíticas em PySpark e SQL
- Integração com GitHub para versionamento de código
- Aplicação de boas práticas de governança de dados via Unity Catalog
- Construção de um Agente de IA para consulta em linguagem natural

---

## 🏁 Resultados

✅ Pipelines funcionais integrados ao Databricks

✅ Dados ingeridos e processados em camadas estruturadas

✅ KPIs e tabelas analíticas prontas para consumo

✅ Integração com agente de IA para insights automatizados

---

## 👨‍💻 Autor

[Antony Fernando Ferreira](https://linkedin.com/in/antonyfferreira) 

---

## 🧾 Créditos

Treinamento original desenvolvido por [Luciano Vasconcelos](https://linkedin.com/in/lucianovasconcelos) e equipe da [Jornada de Dados](https://youtube.com/@jornadadedados)

---

> “A engenharia de dados moderna começa quando você entende que o dado é o seu produto.”
> — Jornada de Dados