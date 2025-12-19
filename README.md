# MVP- ENG de Dados

📡 Data Warehouse – Telefonia Móvel 4G e 5G no Brasil

📌 Visão Geral
Este projeto implementa um Data Warehouse multidimensional para análise da cobertura da telefonia móvel 4G e 5G nos municípios brasileiros, integrando dados de presença de infraestrutura e Qualidade de Experiência (QoE).
A solução foi construída na Google Cloud Platform, utilizando BigQuery para processamento analítico.
________________________________________
🎯 Objetivos
•	Avaliar a distribuição territorial da cobertura 4G e 5G
•	Comparar a capilaridade das operadoras
•	Analisar a qualidade da experiência (QoE) entregue aos usuários
•	Identificar lacunas de cobertura, especialmente para o 5G
________________________________________
🗂️ Fontes de Dados
•	Cobertura de municípios por operadora e tecnologia
•	Dados consolidados de QoE (velocidade de download, número de testes)
•	Métricas demográficas por Unidade Federativa (população, área, densidade)
Os dados são públicos, armazenados em CSV no Google Cloud Storage e acessados via External Tables no BigQuery.
________________________________________
🏗️ Arquitetura
O pipeline segue o padrão Bronze–Silver–Gold:
BRONZE  →  CSVs no GCS (dados brutos)
SILVER  →  Dados limpos e padronizados (curated)
GOLD    →  Data Warehouse + Views Analíticas
________________________________________
🧩 Modelagem
•	Esquema Estrela
•	Dimensões: Tempo, Operadora, Tecnologia, Localidade, UF Métricas
•	Fatos: Presença da cobertura e QoE
•	Uso exclusivo de chaves naturais (PK/FK)
________________________________________
📊 Análises Implementadas
•	Ranking de UFs por cobertura 4G e 5G
•	Cobertura por operadora (Brasil)
•	Evolução temporal da cobertura
•	QoE por operadora e tecnologia
•	Dispersão entre velocidade média e volume de testes
•	Municípios com menor presença de 5G
________________________________________
🛠️ Tecnologias
•	Google Cloud Storage
•	BigQuery
•	BigQuery Studio Notebooks
•	SQL (Standard SQL)
________________________________________
📌 Observação
O projeto tem caráter acadêmico e analítico, podendo ser estendido com novos indicadores, fontes socioeconômicas e análises preditivas.


