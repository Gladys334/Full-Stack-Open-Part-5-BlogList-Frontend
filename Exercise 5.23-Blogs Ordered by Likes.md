Exercise 5.23: Blogs Ordered by Likes

Goal: Make sure the blogs are shown from the one with the most likes to the one with the least.

Code Example:
it('Blogs are ordered according to likes', function() {
  cy.get('.blog').then(blogs => {
    const likes = blogs.map((i, el) => parseInt(Cypress.$(el).find('.likes').text()))
    const sortedLikes = [...likes].sort((a, b) => b - a)
    expect(likes.get()).to.deep.equal(sortedLikes)
  })
})

Explanation: It checks that the most liked blogs show up first.
