<h1>Spark</h1>



<h2>O que é Spark?</h2>

Apache Spark é uma plataforma de processamento de dados de alta velocidade e de grande escala. É projetado para fornecer processamento distribuído e escalável de grandes conjuntos de dados.

PySpark é uma biblioteca do Apache Spark que fornece acesso ao Spark através da linguagem de programação Python. PySpark torna mais fácil para os cientistas de dados trabalharem com grandes quantidades de dados em um cluster distribuído, sem a necessidade de codificar em linguagens como Scala ou Java.

O Spark é amplamente utilizado na área de dados para tarefas como análise de dados em grande escala, processamento de stream, machine learning e muito mais. Ele oferece suporte a diversas fontes de dados, como bancos de dados relacionais, arquivos, sistemas NoSQL e muito mais. Além disso, ele fornece uma ampla gama de bibliotecas de machine learning, como MLlib, para ajudar os cientistas de dados a construir modelos e fazer previsões.

<h3>Pontos relevantes</h3>

1. Processamento em larga escala: Spark é capaz de processar grandes quantidades de dados, tornando-o ideal para aplicativos de análise de dados em larga escala.
2. Distribuição de cluster: Spark permite a distribuição de cálculos em um cluster de nós, o que aumenta a escalabilidade e desempenho.
3. Integração com outras ferramentas: Spark é compatível com uma ampla gama de tecnologias e ferramentas, incluindo Hadoop, Hive, HBase, Cassandra, e muito mais.
4. API de programação: Spark tem uma API de programação fácil de usar, incluindo APIs para Scala, Python, Java e R, tornando-o acessível a uma ampla gama de desenvolvedores.
5. Resilient Distributed Datasets (RDD): Spark usa RDDs para representar conjuntos de dados distribuídos, que são imutáveis e particionados. Este modelo permite a execução de operações paralelas eficientes sobre grandes quantidades de dados.
6. Streaming: Spark fornece suporte nativo ao processamento de fluxo de dados em tempo real, o que permite a análise em tempo real de dados em fluxo.
7. Machine Learning: Spark tem suporte integrado ao aprendizado de máquina, incluindo algoritmos de aprendizado supervisionado e não supervisionado, como regressão linear, k-means e random forests.

<h3>Comandos</h3>

1. read: Lê dados de uma fonte, como arquivos, banco de dados, ou outra fonte.
2. show: Mostra os dados lidos na forma de uma tabela.
3. select: Seleciona as colunas específicas de um DataFrame.
4. filter: Filtra linhas de um DataFrame de acordo com uma expressão lógica.
5. groupBy: Agrupa as linhas de um DataFrame por uma ou mais colunas.
6. aggregate: Aplica uma agregação aos dados agrupados, como soma, média, etc.
7. join: Junta dois DataFrames baseados em colunas comuns.
8. write: Escreve os dados para uma fonte, como arquivos, banco de dados, ou outra fonte.
9. repartition: Redistribui os dados em um DataFrame para melhorar o desempenho.

<h3>Pyspark</h3>

 Apache Spark é uma ferramenta de processamento de dados (somente isso)

 Tecnologia desenvolvida em Scala

Para rodar, necessário ter o JVM instalado

 Ainda assim, não é necessário trabalhar com ele por Scala ou Java – também é possível trabalhar com Spark com SQL, Python (pela biblioteca PySpark) e R

 Os códigos, nas diferentes linguagens, serão convertidos para um formato próprio, chamado RDD – depois serão processados em cluster pela Spark Engine

O Apache Spark foi desenvolvido para processar dados massivos em cluster

 Obs: o Spark não possui uma ferramenta de gerenciamento de cluster – necessário utilizar outras ferramentas com o Yarn (gerenciador de cluster do Radoop), Mesos e Kubernets

· Possível trabalhar tanto com SQL quanto com dataframes

· Os dados idealmente serão provenientes de um data lake, uma vez que o Spark não possui uma ferramenta de armazenamento

PYSPARK NA PRÁTICA

· A máquina do Google Colab, por padrão, possui o Apache Spark já instalado, necessitando somente instalar a biblioteca PySpark, para poder manuseá-lo com Python

<h4>PySpark:</h4>

Instalação da biblioteca PySpark:

!pip install pyspark

Criação de uma sessão para executar comandos do PySpark:

from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("ETL_with_PySpark").getOrCreate()

Importação de funções do PySpark:

from pyspark.sql.functions import lit, col

Aplicar filtros:

df = df.filter(col("coluna1") > 10)
Método .withColumn():

df = df.withColumn("coluna_nova", lit("valor_literal"))

Right join:

df_right_join = df_esquerda.join(df_direita, on="coluna_comum", how="right")

Esses são apenas exemplos básicos, e a complexidade dos comandos pode aumentar dependendo da quantidade e tipo de dados que você precisa manipular. É importante ler a documentação do PySpark e dos métodos específicos para entender suas funcionalidades e como usá-los corretamente.

TIPOS BÁSICOS DE DADOS DO SPARK

Tipos básicos

· ByteType -- Int

· ShortType -- Int

· IntegerType -- Int

· LongType -- Int

· FloatType -- Float

· DoubleType -- Float

· StringType -- String

· BooleanType -- Bool

· DecimalType -- Float

· NULL Para mais informações: https://spark.apache.org/docs/latest/sql-ref-datatypes.html

Tipos complexos

· TimestampType – DateTime

· DateType – DateTime

· ArrayType – Lista, tupla, array

· MapType – Dict

· StructType – Lista, tupla

· StructField – Tipo de campo

STRUCT TYPES

· Definir os tipos das colunas, ao invés de solicitar ao Spark que infira o schema

Os dados inseridos que não forem do tipo determinado entrarão como nulos (o que pode ser interessante para se procurar inconsistências nas linhas – funcionando como uma espécie de validação)
