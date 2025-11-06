Exercise 5.20: Create a New Blog

Goal: Write test that checks if a logged-in user can add a new blog post.

Code Example:
it('User can add a new blog', function() {
  // log in first
  cy.get('#username').type('testuser')
  cy.get('#password').type('password123')
  cy.get('#login-button').click()

  // add a new blog
  cy.contains('new blog').click()
  cy.get('#title').type('Cypress Testing')
  cy.get('#author').type('Test User')
  cy.get('#url').type('https://cypress.io')
  cy.get('#create-button').click()

  // check that it appears on the page
  cy.contains('Cypress Testing')
})

Explanation: It makes sure users can add a new blog.
