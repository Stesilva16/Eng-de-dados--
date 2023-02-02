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

![image-20230201193415490](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193415490.png)



O Apache Spark foi desenvolvido para processar dados massivos em cluster

 Obs: o Spark não possui uma ferramenta de gerenciamento de cluster – necessário utilizar outras ferramentas com o Yarn (gerenciador de cluster do Radoop), Mesos e Kubernets

· Possível trabalhar tanto com SQL quanto com dataframes

· Os dados idealmente serão provenientes de um data lake, uma vez que o Spark não possui uma ferramenta de armazenamento

PYSPARK NA PRÁTICA

· A máquina do Google Colab, por padrão, possui o Apache Spark já instalado, necessitando somente instalar a biblioteca PySpark, para poder manuseá-lo com Python



· Instalação biblioteca PySpark

![image-20230201193347935](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193347935.png)

· Criar sessão para executar comandos do PySpark

![image-20230201193437400](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193437400.png)

· Importando funções do PySpark

![image-20230201193510106](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193510106.png)

![image-20230201193525515](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193525515.png)

![image-20230201193537332](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193537332.png)

![image-20230201193549692](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193549692.png)

![image-20230201193603314](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193603314.png)

![image-20230201193617820](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193617820.png)

![image-20230201193629650](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193629650.png)

![image-20230201193647792](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193647792.png)

![image-20230201193659943](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193659943.png)

![image-20230201193714268](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193714268.png)

![image-20230201193945700](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201193945700.png)

![image-20230201194001277](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194001277.png)

FILTROS

Outra forma de se aplicar filtros

![image-20230201194028434](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194028434.png)

![image-20230201194045859](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194045859.png)

![image-20230201194106247](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194106247.png)

![image-20230201194120253](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194120253.png)

· Observação: esse comando não criou novo dataframe, logo ele não é definitivo

· Método: .withColumn()

· Primeiro parâmetro é o nome da nova coluna

· Segundo parâmetro é função que determina os valores da coluna

o F.lit() permite passar um valor literal, uma string (todas as linhas possuirão mesmo valor literal nessa coluna)

![image-20230201194141207](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194141207.png)

![image-20230201194153359](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194153359.png)

![image-20230201194206959](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194206959.png)

![image-20230201194219728](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194219728.png)

![image-20230201194234162](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194234162.png)

![image-20230201194433632](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194433632.png)

![image-20230201194444426](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194444426.png)

![image-20230201194455005](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194455005.png)

![image-20230201194505481](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194505481.png)

![image-20230201194516904](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201194516904.png)

TRANSFORMAÇÃO DOS DADOS



· Separar string em substrings

![image-20230201195604928](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195604928.png)

![image-20230201195618330](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195618330.png)

![image-20230201195630641](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195630641.png)

![image-20230201195645751](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195645751.png)

![image-20230201195658312](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195658312.png)

![image-20230201195708740](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195708740.png)

![image-20230201195727755](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195727755.png)

![image-20230201195740363](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195740363.png)

![image-20230201195914718](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195914718.png)

![image-20230201195927903](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195927903.png)

![image-20230201195939290](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195939290.png)

![image-20230201195954529](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201195954529.png)

![image-20230201200007064](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200007064.png)

![image-20230201200019303](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200019303.png)

![image-20230201200033295](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200033295.png)

Right Join

· Considera todo conteúdo da tabela da direita importantes, devendo ser obrigatoriamente mostrados

· Right join faz com que registros que não possuem correspondência na tabela da esquerda apareçam com valores nulos

![image-20230201200055331](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200055331.png)

![image-20230201200137789](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200137789.png)

![image-20230201200202717](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200202717.png)

![image-20230201200218316](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200218316.png)

![image-20230201200237280](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200237280.png)

![image-20230201200252582](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200252582.png)

![image-20230201200308698](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201200308698.png)

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

o Os dados inseridos que não forem do tipo determinado entrarão como nulos (o que pode ser interessante para se procurar inconsistências nas linhas – funcionando como uma espécie de validação)