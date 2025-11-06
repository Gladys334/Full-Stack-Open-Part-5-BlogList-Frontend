Exercise 5.17- Blog List End-to-End Testing (Step 1)

Goal: Install Cypress and make a test that checks if the login form shows up when the app first opens.

Code Example:
describe('Blog app', function() {
  beforeEach(function() {
    cy.visit('http://localhost:5173')
  })

  it('Login form is shown', function() {
    cy.contains('login').should('be.visible')
    cy.contains('username')
    cy.contains('password')
  })
})

Explanation: This test checks that the login form shows up automatically when someone opens the app
