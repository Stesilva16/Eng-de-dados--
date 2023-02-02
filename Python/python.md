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

· Extração

o Arquivo consolidado

Observação: o arquivo original deve sempre estar disponível

o Dado extraído

· Transformação

o Limpeza de inconsistências (normalização)

o Verificação de registros duplicados

o Verificação dos tipos de registros

o Filtros, inserções, etc.

· Carregamento





PRÉ-ANÁLISE



Importando Pandas

![image-20230201185158615](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185158615.png)

Importando base de dados (“Data frame”)

o Necessário atribuir uma base de dados a uma variável, doravante chamada de dataframe (df)

![image-20230201185221244](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185221244.png)

Esse comando abre o arquivo, o lê e o transporta para a memória RAM (não modifica a base de dados original)

o No método “.read_extensão” é essencial apontar tipo de arquivo

o Entre parêntesis está uma string com o caminho da base de dados

§ Se o arquivo estivesse no computador, deveria ser passado o endereço interno

o O comando “sep =” indica os separadores de dados, os quais nos arquivos CSV costumam ser vírgulas (se nenhum separador for indicado, o Pandas entende que a base utiliza vírgulas)

o Enconding diz respeito à codificação da base de dados

§ Pandas é multicodificação (consegue ler diferentes codificações)

§ Se nenhuma codificação for atribuída, opta-se por padrão por UTF-8

§ Se não souber, utilizar a biblioteca chardet

o Obs: preferir utilizar a variável “df” no lugar de “dataframe”

Definir tipos das colunas ao importar dados (especialmente colunas que contenham data)

![image-20230201185257081](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185257081.png)

Comando “parse_tipo = [‘nome_coluna’]” é utilizado para modificar o tipo dos dados da coluna no momento da apresentação

· Nesse caso, modificou-se uma coluna com datas, para que seu tipo seja de datas, seguindo padrão internacional (AAAA,MM,DD)



Realizar backup do dataframe

· Fazer um backup, antes de começar a normalizar os dados, é essencial

![image-20230201185317910](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185317910.png)

· Fazer backup de uma coluna somente

![image-20230201185334405](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185334405.png)

o Esse comando criará uma nova coluna na tabela, que servirá como backup (no caso, ‘cidade_backup’)

o Depois, se quiser eliminar a coluna, basta eliminá-la

![image-20230201185352991](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185352991.png)

Configurando opções do Pandas

· Comandos para determinar máximo de colunas e linhas que serão exibidas

![image-20230201185413469](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185413469.png)

Exibindo dataframe

· Para exibir o dataframe, basta chamar a variável

![image-20230201185431824](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185431824.png)

· Método “.head()” exibe primeiras linhas

o Deve ser passado o número de linhas (se não for, por padrão exibem-se 5

![image-20230201185452414](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185452414.png)

· Método “.df.tail()” exibe últimas linhas

o Deve ser passado o número de linhas (se não for, por padrão exibem-se 5)

![image-20230201185513477](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185513477.png)

· Mostrar tipos de dados contidos em colunas

![image-20230201185532213](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185532213.png)

o Observação: quando uma coluna apresenta tipos misturados (i.e. colunas contendo strings e números), o Pandas entende que ela contém “objetos”



Verificação do número de linhas e colunas no dataframe

![image-20230201185549828](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185549828.png)

Verificação mais completa das colunas (nomes, tipos de dados e quantidade de entradas (não nulos))

![image-20230201185607887](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185607887.png)



TRATAMENTO DE DADOS



Tornar coluna index

· Index determinado pelo Pandas deixará de existir

· Importante para localizar logs ou ids mais rapidamente

· Para tornar os valores de uma coluna index, esses devem ser únicos

o É possível perguntar para o Pandas se os valores são únicos



![image-20230201185620310](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185620310.png)

· Transformando a coluna em novo rótulo

![image-20230201185649379](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185649379.png)

 Obs: por esse método, a tabela perde sua ordenação

Dropar colunas (eliminar





· Repare que, no comando, é passada uma lista contendo as colunas que se pretende dropar

· Após a lista, é designado o eixo em que será dropado (se coluna ou linha)

o Pode-se utilizar “columns” ou “rows” , bem como 1 (colunas) ou 0 (linhas)

· Comando “inplace” designa se alteração deve ou não ser aplicada ao dataframe

o Por padrão está como False (resultado será somente um preview da tabela)

![image-20230201185728818](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185728818.png)



Renomear colunas

· Para isso, utiliza-se o método “.rename(columns={‘nome_coluna_modificada’: ‘novo_nome’})”

· Atenção: esse comando pode ser utilizado para renomear linhas

· Preferir nomes de coluna em caixa baixa e sem caracteres especiais (também não deve haver espaço vazio)

![image-20230201185754340](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185754340.png)

Concatenar colunas

· Ambas as colunas devem apresentar dados do mesmo tipo

· No exemplo, iremos concatenar as colunas ‘dia’(DateTime) e ‘horario’(string)

o Necessário, primeiro, converter dados da coluna ‘dia’ para string

![image-20230201185815162](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185815162.png)



· Repare que foi criada uma nova coluna (‘data’)

o As colunas originais não foram deletadas

*Mudar posição das colunas*

Necessário esquematizar novamente todo o dataframe (transforma-se o dataframe inteiro, criando um novo ou sobrescrevendo o original)

![image-20230201185856827](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185856827.png)



Repare que é necessário passar uma lista com o nome das colunas dentro de outra lista (comando do Pandas)

*Verificar se, em uma coluna, existem valores repetidos (ou se são todos únicos)*

![image-20230201185934569](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201185934569.png)

*Código para perceber strings em coluna onde deveriam constar somente números (mesmo que no formato string)*

![image-20230201190002742](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190002742.png)

Limpar dados

· Para saber quais são os elementos únicos dentro de uma coluna, utiliza-se o método “pd.unique(nome_dataframe[‘nome_coluna’])”

o Pandas analisa todas as tuplas e retorna uma lista com todos os elementos

![image-20230201190025468](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190025468.png)

Ordenando consulta alfabeticamente:

![image-20230201190051249](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190051249.png)

Para anular inconsistências, utiliza-se o método “.replace([‘valor1’, valor2, ...] , pd.NA)

![image-20230201190111223](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190111223.png)

o Nesse caso, os campos com inconsistências passarão a conter valores nulos (NA do Pandas)



Para alterar valores contidos em um dataframe, utilizar o método “.replace[‘valor1’, valor2, ...] , [‘novo_valor’])

Frisando: primeira lista contém valores que serão modificados, enquanto a segunda, o valor substituto (somente um)

![image-20230201190715734](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190715734.png)

![image-20230201190727176](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190727176.png)

· Método replace em cima de colunas específicas:

![image-20230201190745644](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190745644.png)

Repare que após a seleção do dataframe, é delimitado a coluna por um ponto

Para fazer correções específicas em dataframes, utiliza-se o método “df.loc[]”

![image-20230201190816199](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190816199.png)

Nesse caso, o campo ‘cidade’ (que é uma coluna), na linha 0, passará a ser “SANTOS”



· Também é possível utilizar filtros para corrigir todos as incorrências em uma coluna

o Primeiro, cria-se um filtro, para selecionar todas as incorrências erradas

![image-20230201190843769](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190843769.png)

§ Repare que o nome Santos foi grafado equivocadamente, com um “m”

§ O filtro seleciona todas as incorrências “SAMTOS” dentro da coluna “localizacao” dentro do dataframe “df”

Depois, atribui-se um novo valor a essas incorrências

![image-20230201190906546](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190906546.png)

§ Repare que é passado uma lista com o filtro e a coluna que será alterada

§ Como se está atribuindo diretamente um valor para o objeto (por meio de um sinal de igual), não é necessário confirmar a modificação com “inplace = True”

*Corrigir dígitos específicos dentro de uma string*

![image-20230201190936237](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201190936237.png)

· Argumento “regex” permite com que se corrija dígitos dentro de uma string (se não utilizasse esse atributo, a substituição só ocorreria se houvesse uma string exatamente igual a “O”)

· Nesse caso, trocou-se o caractere “O” por “0” (zero), erro comum em dataframes

Transformar dado em nulo, sem mudar tipo da coluna

· Utilizar NaN (da biblioteca NumPy)

![image-20230201191002196](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191002196.png)

o Repare que np.NaN é um método da biblioteca NumPy

**Mudar tipo de coluna**

![image-20230201191043453](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191043453.png)



· Nesse caso, mudou-se do tipo Object para Float64

· Observação: método só funciona se os valores forem compatíveis

VISUALIZAÇÃO DO DATAFRAME

**Mostrar colunas específicas de um dataframe**

![image-20230201191132985](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191132985.png)

· Repare que é necessário criar uma lista sobre uma lista

Selecionar células completas

· Para consultar células inteiras, utilizar o método “.loc[número_célula]”

![image-20230201191155917](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191155917.png)



 Repare que todas as colunas são retornadas

· Para localizar um intervalo de células:

![image-20230201191218414](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191218414.png)



Novamente, todas as colunas são retornadas



Selecionar todos os valores de uma coluna específica

![image-20230201191238048](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191238048.png)

Visualizar maior e menor valor dentro de uma coluna (que contenha números)

· Maior valor

![image-20230201191253975](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191253975.png)

Visualizar média dos valores dentro de uma coluna (que contenha números)

![image-20230201191327870](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191327870.png)

![image-20230201191340722](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191340722.png)

Consultar quantas células possuem valores nulos (NA – Not Available)

![image-20230201191412704](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191412704.png)

![image-20230201191426859](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191426859.png)

FILTROS

· Para filtrar uma tabela, é necessário criar um filtro e localizar a partir desse filtro

![image-20230201191907442](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191907442.png)

Criando novo dataframe a partir de um filtro

![image-20230201191950366](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201191950366.png)



· Nesse caso, criou-se um novo dataframe contendo somente os registros em que o “UF” corresponde a “SP”



Filtros compostos

· É possível filtrar uma tabela por mais de um critério

· Para isso, devem ser criados diferentes filtros, os quais deverão ser chamados pelo parâmetro nome_dataframe.loc[filtro1 & filtro2 & filtro3...]

![image-20230201192013835](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192013835.png)

![image-20230201192028112](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192028112.png)

![image-20230201192059398](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192059398.png)



![image-20230201192115707](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192115707.png)

![image-20230201192131644](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192131644.png)

![image-20230201192149459](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192149459.png)

![image-20230201192203631](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192203631.png)

![image-20230201192229709](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192229709.png)

![image-20230201192319866](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192319866.png)

![image-20230201192344907](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192344907.png)

![image-20230201192359128](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192359128.png)

VALIDAÇÃO DE DADOS

· Necessário utilizar a biblioteca Pandera

· Deve-se validar os dados de uma tabela ao menos duas vezes:

Após dropar as tabelas que não serão utilizadas, renomear as utilizadas e corrigir erros muito evidentes

 Antes da última verificação geral

Criação do Schema

![image-20230201192429449](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192429449.png)

![image-20230201192758199](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192758199.png)

· Se depois de rodar o schema aparecer o dataframe, não há inconsistência



RELACIONANDO TABELAS COM PANDAS

· Só é possível relacionar as tabelas que possuírem uma coluna com as mesmas informações (i.e. “id”, “número_ocorrência”)

o O nome da coluna deve ser igual também

· Escolher quem será o dataframe de base (da esquerda)

· Realizar o merge

![image-20230201192833982](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192833982.png)

![image-20230201192849080](C:\Users\stefa\AppData\Roaming\Typora\typora-user-images\image-20230201192849080.png)

