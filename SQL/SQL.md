<h1>SQL</h1>



<h2>O que é o SQL?</h2>

SQL (Structured Query Language) é uma linguagem de programação utilizada para gerenciar bancos de dados relacionais. É usada para criar, consultar, atualizar e excluir dados em uma base de dados.

Como usar:

1. Criar tabelas: Definição da estrutura da tabela e colunas, incluindo tipos de dados, restrições, etc.
2. Inserir dados: Adição de registros a uma tabela
3. Consultar dados: Recuperação de dados de uma ou mais tabelas com base em critérios específicos
4. Atualizar dados: Modificação de dados existentes em uma tabela
5. Excluir dados: Remoção de dados de uma tabela

Para que serve: SQL é usado para gerenciar bancos de dados relacionais, permitindo aos usuários manipular dados de forma eficiente. Ele fornece uma interface para interagir com bancos de dados e realizar operações como inserir, atualizar, excluir e consultar dados.

Como é usado na área de dados: SQL é amplamente utilizado na área de dados para gerenciar grandes quantidades de informações em bancos de dados. Ele é utilizado para extrair insights e informações valiosas dos dados, por exemplo, para análise de dados em empresas, ciência de dados, etc. Além disso, SQL é frequentemente utilizado como uma ferramenta para garantir a integridade dos dados, incluindo a aplicação de restrições e regras de negócio.

<h3>Pontos relevantes</h3>

Tabelas particionadas em BigQuery:

- Divisão de uma tabela em segmentos menores, chamados partições, para melhorar o desempenho da consulta e controlar custos
- Criação de tabela particionada especificando o critério de particionamento
- Adição de opções para definir a expiração da partição

Consultas:

- Consulta sem filtros para retornar um pedido

- Partições ajudam a reduzir o número de bytes lidos por uma consulta

- Exemplo de consulta para calcular a média de precipitação de uma estação meteorológica.

- Consulta utiliza a função AVG() para calcular a média, agrupa os resultados por estação, data, mês, idade da partição, etc.

  <h3>Comandos</h3>

  Os principais comandos do MySQL incluem:

  1. SELECT - utilizado para selecionar dados de uma tabela
  2. INSERT - utilizado para inserir dados em uma tabela
  3. UPDATE - utilizado para atualizar dados em uma tabela
  4. DELETE - utilizado para excluir dados de uma tabela
  5. CREATE - utilizado para criar uma tabela, índice, banco de dados, etc.
  6. ALTER - utilizado para modificar uma tabela existente
  7. DROP - utilizado para excluir uma tabela, índice, banco de dados, etc.
  8. WHERE - utilizado para especificar condições na seleção, atualização e exclusão de dados
  9. LIMIT - utilizado para limitar o número de linhas retornadas em uma consulta
  10. GROUP BY - utilizado para agrupar dados por uma ou mais colunas
  11. JOIN - utilizado para unir duas ou mais tabelas com base em uma coluna em comum.