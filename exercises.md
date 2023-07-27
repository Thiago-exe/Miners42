# Course description:

Curso Ruby e Ruby on Rails codeminers42 do Fábio Makima.

## Pelos números

#### Nível de experiência: Todos os níveis

#### Idiomas: Português

#### Aulas: Jun/Ago 2023

#### Presencial: Todos os sábados.

## AULA 07/15/2023

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
