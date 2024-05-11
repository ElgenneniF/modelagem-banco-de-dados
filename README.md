# modelagem-banco-de-dados

## Cardinalidade

A cardinalidade em um modelo de banco de dados descreve o número de entidades filhas que estão relacionadas a uma única entidade pai em uma relação. Existem três tipos principais de cardinalidade:

Um para Um (1:1): Cada entidade em uma tabela está associada a no máximo uma entidade na outra tabela e vice-versa.

Um para Muitos (1:N): Cada entidade em uma tabela pode estar associada a várias entidades na outra tabela, mas cada entidade nessa outra tabela está associada a no máximo uma entidade na primeira tabela.

Muitos para Muitos (N:N): Cada entidade em uma tabela pode estar associada a várias entidades na outra tabela e vice-versa.

## Chaves Primárias e Estrangeiras
As chaves primárias e estrangeiras são usadas para estabelecer e manter essas relações entre tabelas em um banco de dados relacional. Aqui está uma explicação de como elas são usadas no arquivo fornecido:

Chave Primária (Primary Key): Uma chave primária é uma coluna ou conjunto de colunas que identifica de forma exclusiva cada registro em uma tabela. Ela garante que não haja duplicatas e permite acesso rápido aos dados. No arquivo fornecido, a chave primária é identificada pela cláusula PRIMARY KEY.

Chave Estrangeira (Foreign Key): Uma chave estrangeira é uma coluna ou conjunto de colunas em uma tabela que estabelece uma relação com a chave primária de outra tabela. Ela cria um vínculo entre as duas tabelas e é usada para garantir a integridade referencial dos dados. No arquivo fornecido, as chaves estrangeiras são identificadas pela cláusula FOREIGN KEY, que especifica a relação entre as tabelas e as colunas envolvidas.

## Relações a imagem
Na imagem acima, várias tabelas são definidas juntamente com suas chaves primárias e estrangeiras. Aqui está um resumo das relações entre as tabelas:

game e group: A tabela game possui uma chave estrangeira group_id, que se relaciona com a chave primária id da tabela group. Isso sugere uma relação de um para muitos, onde um jogo pode pertencer a apenas um grupo, mas um grupo pode ter vários jogos.

group, tutor e student: As tabelas group, tutor e student têm relacionamentos entre si através das chaves estrangeiras student_id e tutor_id, que se relacionam com as chaves primárias id das respectivas tabelas. Isso indica que um grupo pode ter um tutor e vários alunos, e um aluno ou tutor pode pertencer a vários grupos.

message e user: A tabela message possui uma chave estrangeira user_id, que se relaciona com a chave primária id da tabela user. Isso sugere uma relação de um para muitos, onde um usuário pode enviar vários mensagens, mas cada mensagem pertence a apenas um usuário.

answer_question e user, question: A tabela answer_question possui chaves estrangeiras student_id e question_id, que se relacionam com as chaves primárias id das tabelas user e question, respectivamente. Isso sugere uma relação onde um usuário pode responder várias questões, e cada questão pode ter várias respostas de usuários diferentes.
