<h1>Python</h1>



<h2>O que é Python?</h2>

Python é uma linguagem de programação de alto nível, com sintaxe clara e fácil de aprender, que é amplamente utilizada para desenvolvimento web, análise de dados, inteligência artificial, entre outras aplicações. As principais razões para usar Python incluem sua flexibilidade, facilidade de uso, ampla comunidade de desenvolvedores e ampla disponibilidade de bibliotecas e ferramentas.

Para usar Python, é necessário baixar e instalar o interpretador Python e um ambiente de desenvolvimento integrado (IDE) opcional, como o PyCharm ou o Jupyter Notebook. Depois disso, você pode escrever e executar códigos Python em um terminal ou em uma janela de código em seu IDE.

Um engenheiro de dados usa Python para processar, analisar e visualizar grandes quantidades de dados, além de treinar modelos de aprendizado de máquina e automatizar tarefas repetitivas. Bibliotecas como Pandas, Numpy e Matplotlib são frequentemente utilizadas para realizar tarefas de análise de dados, enquanto bibliotecas como TensorFlow e PyTorch são usadas para treinar modelos de aprendizado de máquina.

<h3>Pontos relevantes e comandos</h3>

1. Bibliotecas de análise de dados: Python tem uma ampla gama de bibliotecas como NumPy, Pandas, Matplotlib, Seaborn, entre outras, que tornam o processo de análise de dados mais fácil e eficiente.
2. Integração com outras tecnologias: Python é compatível com muitas outras tecnologias como SQL, Hadoop, Spark e NoSQL, tornando-o uma escolha popular para a integração de sistemas.
3. Linguagem de fácil aprendizado: Python é conhecido por sua sintaxe fácil e intuitiva, tornando-o uma linguagem popular para aprendizado inicial em programação e análise de dados.

Alguns dos comandos básicos do Python incluem:

1. Variáveis: Criação e atribuição de valores a variáveis, por exemplo: x = 5.
2. Operadores: Usados para realizar operações matemáticas e de comparação, por exemplo: +, -, *, /, ==, !=, <,>, >=, <=.
3. Condicionais: Usados para executar ações com base em determinadas condições, por exemplo: if, elif, else.
4. Loops: Usados para repetir ações várias vezes, por exemplo: for, while.
5. Funções: Permitem encapsular trechos de código para serem reutilizados, por exemplo: def, return.
6. Bibliotecas: Importação e uso de bibliotecas em seu código, por exemplo: import, as.

<h3>Biblioteca Pandas</h3>

Pandas é uma biblioteca de análise de dados em Python que fornece estruturas de dados rápidas, flexíveis e fáceis de usar para análise e manipulação de dados. Alguns dos principais comandos do Pandas incluem:

1. read_csv() - para ler arquivos CSV e convertê-los em dataframes do Pandas
2. head() - para visualizar as primeiras linhas de um dataframe
3. tail() - para visualizar as últimas linhas de um dataframe
4. shape - para obter as dimensões de um dataframe
5. describe() - para obter uma descrição estatística resumida dos dados
6. info() - para obter informações sobre as colunas de um dataframe, incluindo tipo de dados, quantidade de dados não nulos e memória usada
7. drop() - para remover linhas ou colunas de um dataframe
8. rename() - para renomear colunas em um dataframe
9. groupby() - para agrupar dados em um dataframe com base em uma ou mais colunas
10. pivot_table() - para criar uma tabela dinâmica a partir de dados agrupados.

<h4>Fases do ETL</h4>

Os comandos para realizar o ETL (Extract, Transform, Load) com Python dependem das bibliotecas e fontes de dados que você está usando. Aqui estão alguns exemplos gerais:

*Extraction:*

Ler dados de um arquivo CSV:


import pandas as pd
df = pd.read_csv("nome_do_arquivo.csv")

Ler dados de um banco de dados SQL:

import pandas as pd
import sqlite3
conn = sqlite3.connect("nome_do_banco.db")
df = pd.read_sql_query("SELECT * FROM nome_da_tabela", conn)

*Transform:*
Renomear colunas:

df = df.rename(columns={"coluna_antiga": "coluna_nova"})

Remover duplicatas:

df = df.drop_duplicates()

Tratar valores ausentes:

df = df.fillna(0) # Preenche valores ausentes com 0

*Load:*

Gravar dados em um arquivo CSV:

df.to_csv("nome_do_arquivo_destino.csv", index=False)

Gravar dados em um banco de dados SQL:

df.to_sql("nome_da_tabela_destino", conn, if_exists="replace")

Esses são apenas exemplos gerais, e a complexidade dos comandos pode aumentar dependendo da quantidade e tipo de dados que você precisa manipular. Além disso, existem outras bibliotecas e ferramentas úteis para o ETL com Python, como o SQLAlchemy, o PySpark, etc.


<h4>Observações para extração</h4>

Importar a biblioteca Pandas para o ambiente
Importar o banco de dados em um data frame (df) usando o método read_extension
Especificar o separador usado no banco de dados e a codificação (UTF-8 é o padrão)
Definir os tipos de dados das colunas durante a importação (especialmente para colunas de data)
Criar uma cópia de segurança do data frame ou de uma única coluna antes de iniciar a normalização de dados
Configurar as opções do Pandas para determinar o número de linhas e colunas exibidas
Exibir o data frame usando o nome da variável ou usando o método head (mostra as primeiras 5 linhas por padrão)





