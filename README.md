# dados
Normalização de dados é o processo formal e passo a passo que examina os atributos de uma entidade, com o objetivo de evitar anomalias observadas na inclusão, exclusão e alteração de registros.

O conceito de entidade é muito importante neste processo, ou seja, devemos identificar quais são as entidades que farão parte do projeto de banco de dados. Entidade é qualquer coisa, pessoa ou objeto que abstraído do mundo real torna-se uma tabela para armazenamento de dados. Normalmente usa-se o Modelo de Entidade e Relacionamento para criar o modelo do banco.
A regra de ouro que devemos observar no projeto de um banco de dados baseado no Modelo Relacional de Dados é a de "não misturar assuntos em uma mesma Tabela". Por exemplo: na Tabela Clientes devemos colocar somente campos relacionados com o assunto Clientes. Não devemos misturar campos relacionados com outros assuntos, tais como Pedidos, Produtos, etc. Essa "Mistura de Assuntos" em uma mesma tabela acaba por gerar repetição desnecessária dos dados bem como inconsistência dos dados.
Normalmente após a aplicação das regras de normalização de dados, algumas tabelas acabam sendo divididas em duas ou mais tabelas, o que no final gera um número maior de tabelas do que o originalmente previsto. Este processo causa a simplificação dos atributos de uma tabela, colaborando significativamente para a estabilidade do modelo de dados, reduzindo-se consideravelmente as necessidades de manutenção.
Os objetivos da normalização são muitos, entre eles destaco:

Minimização de redundâncias e inconsistências;
Facilidade de manipulações do banco de dados;
Ganho de performance no SGBD;
Facilidade de manutenção do sistema de Informação;
Entre outros.
As formas normais
O Processo de normalização aplica uma série de regras sobre as tabelas de um banco de dados, para verificar se estas estão corretamente projetadas. Embora existam cinco formas normais (ou regras de normalização), na prática usamos um conjunto de três Formas Normais.
Apesar de existir outras formas normais como a quarta forma normal e quinta forma normal, apenas as três primeiras tem sido considerada atualmente. As formas normais são importantes instrumentos para resolver antecipadamente problemas na estrutura do banco de dados.

Para aplicar a normalização de dados é necessário considerar a sequência das formas normais, isto é, para aplicar a segunda forma normal por exemplo, é necessário que seja aplicado a primeira forma normal. Da mesma forma, para aplicar a terceira forma normal é necessário que já tenha sido feita a normalização na segunda forma normal.

Primeira forma normal
Uma relação estará na primeira forma normal 1FN, se não houver grupo de dados repetidos, isto é, se todos os valores forem únicos. Em outras palavras podemos definir que a primeira forma normal não admite repetições ou campos que tenha mais que um valor.

Os procedimentos mais recomendados para aplicar a 1FN são os seguintes:

a) Identificar a chave primária da entidade;
b) Identificar o grupo repetitivo e removê-lo da entidade;
c) Criar uma nova entidade com a chave primária da entidade anterior e o grupo repetitivo.
A chave primária da nova entidade será obtida pela concatenação da chave primária da entidade inicial e a do grupo repetitivo.

Segunda forma normal
Uma tabela está na Segunda Forma Normal 2FN se ela estiver na 1FN e todos os atributos não chave forem totalmente dependentes da chave primária (dependente de toda a chave e não apenas de parte dela).

Se o nome do produto já existe na tabela produtos, então não é necessário que ele exista na tabela de produtos. A segunda forma normal trata destas anomalias e evita que valores fiquem em redundância no banco de dados.

Procedimentos:

a) Identificar os atributos que não são funcionalmente dependentes de toda a chave primária;
b) Remover da entidade todos esses atributos identificados e criar uma nova entidade com eles.
A chave primária da nova entidade será o atributo do qual os atributos do qual os atributos removidos são funcionalmente dependentes.

Terceira forma normal
Uma tabela está na Terceira Forma Normal 3FN se ela estiver na 2FN e se nenhuma coluna não-chave depender de outra coluna não-chave.

Na terceira forma normal temos de eliminar aqueles campos que podem ser obtidos pela equação de outros campos da mesma tabela.

Procedimentos:

a) Identificar todos os atributos que são funcionalmente dependentes de outros atributos não chave;
b) Removê-los.
A chave primária da nova entidade será o atributo do qual os atributos removidos são funcionalmente dependentes.
