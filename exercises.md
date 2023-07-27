# Course description:

Curso Ruby e Ruby on Rails codeminers42 do Fábio Makima.

## Pelos números

#### Nível de experiência: Todos os níveis

#### Idiomas: Português

#### Aulas: Jun/Ago 2023

#### Presencial: Todos os sábados.

# AULA 07/15/2023

1. Explique o que é o Ruby on Rails.

2. Quais são os componentes do modelo MVC, descreva o papel de cada um no RoR.

3. Qual a filosofia do RoR quanto à organização de código dos models e controllers?

4. Cite quais os elementos e explique o fluxo de acesso do usuário em um aplicação RoR.

5. Explique o que é o Convention over Configuration e no que consiste ao que concerne a convenção de nomenclatura.

6. Como fazer para criar models em um arquivo vazio?

7. Escreva a sintaxe dos seguintes operações do CRUD:

   a) Criar um novo registro usando o metodo create;

   b) = usando o método new;

   c) retornar todos os valores de uma coleção;

   d) retornar o primeiro, último ou valor da coleção em qualquer posição;

   e) retornar buscando por um valor específico;

   f) encontrar todos os resultados com um valor específico e ordenando por um campo específico em ordem decrescente;

   g) buscar, modificar salvar o objeto no banco;

   h) usando o método específico para mudanças;

   i) buscar e destruir um objeto;

   j) encontrar e deletar todas as entradas com um campo com valor específico;

   k) deletar todos os objetos de uma coleção;

   l) salvar fazendo validações com e sem retorno de erro.

8. O que são migrations?

9. O que são associações? Como fazer para estabelecer reuniões de tabelas e fazer com que ao deletar uma, todos sejam deletados.

10. Qual a sintaxe para criação de um objeto já com um relacionamento estabelecido?

11. Quais são os tipos de associações do RoR?

# DESAFIO

## Introdução ao Rails - Peeper

Uma famosa plataforma de microblogging tem passado por maus bocados depois de uma recente aquisição. Os mais pessimistas preveêm que ela não sobreviverá por muito tempo e o seu cliente, contanto com isso, contratou você para desenvolver a nova plataforma que irá tomar o seu lugar: o Peeper.

## Modelos

### User

##### Campos

- handle: O nome que os usuários usam para referenciar uns aos outros dentro da plataforma. É obrigatório, deve conter entre 4 e 12 caracteres, não pode se repetir e não pode conter espaços, acentos ou caracteres especiais, apenas letras, números e underscore (\_).
- display_name: O nome de exibição do usuário. É obrigatório, deve conter no máximo 30 caracteres e pode conter qualquer caractere.
- bio: Texto livre de até 300 caracteres. É opcional.
- born_at: Data de nascimento do usuário. É obrigatório. O usuário precisa ter pelo menos 13 (anos) para criar a conta.

## Associações

- um usuário pode ter vários status.
- um usuário pode seguir outros usuários.

## Requisitos extra

- O usuário deve ser capaz de fazer upload de uma imagem para representar a sua conta.

## Status

#####Campos

- body: é o corpo da postagem. Texto livre de até 300 caracteres (mais que a concorrência!), obrigatório.

### Associações

- um status pertence a um usuário.
- um status pode ser em resposta a outro status.
- um status pode ter entre 0 e 4 mídias.

## Media

#####Campos

- type: Define se a mídia é uma imagem ou um vídeo. É um campo inteiro, obrigatório.
- url: a URL que aponta para a mídia em questão.

### Associações

uma mídia pertence a um status.

## Requisitos extra

- O usuários deve ser capaz de fazer upload da imagem ou vídeo da mídia.

## Requisitos

- Podem usar o SQLite como banco de dados.
- Não usem scaffold.
- Não há necessidade de criar views nesse momento.
- Todos os models devem possuir testes unitários usando RSpec.
- Façam commits organizados.

# AULA 07/22/2023

1. O que é o Rails Router e qual o seu papel no framework?

2. O que é o Controller e qual o seu papel?

3. Quais as convenções de nome do controller?

4. Como criar um controller em um documento em branco?

5. Explique qual o fluxo de uso de um controller em uma aplicação rails.

6. Explique quais são os três tipos possíveis de parâmetros em uma aplicação RoR.

7. O que são Strong Parameters? Como eles são definidos em uma aplicação rails?

8. O que é o render e quais as opções de render? Explique cada uma delas.

9. Qual a função do helper redirect_to?

10. O que faz o helper head?

11. Em que consiste o HTML e ERB? Qual a sua notação?

12. Como acessar uma variável do controller a partir da view?

13. Qual a diferença de papeis entre o Action Controller e a ActionView?

14. Qual o papel do url helper e como utilizá-lo? Qual a sintaxe dos 3 tipos?

15. Explique:

a) form_for

b) fields_for

16. O que é um asset pipeline? Qual a sua utilidade?

## DESAFIO

 Desenvolvimento web com Rails - Peeper
Já tendo a aplicação Rails com os modelos bem estruturados da nossa plataforma de microblogging Peeper, agora é necessário criar as views e controllers para ser possível finalmente visualizar a plataforma!

## Timeline
O mais importante para o microblog agora é ter um feed, onde seja possível visualizar todos os status que já foram postados e também adiconar novos status. Assim, a plataforma se tornará funcional.

### Views

#### Index (localhost:3000/status)
- Esta página é o feed, ou seja, uma lista de todos os status.
- No topo da página é necessário ter um botão para adicionar um status novo. Este botão rediretiona para a página `new`.
- Os dados do status que serão mostrados no feed são: `display_name` do user autor do status e o `body` do status (mas apenas os primeiros 50 caracteres).
- Para cada status existem ter 3 ações: responder, visualizar e deletar.
- Ao responder um status, redirecionar para a página `new`. Importante lembrar que é necessário ter a informação de qual status está sendo respodido para a criação do novo status, eles terão que estar associados.
- Ao visualizar um status, redirecionar para a página `show`.
- Ao cliar o botão para deletar um status, este status será apagado do banco de dados.

#### New (localhost:3000/status/new)
- Nesta página é necessário um formulário com os seguintes campos:
  - Campo select para selecionar o user que é o autor deste status.
  - Campo text para escrever o `body`.
  - Campo para adicionar uma mídia.
  - Botão "save" para salvar o novo status.

#### Show (localhost:3000/status/1)
- Esta é a página de detalhes do status.
- É necessário visualizar todos os campos do status (inclusive as mídias).
- Por fim, dois botões ao final da página: "back" (que volta para a página `index`) e "edit" (que redireciona para a página de editar o status).

#### Edit (localhost:3000/status/1/edit)
- Esta é a página de edição.
- Ela é igual a página de criação de um novo status, mas com o formulário já preenchido. Dica: é possível utilizar uma view compartilhada (partial).
- Ao final da página, o botão "save" para salvar as edições que foram feitas.

### Controller

- Criar a StatusController.
- Criar todos os métodos necessários para as actions que foram citadas acima.

### Rotas

- No arquivo `routes.rb` criar as rotas necessárias **sem o uso de resources**. 

## Requisitos

- Como citado acima, não usar resources quando forem criar as rotas.
- Criar testes de requisição.
- Façam commits organizados.

