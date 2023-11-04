# Descrição

O Sistema de Informações sobre Nascidos Vivos (Sinasc), foi implantado oficialmente a partir de 1990, com o objetivo de coletar dados sobre os nascimentos informados em todo território nacional e fornecer dados sobre natalidade para todos os níveis do Sistema de Saúde. A implantação do Sinasc ocorreu de forma gradual em todas as unidades da Federação e já vem apresentando em muitos municípios, desde o ano de 1994, um número maior de registros do que o publicado pelo IBGE com base nos dados de Cartório de Registro Civil.

O nascimento é um dos eventos vitais e seu monitoramento pode contribuir para o conhecimento da situação de saúde de uma população e a avaliação de políticas e ações de vigilância e atenção à saúde na área da saúde materno-infantil.

# Objetivo

Mostrar um panorama do cenário obstétrico no Brasil no ano de 2022. 

# Ferramentas utilizadas

Escolhemos utilizar as seguintes ferramentas/linguagens para a análise:

* **Databricks / Spark**: ferramenta para processamento e manipulação de Big Data. O dataset completo tem mais de dois milhões de registros, por isso a escolha do databricks / spark.

* **SQL**: utilizamos SQL para análise e manipulação dos dados, por ser simples, de fácil entendimento e permite bastante maleabilidade. 

* **Big Query**: Banco de dados em nuvem no qual tenho familiaridade e créditos para uso gratuito da GCS por três meses. 

* **Power BI**: Ferramenta de dataviz que permite compartilhamento de dashboards/relatórios de forma gratuita, além de ser uma das mais utilizadas no mercado brasileiro atualmente. 


# Escolha dos dados

Utilizei os dados mais recentes disponíveis no site, ainda em sua versão preliminar:  
https://opendatasus.saude.gov.br/dataset/sistema-de-informacao-sobre-nascidos-vivos-sinasc


# Caminho dos dados

Baixamos a tabela do site do OpenDataSus e fizemos a leitura com o databricks. Fizemos a análise descritiva dos dados com SQL. Salvamos o arquivo em parquet. Fizemos a transferência dos dados para o GCS, salvando o arquivo em um bucket. Leitura do dataset em Big Query. No Big Query criamos uma external table e uma view para permitir o acesso aos dados direto com o Power BI. No PBI, importamos os dados para a criação dos gráficos e da apresentação.

# Entregáveis

Nesse repositório encontram-se os seguintes arquivos: 

* Dicionário dos dados do SINASC;

* Notebook databricks com o código de extração dos dados. 

* Notebook databricks com a transformação dos dados e análise descritiva inicial;

* Dashboard em PBI com análise final dos dados e conclusões. 

