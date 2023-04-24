# CHIPS (Programming assignments)

To complement the Content-Oriented Didactic (COD) materials such as the book and lectures, CHIPS (Coding & Hands-on Integrated Projects) provide hands-on skills practice and are keyed to specific sections in the book. This section describes how to use them with Codio. The [book's website](http://www.saasbook.info/instructors) has other options if you don't wish to use Codio, but we have pretty extensive automated workflows that are optimized for Codio, for publishing both the book content itself and these CHIPS along with their autograders.

The relative effort of each CHIPS is indicated by one star (a couple of hours of work), two stars (several hours of work), or three stars (a potentially multi-day assignment).

If you're using Codio, all you really need to know is how the CHIPS work—see below. If you want to use the CHIPS outside of Codio, or contribute to their development, look at the README in the CHIPS [repo](https://github.com/saasbook/chips) (visible to [registered instructors](https://www.saasbook.info/instructors)).

Here's a quick summary of the assignments, presented in the order in which they appear in the [ESaaS textbook](http://www.saasbook.info). There are three types:

1. **Autograded:** The solutions repos include reference solutions, Codio-based autograders in the Codio course, and files for manually configuring [Gradescope](https://gradescope.com)-based autograding. (Gradescope is no longer officially supported, so use those files at your own risk.)
2. **Self-graded:** CHIPS involves coding, but rather than an autograder, includes tests students run themselves.
3. **Comprehension:** CHIPS involves minimal or no coding, but rather performing some tasks and answering self-check questions about them. The questions are usually built into the Codio version of the assignment.



* 2.5 [Ruby Intro](https://github.com/saasbook/hw-ruby-intro) ([autograder/solutions](https://github.com/saasbook/hw-ruby-intro-ci)): gentle intro to Ruby idioms, including running instructor-provided unit tests to check your answers
* 3.3 [HTTP and URIs](https://github.com/saasbook/hw-http-intro) (comprehension): intro to HTTP requests, URIs, and cookies, using `curl` and `netcat` to see raw data, using the [esaas-cookie-demo app](https://esaas-cookie-demo.herokuapp.com) ([source](https://github.com/saasbook/esaas-cookie-demo)).
* 3.7 [Create and Deploy a Simple SaaS App](https://github.com/saasbook/hw-sinatra-saas-wordguesser) ([autograder/solutions](https://github.com/saasbook/hw-sinatra-saas-wordguesser-ci)): de-mystifies the creation of a SaaS app (a simple word-guessing game using Sinatra) including use of an external service, and how to think about RESTfully "wrapping" application logic in SaaS.
* 4.3 [ActiveRecord Basics](https://github.com/saasbook/hw-activerecord-practice) (self-graded): write ActiveRecord queries against a provided seeded database.
* 4.5 [Rails Routes](https://rails-routing-practice.herokuapp.com) (self-graded): not actually a homework assignment, but a simple app that lets students enter syntactically valid Rails routes and understand the RESTful routes that Rails would generate for them.
* 4.7 [Word Guesser on Rails](https://github.com/saasbook/hw-rails-wordguesser) (comprehension with [reference solutions](https://github.com/saasbook/hw-rails-wordguesser-ci)): use the same Hangperson game logic and Cucumber scenarios as CHIPS 3.7, but scaffolds a walkthrough of how to deploy the app with Rails instead of Sinatra, as an on-ramp understanding the complex Rails framework.
* 4.9 [Hello Rails](https://github.com/saasbook/hw-hello-rails) (self-graded): create a brand-new Rails app (RottenPotatoes) from scratch, including routes, database setup, using the debugger, and deploying to Heroku.
* 5.3 [Rails Intro](https://github.com/saasbook/hw-rails-intro) ([autograder/solutions](https://github.com/saasbook/hw-rails-intro-ci)): enhance RottenPotatoes to filter and sort movie lists. (Coming soon: also add SSO login to RottenPotatoes.)
* 5.7 Associations (TBD)
* 6.9 AJAX Enhancements to RottenPotatoes (TBD)
* 7.7 [Intro to BDD and Cucumber](https://github.com/saasbook/hw-bdd-cucumber) ([autograder/solutions](https://github.com/saasbook/hw-bdd-cucumber-ci)): write features to test happy and sad paths of RottenPotatoes.
* 8.5 [RSpec on Rails](https://github.com/saasbook/hw-tdd-rspec): (**Note:** This CHIPS is in the process of being replaced. We recommend just using 8.9 until that time.) Given a Cucumber scenario for a not-yet-implemented feature, students use TDD and RSpec to write tests that drive the creation of the code to make the scenario pass. Students also learn to use Travis CI to automate testing workflow.
* 8.9 [BDD/TDD Cycle](https://github.com/saasbook/hw-acceptance-unit-test-cycle-lite): a complete pass through the BDD and TDD cycle of specifying a feature in terms of stories and then using TDD with RSpec to drive the development and deployment of the feature.
* 10.5 Agile Iterations Two (or more) full iterations of Agile adding features to an existing (legacy) app
* 12.8 [Exploiting Caching and Indices](https://github.com/saasbook/hw-indices-performance): improve the performance of RottenPotatoes by adding database indices to speed up key queries.

### Optional additional CHIPS (not referenced in textbook)

* [Oracle of Bacon](https://github.com/saasbook/hw-oracle-of-bacon): Build a simple command-line app that uses external services in a SOA, including parsing XML responses.
* [Design Review](https://github.com/saasbook/hw-design-review): We use this in the project portion of the course. This is not a programming assignment but rather a 3-part scaffolded process for doing design reviews and technical presentations. (Each part can be used more or less independently.) It is intended to be used in conjunction with student teams doing their own open-ended projects, so no code is provided. In part 1 (Design Review), teams are paired up and each team evaluates the other's design and gives feedback on possible improvements. In part 2 (Presentation), teams give technical presentations about the design review; these are peer-evaluated (or instructor-evaluated) according to a provided rubric. In part 3 (Handoff), teams modify their repos as needed to ensure the project is easy for another team to pick up and continue working on.
