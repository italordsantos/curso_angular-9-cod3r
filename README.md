# Projeto de estudo do Angular 9 - Curso by [Cod3r](https://www.cod3r.com.br/ "Cod3r")

## Ferramentas
- npm: gerenciar as dependências do projeto
- JsonServer: ele lê um arquivo que tem um json e cria uma API baseada nele
- TypeScript: linguagem para o angular. Eles posteriormente converte para JS, HTML e CSS

## Processos de instalação
- Inicie um projeto com `npm init -y`
- Instale o gerador da API `npm i json-server`
- Crie o arquivo que servirá como banco de dados para a nossa API `db.json`
- Popule o banco com alguns dados iniciais:
```json
{
    "products": [
        {
            "id": 1,
            "name": "Caneta",
            "price": 5.89
        },
        {
            "id": 2,
            "name": "Macbook",
            "price": 6289.89
        },
        {
            "id": 3,
            "name": "Tablet",
            "price": 650.99
        }
    ]
}
```

## Conceitos
- `main.ts`: o primeiro arquivo
 - Ele carrega depois o `AppModule`
   - Os componentes são separados por módulos, com isso é possível alterar a visibilidade de cada componente presente no módulo
   - O atributo `bootstrap` significa "carregar"/"inicializar", ou seja, nele vai ser definido qual o módulo de componente que dará início à aplicação em si
   - Nisso, ele chama o `AppComponent`, que futuramente pode chamar outros componentes e assim vai
- Componente é um trecho de código que representa um componente visual na sua interface, como um botão, input
 - Autocontido: HTML, CSS e TS
 - O componente possui Comportamento com o TS, Estrutura com o HTML e o Estilo com o CSS
 - Exemplo de componente:
   - home.component.css
   - home.component.html
   - home.component.ts
- Ao criar este componente, você poderá utilizá-lo através de uma tag personalizada, como: `<app-home></app-home>`
- Anatomia do módulo: ele contém os 5 atributos abaixo que são usados para configurar o módulo
  - Declarations: componentes, diretivas e pipes. Este atributo é utilizado principalmente para declarar os componentes, porém, não necessariamente eles estarão visíveis fora do módulo. Para tal, é necessário exportá-los no atributo de Exports.
  - Exports: componentes, diretivas e pipes. Aqui você declara quais partes você quer tornar visível além do módulo declarado.
  - Imports: aqui você importa outros módulos que serão utilizados, tipo o Material Design.
  - Providers: aqui são declarado os services.
  - Bootstrap: o componente que será carregado ao inicializar o módulo, tipo o "main".