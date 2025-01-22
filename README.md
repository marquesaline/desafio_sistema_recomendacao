# Sistema de Recomendação de Filmes

## Descrição

O desafio é criar um sistema de recomendação de filmes que terá as seguintes funcionalidades:

- Adicionar filmes
- Recomendar filmes com base no gênero informado pelo usuário
- Remover filmes com base no ID

Este desafio pode ser feito usando funções e módulos para organizar melhor o código. 

## Tarefas

### Gerar filmes fictícios

Para garantir que o sistema já tenha filmes para recomendar, deve ser usado as bibliotecas [Faker](https://faker.readthedocs.io/en/master/) e [random](https://docs.python.org/pt-br/3/library/random.html) para ajudar a gerar os dados.

Cada filme deve ser um dicionário composto dos seguintes dados:

```
{
  'id': 1,
  'nome': 'exemplo',
  'genero': 'ação',
  'classificacao': 4
}
```
**Os filmes devem ser armazenados em uma lista (lista de dicionários).**

Dicas:
- A biblioteca Faker pode gerar o nome dos filmes através da função `catch_phrase`.
- A biblioteca random pode ser usada para:
  - Escolher aleatoriamente um gênero de uma lista de gêneros disponíveis através da função `choice`.
    ```
    GENEROS = ["Ação", "Comédia", "Drama", "Suspense", "Ficção Científica"]
    ```
  - Gerar números aleatórios para a classificação do filme (por exemplo, valores entre 1 e 5).

### Adicionar filmes

Além dos filmes que são gerados automaticamente, o sistema deve permitir que o usuário adicione filmes seguindo a mesma estrutura mencionada no tópico anterior. 

Na adição alguns pontos devem ser observados:

1) O id do filme deve ser gerado automaticamente no momento da adição;
2) A classificação do filme deve ser um número inteiro entre 1 e 5;
3) Os filmes adicionados pelo usuário devem ser adicionados na mesma lista de filmes geradas no tópico anterior;

### Recomendação de filmes

O sistema deve permitir que o usuário informe um gênero e, com base nele, recomendar 3 filmes para o usuário assistir.

OBS: se houver menos de 3, mostrar todos os filmes do gênero.

Se não houver filmes disponíveis do gênero informado, o sistema deve exibir uma mensagem como: "Não há filmes desse gênero disponíveis no momento."

### Remoção de filmes

O sistema deve permitir que o usuário informe o ID de um filme e, com base nele, esse filme deve ser removido da lista de filmes. 

## Como o sistema deve funcionar

O sistema deve apresentar um menu interativo no terminal, permitindo que o usuário escolha a funcionalidade desejada. Cada opção deve corresponder a uma ação no sistema.

Exemplo:

```
Bem-vindo ao Sistema de Recomendação de Filmes!

Escolha uma opção:
1. Adicionar um novo filme
2. Recomendar filmes por gênero
3. Remover um filme pelo ID
4. Exibir todos os filmes cadastrados
5. Sair
```

O programa deve ficar mostrando o menu até que o usuário escolha a opção 'Sair'. 

Assim que o programa começar a rodar, ele deve gerar a lista de filmes fictícios.


