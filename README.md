# US Economy Monitor: Análise do Payroll & Pipeline Governança

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Stack](https://img.shields.io/badge/Stack-Azure%20Databricks%20|%20Unity%20Catalog%20|%20PowerBI-blue)

> **"Como a maior economia do mundo se recuperou pós-2020?"**

Este projeto não é apenas um pipeline de dados; é um **Monitor Econômico** focado no *Nonfarm Payrolls (NFP)*, um dos indicadores mais críticos para tomada de decisão no mercado financeiro global.

O objetivo foi construir uma solução analítica robusta, onde a **Engenharia de Dados (Azure Databricks)** serve para garantir a **Qualidade e Governança (Unity Catalog)** da informação que chega ao dashboard.

---

## 📊 Visão do Analista (Dashboard)

O produto final é um painel que permite visualizar os ciclos econômicos e a volatilidade da criação de empregos nos EUA.

<img width="930" height="626" alt="Dashboard Power BI Payroll" src="https://github.com/user-attachments/assets/68bad7ac-6129-428d-bff5-e1cc89991427" />

---

## 🛡️ Governança e Qualidade (O Diferencial)

Para um Analista de Dados, a confiança na fonte é tudo. Por isso, este projeto utiliza o **Unity Catalog** no Azure. Isso garante que cada número no Power BI seja auditável e venha de uma fonte "Silver/Gold" certificada.

**Evidência do Ambiente (Azure + Unity Catalog):**
<img width="1394" height="631" alt="Ambiente Databricks Unity Catalog" src="https://github.com/user-attachments/assets/39205097-9830-492c-b143-d842e94522cc" />

---

## 🛠 Arquitetura da Solução (Data Lineage)

Utilizei a arquitetura **Medalhão (Medallion Architecture)** para transformar dados brutos em inteligência de negócio:

### 1. Coleta e Ingestão (Camada Bronze)
* Conexão direta com a API do **Bureau of Labor Statistics (BLS)** via Python.
* Objetivo: Automatizar a busca do dado para não depender de downloads manuais.

### 2. Tratamento e Limpeza (Camada Silver)
* Normalização de datas e tipagem de dados (Casting).
* **Data Quality:** Garantia de que não existem registros duplicados ou nulos que distorçam a análise macroeconômica.

### 3. Modelagem para BI (Camada Gold)
* Criação da tabela fato `ft_payroll_evolucao_eua`.
* Otimização para leitura rápida no **Power BI**.

---

## 💼 Por que isso importa para o Negócio?

O *Nonfarm Payrolls* move mercados. Ter um pipeline próprio permite:
1.  **Independência:** Não depender de relatórios de terceiros.
2.  **Histórico:** Capacidade de analisar tendências de longo prazo (pré e pós-pandemia).
3.  **Agilidade:** O dado sai na API e atualiza o dashboard automaticamente.

---

## 💻 Tech Stack
* **Análise & Viz:** Power BI, DAX.
* **Engenharia & Governança:** Azure Databricks, Unity Catalog, Delta Lake.
* **Linguagem:** Python (PySpark) e SQL.
