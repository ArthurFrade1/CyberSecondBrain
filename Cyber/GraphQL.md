É uma linguagem de consulta para APIs, junto com uma especificação e runtime. é uma forma de se usar o protocolo HTTP para comunicação front-back-end assim como o REST, mas diferentemente do REST não é focado em recursos.
A principal diferença entre o REST e GraphQL é que o rest se busca uma informação como:
`GET /user/jhon` e assim obtém os dados do usuário. 
Já o GraphQL busca informações sempre com o :
`/graphql` e dentro do corpo da requisição são enviados os campos que se deseja obter.

### A idéia

A ideia surgiu pelos ocnceitos de *underfetching* e *overfatching* que ocorre com o uso arquitetural do REST, em que não é possível especificar diretamente o que se quer de resposta do servidor, ao buscar por `/user/jhon` provavelmente o servidor vai retornar o nome, idade, endereço e etc... Todas informações sobre aquele usuário, aí o front vai separar o que é útil, provavelmente menos que isso ou vai faltar alguma informação, tendo que consultar outro *endpoint*.

Com o GraphQL isso não acontece, pois a busca é exatamente pelo que se deseja, como: 

`"query": "query { user(id: 1) `{ id name}}"`
obtendo assim justamente os campos desejados, deixando uma arquitetura mais organizada, de mais fácil manutenção e com menos trafégo desnecessário de dados

#### Quando usar
O uso é indicado somente em aplicações mais robustas e complexas em que o front pode pedir uma variedade muito grande de coisas e pra isso seria necessário criar muitos endpoints ou retornar um número muito grande de informações me um endpoint só