# Payroll Evolution (Evolução do Emprego EUA)

> **Pipeline de Engenharia de Dados do *Nonfarm Payrolls* (NFP) dos EUA, executado no Azure Databricks com Unity Catalog e entrega final otimizada para Power BI.**

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Stack](https://img.shields.io/badge/Stack-Azure%20Databricks%20|%20PySpark%20|%20DeltaLake%20|%20PowerBI-blue)

---

## 🖼️ Visão Geral do Dashboard

<img width="930" height="626" alt="Image" src="https://github.com/user-attachments/assets/68bad7ac-6129-428d-bff5-e1cc89991427" />

---

## ☁️ Prova do Ambiente — Azure Databricks + Unity Catalog

Este print valida a execução real no ambiente Azure Databricks, mostrando:

- domínio *.azuredatabricks.net*  
- catálogo governado `payroll`  
- armazenamento no ADLS Gen2  
- configuração Unity Catalog (metastore + storage root)

<img width="1394" height="631" alt="Image" src="https://github.com/user-attachments/assets/39205097-9830-492c-b143-d842e94522cc" />

---

## 💼 O Problema de Negócio

O *Nonfarm Payrolls (NFP)* é um dos indicadores mais relevantes da economia americana  
e do mercado financeiro. A série histórica é utilizada para:

1. 📉 compreender ciclos econômicos  
2. 📈 antecipar decisões de política monetária  
3. 💹 criar estratégias macro e quantitativas  

O desafio: **criar um pipeline confiável e governado**, capaz de entregar uma camada Gold certificada para uso em BI e análises temporais.

---

## 🏗️ A Solução Técnica (Lakehouse no Azure)

A arquitetura foi construída utilizando o **Azure Databricks**, com governança completa pelo **Unity Catalog**, seguindo o padrão **Medalhão**.

### **Arquitetura do Pipeline**

#### 🔶 Bronze — Ingestão Bruta
- Coleta da API oficial do **Bureau of Labor Statistics (BLS)**  
- Armazenamento em Delta Lake (sem transformação)

#### 🔷 Silver — Limpeza e Padronização
- Conversão e padronização de datas  
- Tipagem correta dos atributos  
- Tratamento da série temporal  
- Particionamento por ano

#### 🟡 Gold — Modelo Analítico para BI
- Criação da tabela `ft_payroll_evolucao_eua`  
- Ordenação temporal garantida (`ano_mes_chave`)  
- Otimização com Delta Engine  

---

## 💡 Insights & Conclusões

### 📌 Choque Econômico de 2020
A queda abrupta no Payroll devido à pandemia é claramente evidenciada na linha temporal, seguida pela recuperação em ondas subsequentes.

### 📌 Camada Gold Certificada
A tabela final é:

- 🔒 Governada  
- 🧹 Limpa  
- ⚡ Otimizada  
- 📊 Ideal para Power BI (DirectQuery ou Import)  

---

## 💻 Tech Stack

- **Cloud:** Azure Databricks  
- **Storage:** Delta Lake + ADLS Gen2  
- **Governança:** Unity Catalog  
- **Linguagens:** Python (PySpark), SQL  
- **Visualização:** Power BI  
- **Arquitetura:** Lakehouse (Bronze → Silver → Gold)  

---

## 🏁 Conclusão

Este projeto demonstra a implementação de um pipeline moderno e governado em **Azure Databricks**, aplicando boas práticas de engenharia de dados, Delta Lake, Unity Catalog e Arquitetura Medalhão.

O resultado final é um dataset confiável, versionado e otimizado — pronto para análises estratégicas no Power BI.

---

## 🚀 Extensões Futuras

- Previsão de Payroll com modelos de séries temporais  
- Data Quality com Expectation Constraints  
- Orquestração com Databricks Workflows  
- Publicação da Gold como Delta Live Table  





