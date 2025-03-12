# Unit Test Portfolio

Welcome to the Unit Tests repository of my Test Automation Portfolio!

This repository was created to demonstrate my approach to unit testing, focusing on validating isolated functions and methods. Here, I use examples inspired by Medusa's business logic to illustrate best practices in test development—from properly using mocks to covering positive, negative, and edge cases.

## Objectives

- Function Isolation: Ensure that each component or function is tested independently.
- Efficient Use of Mocks: Simulate dependencies and isolate the unit under test using Jest's native capabilities.
- Comprehensive Coverage: Include tests that validate both expected scenarios and error/edge cases.

## Technologies Used

- Language: JavaScript
- Test Framework: Jest
- Mocking: Implemented directly with Jest (no additional libraries required)
- Project Context: Examples inspired by Medusa's business logic

## How to Run the Tests

1. Install the dependencies:
   Run in the terminal:
   npm install

2. Run the tests:
   To execute the unit tests with Jest, use:
   npm test

3. Generate a Coverage Report (Optional):
   To view the test coverage, run:
   npx jest --coverage

## Example Test Case

Below is an example unit test for a `calculateDiscount` function, simulating part of the business logic:

// tests/calculator/calculator.test.js
const { calculateDiscount } = require('../../src/calculator');

describe('calculateDiscount', () => {
  test('returns the correct discount for valid values', () => {
    const price = 100;
    const discountRate = 0.1;
    const expectedDiscount = 10;
    const discount = calculateDiscount(price, discountRate);
    expect(discount).toBe(expectedDiscount);
  });

  test('returns 0 when the discount rate is 0', () => {
    const price = 100;
    const discountRate = 0;
    const discount = calculateDiscount(price, discountRate);
    expect(discount).toBe(0);
  });
});

## Best Practices Applied

- Focused Tests: Each test evaluates a single functionality, promoting clarity and ease of maintenance.
- Isolation with Mocks: Utilizing Jest’s native mocking mechanisms to simulate dependencies and concentrate tests on the unit under evaluation.
- Diverse Scenario Coverage: Including positive, negative, and edge cases to ensure robust code validation.

## Contributions

This repository is part of my Test Automation Portfolio. I am always open to suggestions and feedback to enhance the practices demonstrated here. Feel free to open an issue or submit a pull request with improvements and ideas.

## Contact

- Email: felipe.dua.brito@gmail.com
- LinkedIn: https://www.linkedin.com/in/felipe-duarte-de-brito-0ba3bb199/

Felipe Duarte de Brito
