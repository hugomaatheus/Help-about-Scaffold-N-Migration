-Scaffold-

Scaffold, é um tipo de generator que pode ser utilizado na criação de um conjunto completo de models, database migration para este model, controllers para manipulá-los, views para exibir e manipular os dados e um conjunto de testes para cada item acima.

Vamos configurar um simples recurso chamado “Usuario” (passando também seus atributos “nome:string”, “email:string”) para melhor exemplificar:

![scaffold](https://github.com/hugomaatheus/Help-about-Scaffold-N-Migration/blob/master/image/cap1.png)

O generator gera models, controllers, layouts, helpers, testes funcionais e unitários, stylesheets, cria também as views, e database migration para “Usuario” e cria route para o recurso.

-Migrations-

Após utilizar o scaffold precisaremos realizar uma migration para criar as tabelas dos models no database. Migrations são uma maneira fácil e rápida de fazer alterações no seu database schema utilizando Ruby DSL, então você não precisa escrever SQL “na mão”.
Cada database schema começa “vazio”, então você pode pensar que cada migration como uma nova versão do seu database. Cada migration modifica para adicionar/remover tabelas, colunas ou entradas. Vamos visualizar a migration gerada através do scaffold para o recurso “Usuario”:

![migration1](https://github.com/hugomaatheus/Help-about-Scaffold-N-Migration/blob/master/image/cap2.png)

Agora que temos nossa migration criada, iremos rodar para realizar as alterações no database com o comando rails db:migrate.

![migration2](https://github.com/hugomaatheus/Help-about-Scaffold-N-Migration/blob/master/image/cap3.png)

Essa migration adiciona uma tabela chamada usuarios com uma coluna string nome e outra email, uma chave primária será adicionada implicitamente. A linha t.timestamps da migration irá adicionar duas colunas created_at e updated_at, que são automaticamente atualizadas pelo Active Record.

Tabela gerada no database pela migration.

![migration3](https://github.com/hugomaatheus/Help-about-Scaffold-N-Migration/blob/master/image/cap4.png)

