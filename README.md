# Projeto OLAP - Análise de Dados Ambulatoriais de Pernambuco

Este projeto visa criar um Data Mart com dados ambulatoriais do estado de Pernambuco, utilizando o método de Ralph Kimball (Bottom-Up) e esquema Star Schema, para melhorar a gestão da saúde pública. Utilizamos dados extraídos do DATASUS, realizando transformações e carga de dados para análises OLAP.

## Estrutura do Projeto

O projeto é composto pelas seguintes dimensões e tabela fato:

### Dimensões:
- **dim_tempo**: Informações relacionadas ao tempo (mês, ano, trimestre, semestre, descricao_mes).
- **dim_paciente**: Detalhes dos pacientes (idade, sexo, raça/cor, faixa etária).
- **dim_local**: Dados do local de atendimento (código e nome do município).
- **dim_procedimento**: Informações sobre o procedimento realizado (descrição, categorias e sub-categorias CID).

### Tabela Fato:
- **fato_atendimento**: Registra as relações entre tempo, local, paciente e procedimento, além da quantidade de procedimentos realizados.

## Processo ETL

1. **Extração**: Os dados são extraídos do DATASUS com foco na região de Pernambuco.
2. **Transformação**: Limpeza e padronização dos dados, incluindo a exclusão de registros nulos.
3. **Carga**: Os dados transformados são carregados no Data Mart, prontos para análise OLAP.

## Objetivo do Projeto

O projeto tem como principal objetivo apoiar gestores de saúde estaduais, profissionais da saúde nos municípios, gestores de políticas públicas e analistas, fornecendo dados para decisões estratégicas e identificação de tendências relacionadas à saúde ambulatorial no estado de Pernambuco.

## Utilização

A aplicação OLAP permite a exploração dos dados carregados no Data Mart, gerando relatórios e métricas que podem ser utilizadas para:

- Tomada de decisões estratégicas na gestão de saúde pública.
- Identificação de padrões e tendências no atendimento ambulatorial.
- Suporte a análises detalhadas por município, idade, raça, sexo e outros fatores.

## Ferramentas Utilizadas

- **PostgreSQL**: Para o armazenamento e manipulação dos dados.
- **Pentaho**: Para a criação do processo ETL e desenvolvimento de relatórios e análises OLAP.
