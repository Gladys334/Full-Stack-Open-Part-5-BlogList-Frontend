Exercise 5.22: Delete a Blog

Goal: Check that the user who made the blog can delete it.

Code Example:
it('User can delete their own blog', function() {
  cy.contains('view').click()
  cy.contains('remove').click()
  cy.get('html').should('not.contain', 'Cypress testing made easy')
})

Explanation: This test makes sure that only the person who created the blog can remove it.
