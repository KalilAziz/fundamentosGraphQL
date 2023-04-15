- Quais problemas GraphQL resolve?
  - Overfetching
    - http://localhost:3000/users
      - DB (usuários, endereços)
  - Underfetching
    - http://localhost:3000/users
      - DB (usuários)
- Como GraphQL funciona?
  - O GraphQL é uma linguagem de consulta para APIs
  - O GraphQL serve como uma camada de abstração entre o cliente e o servidor
  - O Graph é uma linguagem de realização de queries, tanto escrita quanto leitura
- Como GraphQL se compara a REST?

  - REST
    - http://localhost:3000/users
      - DB (usuários, endereços)
  - GraphQL

    - http://localhost:3000/graphql
      - DB (usuários, endereços)

  - O principal ponto do GraphQL é a realização de queries, onde podemos fazer
    queries de forma mais simples e direta, sem a necessidade de realizar
    requisições para múltiplas rotas, como no REST. Além de poder obter apenas
    os dados que precisamos, sem a necessidade de realizar requisições para
    múltiplas rotas, como no REST

```gql
query {
  users {
    id
    name
    email
    address {
      street
      number
      city
      state
    }
  }
}
```

- Diferentemente da Rest, que não iríamos conseguir escolher quais dados
  queremos, no GraphQL podemos escolher quais dados queremos, sem a necessidade
  de realizar requisições para múltiplas rotas, como no REST

- Dificuldades:

  - Como qualquer nova ferramenta, o GraphQL possui algumas dificuldades, que
    são:
    - Acaba trazendo mais complexidade para o projeto
    - Aumenta a curva de aprendizado
    - Aumenta a complexidade do projeto
    - Dificuldade de cache de dados
    - Dificuldade de debug
    - Dificuldade de Tratatamento de Erros

- Apollo CLient
  - A dificuldade de utilizar o GraphQL é que ele não é uma linguagem de
    programação, mas sim uma linguagem de consulta, que é utilizada para
    realizar queries, tanto escrita quanto leitura, para o servidor. Por isso,
    precisamos de uma ferramenta que nos ajude a realizar essas queries, e
    essa ferramenta é o Apollo Client
