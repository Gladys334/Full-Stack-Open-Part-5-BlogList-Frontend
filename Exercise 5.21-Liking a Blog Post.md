Exercise 5.21: Liking a Blog Post

Goal: Write a test that checks if a user can like a blog post.

Code Example:
it('User can like a blog post', function() {
  // log in first
  cy.get('#username').type('testuser')
  cy.get('#password').type('password123')
  cy.get('#login-button').click()

  // make sure a blog exists
  cy.contains('new blog').click()
  cy.get('#title').type('Like Feature Test')
  cy.get('#author').type('Tester')
  cy.get('#url').type('https://testblog.com')
  cy.get('#create-button').click()

  // like the blog
  cy.contains('Like Feature Test').parent().find('.view-button').click()
  cy.contains('like').click()

  // check that like count increased
  cy.contains('likes 1')
})

Explanation: This test makes sure that when a use is logged-in, they can click the like button and the like count goes up.
