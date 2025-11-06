Exercise 5.19: Login Fails With Wrong Credentials

Goal: Write a test that checks if the app shows an error message when a user enters the wrong username or password.

Code Example:
it('Login fails with wrong password', function() {
  cy.get('#username').type('testuser')
  cy.get('#password').type('wrongpass')
  cy.get('#login-button').click()

  cy.contains('invalid username or password')
  cy.get('html').should('not.contain', 'testuser logged in')
})

Explanation: It checks that login fails when the password is wrong.
