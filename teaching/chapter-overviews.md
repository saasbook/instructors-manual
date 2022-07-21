Here is a 1-paragraph overview of the main content-oriented didactics (COD)
in each chapter, and the associated CHIPS or other materials for
hands-on practice.

# 1. Introduction to Software as a Service, Agile Development, and Cloud Computing

We contrast SaaS with shrink-wrapped software, Agile with other
development methodologies, and cloud computing with earlier models of
provisioning computing, and describe the synergy among the three.
SaaS/cloud/agile are not necessarily always
superior, but the learner should understand when each is
appropriate to use.  We describe techniques that programmers have
developed over time to improve their productivity, such as software
reuse, conciseness, and rich tooling.  We introduce the fundamental
architectural concepts of cloud computing and mobile clients.
Finally, we emphasize the importance of the maligned term "legacy
code," the relationship between legacy code and beautiful code (and
refacotring), and why all software engineers should hope that their code
becomes legacy code.

{% hint style="info" %}
In describing cloud+client app architecture, we avoid diving into "client
native" frameworks such as React Native or iOS, since these present
significant learning-curve and maintainability challenges and all the concepts
we need to teach can be embodied in mobile-first HTML/CSS/JavaScript apps.
{% endhint %}

The next five chapters form Part I of the book, which covers SaaS
architecture, a server-side SaaS language and framework (Ruby and
Rails), and client-side SaaS language and framework (JavaScript and jQuery).

# 2. How to Learn a New Language

This quick introduction will get you up to speed on how to learn any
new language and framework, using Ruby, a highly productive scripting
language, as an example.
We focus on the unique productivity-enhancing features of Ruby that
may be unfamiliar to Python programmers, and we omit many details that
are well covered by existing materials.
As with all languages, becoming truly comfortable with Ruby's
powerful features will require going beyond this material; the end of
the chapter gives suggested resources.

* **CHIPS 2.5 Ruby Intro:** a gentle intro to Ruby idioms, including
running instructor-provided unit tests to check your answers 

# 3. SaaS Application Architecture: Microservices, APIs, and REST

Fundamentally, a RESTful SaaS app is a collection of resources and
operations on those resources.
This chapter examines the basics of the client-server Web
architecture for SaaS, which uses HTTP, HTML, and JSON as the
mechanisms by which resources are represented and operations on them
are carried out.  We'll contrast Service-Oriented Architecture and its
latest manifestations, microservices and serverless computing, with
traditional monolithic SaaS.  We'll put all these ideas together by
building and deploying a simple SaaS app that plays a
letter-guessing-based word game, using the simple Ruby-based framework Sinatra.

* **CHIPS 3.3 HTTP and URIs:** intro to HTTP requests, URIs, and
cookies, using `curl` and `netcat` to see raw data 

* **CHIPS 3.7 Create and Deploy a Simple SaaS App** de-mystifies the
creation of a SaaS app (a simple word-guessing game using Sinatra)
including use of an external service, and how to think about RESTfully
"wrapping" application logic in SaaS. 

# 4. SaaS Framework: Rails as a Model--View--Controller Framework

Rails is a Ruby-based framework that uses three
  patterns to organize SaaS apps:
  Model--View--Controller for the app as a whole, Active Record for 
  models backed by a relational database in the persistence tier, and
  Template View for constructing HTML pages.  For
  conciseness, DRYness and productivity, Rails makes pervasive use of
  Ruby's reflection and 
  metaprogramming as well
  as [convention over
  configuration](https://en.wikipedia.org/wiki/Convention_over_configuration),
  a design paradigm that
  automates some configuration based on the names of
  data structures and variables.  Although
  Rails presents a lot of machinery for the simple examples
  developed in this chapter, you will quickly ``grow into'' these
  features as your apps become more sophisticated.

* **CHIPS 4.3 ActiveRecord Basics**: write ActiveRecord queries against a provided seeded database.

* **CHIPS 4.5 Rails Routes**: not actually a homework assignment, but
a simple app that lets students enter syntactically valid Rails routes
and understand the RESTful routes that Rails would generate for them. 

* **CHIPS 4.7 Word Guesser on Rails**: use the same Hangperson game
logic and Cucumber scenarios as CHIPS 3.7, but scaffolds a walkthrough
of how to deploy the app with Rails instead of Sinatra, as an on-ramp
understanding the complex Rails framework. 

* **CHIPS 4.9 Hello Rails**: create a brand-new Rails app
(RottenPotatoes) from scratch, including routes, database setup, using
the debugger, and deploying to Heroku.


# 5. SaaS Framework: Advanced Programming Abstractions for SaaS

This chapter explores three sets of mechanisms for
  DRYing out your code, thereby making it more concise, beautiful and
  maintainable.  Model validations and controller filters centralize
  what invariants must hold in order for a model object to be valid (for
  example, a movie must have a nonblank title) or for a controller
  action to proceed (for example, the user must be logged in as an
  admin).  ActiveRecord Associations use Ruby language features to
  represent and manipulate relationships among different types of
  ActiveRecord models, while using relational-database functionality to
  represent these relationships as foreign-key associations.  
  Finally, scopes let you encapsulate different ActiveRecord queries
  into composable ``building blocks'' that you can easily reuse to add
  new query functionality to your app.
  In each case,
  tastefully-chosen language features and framework architecture support
  DRY and concise app code.

* **CHIPS 5.3 Rails Intro**: enhance RottenPotatoes to filter and sort
movie lists.

{% hint style="info" %}
Coming soon: CHIPS 5.3 will be augmented to also add SSO login to
RottenPotatoes, and a new CHIPS 5.7 on Associations will add Reviews
to RottenPotatoes, where each review is associated with both a movie
and a reviewer.
{% endhint %}



# 6. Mobile and Desktop SaaS Clients: JavaScript Introduction

{% hint style="danger" %}
This chapter topically belongs in Part I, but should perhaps be
covered later, and can be excluded entirely.  Many interesting SaaS
apps are possible without JavaScript, and the advice on JavaScript TDD
makes more sense if covered after Chapter 8.
{% endhint %}

Proper use of JavaScript enhances the user experience and can make
SaaS apps richer and more interactive.
The Web's client-side programming language has a
bad reputation because most people who use it lack the programming
experience to use its unusual features to write beautiful
code.   
The approach
that Chapter 2 introduced for learning Ruby and Rails is  used here to quickly
introduce JavaScript, jQuery,and AJAX.
The approach to RSpec in Chapter 8 is mirrored in introducing Jasmine
for test-driven development in JavaScript.


{% hint style="info" %}
We  deliberately avoid introducing "heavyweight" client-side
frameworks such as React or Angular because they add significant complexity and learning curve
that is unnecessary for many apps, and because our focus is on the
cloud (SaaS) aspects of the app.  
{% endhint %}

{% hint style="info" %}
Coming soon: CHIPS 6.9 will add AJAX enhancements to RottenPotatoes.
{% endhint %}

The next six chapters form Part II of the book, which covers software development. Each chapter first introduces and explains the Agile approach to the topic, plus a section at the end of the chapter that offers the contrasting approach from the Plan-and-Document perspective.

# 7. Requirements: Behavior-Driven Design and User Stories

The first step in the Agile cycle, and 
 often the most difficult, is a dialogue with each of the 
 stakeholders to understand the requirements. We first derive \w{user stories}, which are short narratives each describing a specific interaction between some stakeholder and the application. Velocity-based iteration planning,
supported by tools such as [Pivotal Tracker](https://pivotaltracker.com), use user stories to help 
estimate the difficulty of the work so as to produce a schedule and how to
correct the schedule when actual progress differs from predicted
progress. The [Cucumber](https://cukes.info) tool turns these stylized
but informal English narratives into acceptance and integration
tests. As SaaS usually involves end users, we also need a user
interface. We do this with _low-fidelity (Lo-Fi)_ drawings of the
Web pages and combine them into _storyboards_ before creating the UI
in HTML. 
In this chapter you will learn requirements elicitation, cost
estimation, project scheduling, and monitoring progress. 

* **CHIPS 7.7 Intro to BDD and Cucumber**: write Cucumber features
(integration/acceptance tests) to test
happy and sad paths of RottenPotatoes. 

# 8. Testing: Test-Driven Development

 In test-driven development, you first write failing tests for
 a small amount of nonexistent code and then fill in the code needed to
 make them pass, and look
 for opportunities to refactor (improve the code's structure) before
 going on to the next test case.  
 This cycle is sometimes called Red--Green--Refactor,
 since 
 many testing tools print failed test results in red and passing
 results in green.
 To keep tests small and isolate them from the behavior of other
 classes, we introduce mock
 objects and stubs as examples of _seams_---places where you can
 change the behavior of your program at testing time without changing
 the source code itself.

{% hint style="info" %}
Coming soon: revamped CHIPS 8.5 that scaffolds the process of learning
to write RSpec tests.
{% endhint %}

* **CHIPS 8.9 BDD/TDD Cycle:** a complete pass through the BDD and TDD
cycle of specifying a feature in terms of stories and then using TDD
with RSpec to drive the development and deployment of the feature. 

# 9. Software Maintenance: Enhancing Legacy Software Using Refactoring and Agile Methods

Out of every dollar spent on software, 36% is spent on
  enhancements, 10% on fixing bugs, 11% on adapting to environmental
  changes such as new library versions or API changes, and 3% on
  _refactoring_ to make the software more maintainable.  In total,
  therefore, about 60% of software expenses is devoted to software
  maintenance, so your first job is more likely to involve improving
  existing code than creating a brand-new system from a clean slate.
  Chapters 7--8 (BDD+TDD) looked at disciplined
  ways to evolve new code.  Although thorough formal documentation of
  legacy systems may be lacking or inaccurate, the Agile techniques we
  already know can be pressed into service to help understand the
  structure of legacy software and create a foundation for extending and
  modifying it with confidence.  We describe what good code looks
  like and why, and show how to apply refactoring techniques to
  legacy code both to make it more testable (and therefore modifiable
  with confidence) and to leave it in better shape than we found it for
  the next developers.  

# 10. Agile Teams


Programming is now primarily a team sport, and this
 chapter covers techniques that can help teams succeed. 
_Pair programming, design reviews, and code reviews_ can improve
software quality. Good version control practices, supported by tools
such as Git,  
address code management.  Distributed development using
branch-per-feature, pull requests, and upstream merging allows ``teams
of teams'' to collaborate on large projects.  We outline successful
workflows for small teams that keep everyone in sync and disseminates
knowledge about different parts of the codebase to all team members.

* **CHIPS 10.5  Agile Iterations:** Two (or more) full iterations of
Agile adding features to an existing (legacy) app

{% hint style="info" %}
**Bluejay**, a tool for scaffolding students through the Agile
workflow (claim a story, make a feature branch, request code review
via pull request, deliver feature to client) will be made available to
instructors soon.
{% endhint %}

# 11. Design Patterns for SaaS Apps

Besides reusability, programmer productivity requires
concise, readable code with minimal clutter.
In this chapter, we describe some concrete guidelines for making your
class architecture DRY and maintainable: the SOLID principles of
object-oriented design---Single Responsibility, Open/Closed, Liskov
Substitution, Injection of Dependencies, and Demeter---and some design
patterns supporting them. 
We will learn about design smells and metrics that may warn you of
violations of SOLID, and explore some refactorings to fix those
problems.
In some cases, those refactorings will lead us to one of a collection a
design patterns---proven ``templates'' for class interaction that
capture successful structural solutions to common software problems.

# 12. Dev/Ops

Unlike shrink-wrapped software, SaaS developers are
  typically  much closer to post-release
  operations and maintenance.  This chapter covers what your SaaS app
  should _not_ do when released: crash, become unresponsive when it
  experiences a surge in popularity, or compromise customer data.  Since
  many of these concerns are greatly alleviated by deploying in a
  well-curated PaaS (Platform-as-a-Service) environment such as Heroku,
  we focus on how to steward your app to leverage those benefits as long
  as possible by monitoring to identify problems that
  interfere with responsive service,
  addressing those problems with caching and efficient database usage, 
  and thwarting common attacks against customer data.
  
* **CHIPS  12.8 Exploiting Caching and Indices:** improve the
performance of RottenPotatoes by adding database indices to speed up
key queries. 

# 13. Afterword

In this chapter we give perspectives on the big ideas in this book---Agile, Cloud Computing, Rails, SaaS, and SOA---and show how Berkeley students who have graduated and taken jobs in industry rank their importance.
