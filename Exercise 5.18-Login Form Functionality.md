Exercise 5.18: Login Form Functionality

Goal: Write a test that checks if a user can login correctly when they enter the right username and password

Code Example:
it('User can log in', function() {
  cy.get('#username').type('testuser')
  cy.get('#password').type('password123')
  cy.get('#login-button').click()

  cy.contains('testuser logged in')
})

Explanation: It makes sure login works when the right username and password are entered.
