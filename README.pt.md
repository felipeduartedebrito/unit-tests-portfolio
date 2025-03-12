# Unit Test Portfolio

Bem-vindo ao repositório de Testes Unitários do meu Portfólio de Automação de Testes!

Este repositório foi criado para demonstrar minha abordagem na criação de testes unitários, focando na validação de funções e métodos isolados. Aqui, utilizo exemplos inspirados na lógica de negócio do Medusa para ilustrar as melhores práticas em desenvolvimento de testes – desde o uso adequado de mocks até a cobertura de cenários positivos, negativos e de borda.

## Objetivos

- Isolamento de Funções: Garantir que cada componente ou função seja testado de forma independente.
- Uso Eficiente de Mocks: Simular dependências e isolar a unidade em teste utilizando os recursos nativos do Jest.
- Cobertura Abrangente: Incluir testes que validem tanto os cenários esperados quanto os casos de erro e condições extremas.

## Tecnologias Utilizadas

- Linguagem: JavaScript
- Framework de Testes: Jest
- Mocking: Implementado diretamente com Jest (sem a necessidade de bibliotecas adicionais)
- Contexto do Projeto: Exemplos inspirados na lógica do Medusa

## Como Executar os Testes

1. Instale as dependências:
   Execute no terminal:
   npm install

2. Execute os testes:
   Para rodar os testes unitários com Jest, utilize:
   npm test

3. Gerar Relatório de Cobertura (Opcional):
   Para visualizar a cobertura dos testes, execute:
   npx jest --coverage

## Exemplo de Caso de Teste

A seguir, um exemplo de teste unitário para uma função `calculateDiscount`, simulando parte da lógica de negócio:

// tests/calculator/calculator.test.js
const { calculateDiscount } = require('../../src/calculator');

describe('calculateDiscount', () => {
  test('retorna o desconto correto para valores válidos', () => {
    const price = 100;
    const discountRate = 0.1;
    const expectedDiscount = 10;
    const discount = calculateDiscount(price, discountRate);
    expect(discount).toBe(expectedDiscount);
  });

  test('retorna 0 quando a taxa de desconto é 0', () => {
    const price = 100;
    const discountRate = 0;
    const discount = calculateDiscount(price, discountRate);
    expect(discount).toBe(0);
  });
});

## Boas Práticas Aplicadas

- Testes Focados: Cada teste avalia uma única funcionalidade, promovendo clareza e facilidade de manutenção.
- Isolamento por Mocks: Utilização dos mecanismos de mocking do Jest para simular dependências e concentrar os testes na unidade em questão.
- Cobertura de Cenários Diversos: Inclusão de casos positivos, negativos e de borda para assegurar a robustez do código.

## Contribuições

Este repositório faz parte do meu portfólio de automação de testes. Estou sempre aberto a sugestões e feedbacks que possam enriquecer as práticas aqui demonstradas. Sinta-se à vontade para abrir uma issue ou enviar um pull request com melhorias e ideias.

## Contato

- Email: felipe.dua.brito@gmail.com
- LinkedIn: https://www.linkedin.com/in/felipe-duarte-de-brito-0ba3bb199/

Felipe Duarte de Brito
