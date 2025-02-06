# Tech-Quiz-Test-Suite
this underscores the importance of ensuring reliability and robustness in modern web applications through comprehensive testing. In today's dynamic development environment, testing is not just an afterthought but a critical part of the development process that ensures applications meet user demands and perform efficiently under various conditions.
 The app was built using the MERN stack with a React front end, MongoDB database, and Node.js/Express.js server and API. It allows users to take a quiz of ten random questions and view their final score.

 ## To get started you’ll need to do the following:

1. Install Cypress as a dev dependency

2. Configure Cypress for both component and end-to-end testing

3. Create a component test for the quiz component

4. Create an end-to-test for the quiz component

Your testing should use [Cypress](https://docs.cypress.io/guides/overview/why-cypress) to run both the component tests and the end-to-end tests. The testing will be invoked using the following command:

```bash
npm run test
npx cypress run --component (Run Component Tests)
npx cypress run (Run End-to-End Tests)
```


It's recommended that you start with a directory structure that looks like the following example:

```md
.
├── client/                 // the client application
├── cypress/                // Folder for Cypress
    ├── component/          // Folder for component tests
        └── Quiz.cy.jsx     // Component tests for the Quiz component
    ├── e2e/                // Folder for end-to-end tests
        └── quiz.cy.js      // End-to-end tests for the Tech Quiz
    ├── fixtures/           // Folder for test fixtures
        └── questions.json  // Mock data for testing
    └── tsconfig.json
├── server/                 // the server application
├── .gitignore
├── cypress.config.ts       // Runs the application using imports from lib/
├── package.json
├── tsconfig.json
└── README.md              // App description, link to video, setup and usage instructions           
```

## Key Considerations
- Adjust Selectors: Make sure to replace placeholders like `.question-text` with the actual CSS selectors or `data-testid` attributes for better stability in tests.
- Handle Asynchronous Operations: If your quiz has asynchronous operations (e.g., API calls), use commands like `cy.wait()` or `cy.intercept()` to handle them effectively.

## User Story

```md
AS AN aspiring developer
I WANT to take a tech quiz
SO THAT I can test my knowledge and improve my skills
```
## Mock-Up

The following animation demonstrates the application functionality:

![A GIF demonstrates a functioning quiz.](./Assets/19-testing-homework-demo.gif)