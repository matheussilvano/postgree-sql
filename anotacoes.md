# Conteúdos
- Conceitos básicos sobre banco de dados
- Postgresql
- Banco de dados de Pedidos (básico ao avançado)
- Tópicos especiais
- Álgebra relacional
- Projeto de banco de dados

# Conceitos básicos
- Pode estar presente em qualquer lugar independente do uso de tecnologia
- Exemplos
  - Caderno
  - Lista Telefônica
  - Agenda
- Com base em dados é possível gerar diversos relatórios
- Banco de Dados pode ser definido como "uma coleção de dados persistentes usada pelos sistemas de informação de uma determinada empresa"
- Qualquer empresa precisa manter muitos dados sobre suas operações
- Em resumo, é um conjunto de várias tabelas, onde cada tabela guarda um conjunto de dados
- Operações que podem ser realizadas em um banco de dados:
  - Inserir
  - Buscar
  - Excluir
  - Alterar
- Permite que os usuários busquem e atualizem os dados quando necessários
- Um sistema de banco de dados envolve principalmente quatro componentes:
 - Dados
   - É o que está armazenado no banco de dados
   - Precisam ser integrados
   - São compartilhados
   - Precisam ser persistentes
 - Hardware
   - É a máquina/computador/servidor em que o sistema de banco de dados irá funcionar
   - Volumes de armazenamento
   - Dispositivos de entrada e saída
   - Processador
   - Memória
 - Software
   - Entre o banco de dados físico e os usuários existe uma camada de software conhecida como gerenciador ou servidor de banco de dados
   - É mais conhecido como Sistema Gerenciador de Banco de Dados (SGBD)
   - No curso, será usado o PostgreSQL
   - Realiza o tratamento das requisições (inclusão, alteração, consulta e exclusão)
   - Isola os usuários dos detalhes do nível de hardware
 - Usuários
   - Programadores de aplicações (liguagem de programação)
   - Usuários Finais
   - Administrador de dados
   - Administrador de banco de dados (DBA - Database administrator)
- O acesso ao banco de dados pode ser realizado pela linguagem SQL (Structured Query Language)
- Foi desenvolvida nos anos 1970
- É a linguagem padrão para trabalhar com bases dados relacionais
- O código criado em SQL é o mesmo utilizado em outros SGBDs
- DDL: É a linguagem SQL de definição de dados
- DML: É a linguagemm SQL para manipulação de dados
- Link dos materiais do Curso: https://drive.google.com/drive/folders/12sDuhZTNDzS3BgfqCiLgAyccNlOAYj-n?usp=sharing

# Tabelas e consultas
- Base de dados de pedidos
   - Clientes, fornecedores, municípios, pedidos
- Criação de tabelas
- Inserção de dados
- Chaves primárias e estrangeiras
- Consultas básicas e avançadas
  - Agrupamentos, junções(joins), subconsultas
- View, campos autoincremento, índices
- Mais de 180 exercícios
- Avaliação prática com 50 questões

## Tabelas de clientes
- Clicar com o botão direito na database > Query tool
- Criar tabela:
```
create table nometabela (
  idcliente integer not null,
  nome varchar(50) not null,
  cpf char(11),
  rg varchar(15),
  data_nascimento date,
  genero char(1),
  profissao varchar(30),
  nacionalidade varchar(30),
  logradouro varchar(30),
  numero varchar(10),
  complemento varchar(30),
  bairro varchar(30),
  municipio varchar(30),
  uf varchar(30),
  observacoes text,

  constraint pk_cln_idcliente primary key (idcliente)
)
```
- Legenda:
  - integer: número inteiro
  - varchar: até (n) caracteres
  - char: exatamente (n) caracteres
  - not null: preenchimento obrigatório
  - Constraint: Restrição
  - pk: Primary key

- As colunas ficam salvas em: Databeses > NomeDoDatabase > Schemas > Public > Tables > nometabela > Columns
- As constraints ficam salvas em: Databeses > NomeDoDatabase > Schemas > Public > Tables > nometabela > Constraints