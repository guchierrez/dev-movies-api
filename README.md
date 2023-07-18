<h1 align="center">
  <img alt="KenzieHub" title="KenzieHub" src="https://kenzie.com.br/_next/image?url=%2Fimages%2Flogo.png&w=640&q=75" width="100px" />
</h1>

<h1 align="center">
  Dev Movies - API
</h1>

<p align="center">
  <a href="#endpoints">Endpoints</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</p>

A API tem um total de 13 endpoints, sendo em volta principalmente do usuário (dev) - podendo cadastrar seu perfil, tecnologias que estuda e trabalhos realizados. <br/>

A url base da API é https://dev-movies-api.onrender.com/

## Rotas que não precisam de autenticação

<h2 align ='center'> Listagem de produtos </h2>

Nessa aplicação o usuário sem fazer login ou se cadastrar pode ver os filmes já cadastrados na plataforma, na API podemos acessar a lista dessa forma:

`GET /movies - FORMATO DA RESPOSTA - STATUS 200`

```json
[
    {
      "id": 1,
      "name": "The Random Heros",
      "type": "ficção",
      "duration": 120,
      "synopsis": "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores repellat.",
      "image": "https://res.cloudinary.com/dsbkp5841/image/upload/v1688390764/Rectangle_5_mgqd46.jpg"
    },
    {
      "id": 2,
      "name": "The Road",
      "type": "ficção",
      "duration": 90,
      "synopsis": "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores repellat.",
      "image": "https://res.cloudinary.com/dsbkp5841/image/upload/v1688390787/Rectangle_1_chtni6.jpg"
    },
    {
      "id": 3,
      "name": "The City Girls",
      "type": "comédia",
      "duration": 84,
      "synopsis": "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores repellat.",
      "image": "https://res.cloudinary.com/dsbkp5841/image/upload/v1688390817/Rectangle_2_cde9gm.jpg"
    },
    {
      "id": 4,
      "name": "The Indie Movie",
      "type": "drama",
      "duration": 132,
      "synopsis": "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores repellat.",
      "image": "https://res.cloudinary.com/dsbkp5841/image/upload/v1688390842/Rectangle_3_iwbv86.jpg"
    }
  ]
```

Acessar todos os filmes com as respectivas reviews:

`GET /movies?_embed=reviews - FORMATO DA RESPOSTA - STATUS 200`

```json
[
  {
    "id": 1,
    "name": "The Random Heros",
    "type": "ficção",
    "duration": 120,
    "synopsis": "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores repellat.",
    "image": "https://res.cloudinary.com/dsbkp5841/image/upload/v1688390764/Rectangle_5_mgqd46.jpg",
    "reviews": [
      {
        "id": 1,
        "movieId": 1,
        "userId": 1,
        "score": 8,
        "description": "Filme muitoooooo bom."
      },
      {
        "id": 2,
        "movieId": 1,
        "userId": 5,
        "score": 8,
        "description": "Filme massa.",
      }
    ]
  },
]  
```

Também é possível acessar um filme específico com suas respecitvas avaliações passando o id para rota:

`GET /movies/:id?_embed=reviews - FORMATO DA RESPOSTA - STATUS 200`
```json
 {
    "id": 1,
    "name": "The Random Heros",
    "type": "ficção",
    "duration": 120,
    "synopsis": "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores repellat.",
    "image": "https://res.cloudinary.com/dsbkp5841/image/upload/v1688390764/Rectangle_5_mgqd46.jpg",
    "reviews": [
      {
          "id": 1,
          "movieId": 1,
          "userId": 1,
          "score": 8,
          "description": "Filme muitoooooo bom."
      }
    ]
}
```

Também é possível buscar as avaliações de um usuário especifico por filme:

`GET /movies/:idMovie/reviews?userId=:idUser - FORMATO DA RESPOSTA - STATUS 200`
```json
[
  {
    "id": 1,
    "movieId": 1,
    "userId": 1,
    "score": 8,
    "description": "Filme muitoooooo bom."
  }
]
```

<h2 align ='center'> Criação de usuário </h2>

`POST /users - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "johndoe@email.com",
  "password": "123456",
  "name": "John Doe",
}
```

Caso dê tudo certo, a resposta será assim:

`POST /users - FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImpvaG5kb2VAZW1haWwuY29tIiwiaWF0IjoxNjg3ODA4MTYzLCJleHAiOjE2ODc4MTE3NjMsInN1YiI6IjMifQ.nWj1gqD4t3x00UTQvfFiK-PQjcgSpzbGeHknpncgC9E",
  "user": {
    "email": "johndoe@email.com",
    "name": "John Doe",
    "id": 3
  }
}
```


<h2 align = "center"> Login </h2>

`POST /login - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "johndoe@email.com",
  "password": "123456"
}
```

Caso dê tudo certo, a resposta será assim:

`POST /login - FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImpvaG5kb2VAZW1haWwuY29tIiwiaWF0IjoxNjg3ODA4MTYzLCJleHAiOjE2ODc4MTE3NjMsInN1YiI6IjMifQ.nWj1gqD4t3x00UTQvfFiK-PQjcgSpzbGeHknpncgC9E",
  "user": {
    "email": "johndoe@email.com",
    "name": "John Doe",
    "id": 3
  }
}
```

<h2 align ='center'> Consultar usuários </h2>

`GET /users - FORMATO DA REQUISIÇÃO`

```json
[
	{
		"email": "kenzinho@mail.com",
		"name": "Kenzinho",
		"age": 38,
		"id": 1
	}
]
```

<h2 align ='center'> Consultar um único usuario </h2>

`GET /users/:id - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "kenzinho@mail.com",
  "name": "Kenzinho",
  "age": 38,
  "id": 1
}
```

## Rotas que necessitam de autorização

Rotas que necessitam de autorização deve ser informado no cabeçalho da requisição o campo "Authorization", dessa forma:

> Authorization: Bearer {token}

<h2 align ='center'> Criar uma avaliação </h2>

`POST /reviews - FORMATO DA REQUISIÇÃO`

```json
{
  "movieId": 1,
  "userId": 1,
  "score": 8,
  "description": "Filme muitoooooo bom."
}
```

<h2 align ='center'> Atualizar uma avaliação </h2>

`PUT /reviews/:id - FORMATO DA REQUISIÇÃO`

```json
{
  "movieId": 1,
  "userId": 1,
  "score": 8,
  "description": "Filme muitoooooo bom."
}
```

Também é possível deletar uma avaliação, utilizando este endpoint:

`DELETE /reviews/:id`

```
Não é necessário um corpo da requisição.
```
