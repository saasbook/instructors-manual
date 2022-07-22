# Philosophy: Why Agile? Why Rails? etc.

This book is a hands on path through the bewildering array of methodologies, languages, tools, and artifact types that collectively make up "software engineering." The goal is to instill good software habits in students—testability, software architecture, modularity, and reusability—while providing them the gratification of building a working deployed artifact that they themselves (and their peers) would use and find compelling.

This Instructors Manual contains the authors' own materials as well as materials and hints contributed by other instructors, by our student teaching assistants, by our students, and more.

We also document the relationship between these materials and the 2013 ACM-IEEE Computer Society software engineering curriculum standard.

### Student Projects and Learning By Doing <a href="#student-projects-and-learning-by-doing-.unnumbered" id="student-projects-and-learning-by-doing-.unnumbered"></a>

The ACM/IEEE software engineering curriculum guidelines emphasize the value of an iterative approach in which students assess and revise their work continuously. We have found that students are much more likely to actually follow the Agile methodology because the Ruby on Rails tools, which we introduce in this book, make it easy and because the advice is genuinely helpful for their projects. We believe Agile offers learning skills that transfer to non-agile projects, should need arise. We even show how to use Agile techniques on legacy code that wasn't developed that way to begin with; that is, Agile is good for more than just writing new code from scratch.

The ACM/IEEE curriculum guidelines also highlight team projects as a critical learning mechanism for software engineering students. The experience of many instructors (including ourselves) is that students enjoy learning and using Agile in projects. Its iteration-based, short-planning-cycle approach is a great fit for the reality of crowded undergraduate schedules and fast-paced courses. Busy students will by nature procrastinate and then pull several all-nighters to get a demo cobbled together and working by the project deadline; Agile not only thwarts this tactic (since students are evaluated on progress being made each iteration) but in our experience actually leads to real progress using responsible practices on a more regular basis.

One of the CHIPS (Coding/Hands-on Integrated Projects) assignments takes students through a two-iteration "mini-project" using Agile/XP workflows. To help you run successful projects, the contains detailed suggestions for organizing and scheduling project milestones in a classroom course, and gives example rubrics for grading the projects based on both the artifacts produced and the processes used to produce them, taking full advantage of being able to do multiple iterations in a single course. We also survey each generation of students to determine what they learned from the projects and where they had difficulty; the distills these "habits of highly effective projects" based on several offerings of the course at UC Berkeley and elsewhere.

### Why Software as a Service?

To motivate students, it's helpful to use a platform that lets them create compelling apps. Today there are approximately 4.2 billion mobile phones deployed worldwide, or enough for 3 out of every 5 people on the planet; combined with the explosive growth of SaaS, we believe the future of software is "client + cloud" applications that are split between a tablet or smart phone and a cluster of servers to do heavy computation and persist data.

Therefore, both mobile applications for smart phones and tablets and Software as a Service (SaaS) for cloud computing are compelling targets for teaching students. As you can teach the principles with either target, given the time constraints of a single college course, we choose in favor of the platform with the most productive tools. Our experience is that it is no contest: the programming and testing frameworks for SaaS and cloud computing are dramatically more productive than those for mobile apps, and the client part of many SaaS apps can be adapted to mobile devices using the HTML/CSS/JavaScript skills learned in creating SaaS.

In addition, beyond the commercial promise of SaaS and the "hireability" of students who know how to create it, SaaS projects can be deployed inexpensively using public cloud computing, which means students' course artifacts are on display for the whole world to see. The exposure and "look what I made" factor of public deployment are hard to match.

### Why Emphasize Agile?

While the Agile Manifesto was considered controversial when released in 2001, today Agile is an accepted practice alongside disciplined or Plan-and-Document processes like Spiral or the Rational Unified Process. As the textbook explains, most software companies now use Agile in both large and small projects; we provide guidance on when Agile makes sense, and we conclude that it certainly makes sense for student projects in a cloud-computing-centric software engineering course. Within each iteration, we are able to address the major issues of the software lifecycle in microcosm—requirements elicitation from the customer, transforming requirements to user stories, driving the class-level architecture of the software using behavior-driven development, driving the implementation using test-driven development, and evaluating both unit/regression test coverage and acceptance/integration test results. That is, rather than first evaluating students on requirements gathering, then on good design, then on development and finally on test coverage and a working demo, _all_ of these elements are evaluated on _every iteration_, encouraging the students to see the concepts and techniques as part of an integrated ongoing process rather than as isolated stages in a pipeline.

### Why Ruby and Rails? Why Not Java, C++, Python, or Scala?

We want students to understand that in the real world, programmers are rewarded not for the number of lines of code written or for how quickly they can "bash out" a feature, but for functionality delivered with high assurance of stability and while keeping the codebase beautiful and maintainable for continued growth. To many students, especially "hotshot" coders who come into a software engineering course with nontrivial programming experience, the methodologies and techniques we use to do this—design patterns, refactoring, test-first development, behavior-driven design—seem a strange and dubious use of time.

We have found that students are more likely to gradually embrace these practices if given the best possible tools to support the practices. The Rails community has created by far the most seamless, elegant, and comprehensive tool set to support Agile and XP, and the idea of constantly refining and inventing tools that support testing as well as helping produce beautiful application code is a distinguishing characteristic of the Ruby developer ecosystem. While learning Ruby and Rails will be new to most students, juniors and seniors seem to learn it without difficulty, and far superior tools outweigh the learning costs.

In other words, Agile and Rails were selected not because we expect them to dominate students' professional careers, but because their synergistic productivity allows us to fit several critical ideas and best practices into a single college course in the hope that students will later apply them to other methodologies, languages, and frameworks.

A common counterargument in academia is "Our curriculum already teaches language _X_, so upper-division courses should leverage that knowledge." We believe this approach optimizes for the wrong thing. First, software professionals are routinely expected to learn new languages by applying concepts from languages they already know, so "learning how to learn" new languages is a good skill to cultivate in class. Second, a language that makes it difficult to write and test beautiful and concise code is a poor vehicle for teaching those techniques, so the only investment being "leveraged" is syntactic knowledge, a hurdle surmounted with relative ease. Thus, even if our students never use Ruby again, they will have learned how to _reduce to practice_ such important ideas as metaprogramming, higher-order programming, functional programming, and use of closures in the service of higher productivity and more maintainable code. We believe these skills will transfer to new languages, framework, and programming systems. Our survey of alumni of the course that led to this book suggests that our belief is well founded.

### Why Cucumber Instead of Capybara + RSpec?

Another debate in the Rails community is whether scenarios should be written using Cucumber or by writing RSpec tests that call Capybara directly or using a Ruby-level tool such as Steak.

Since we believe it's critical for students to engage the customer, we want to get them accustomed to the fact that code is not the right medium for collaborating with the customer, so we insist on Cucumber scenarios.

### Why Imperative Scenarios?

In 2011, Cucumber's designer Aslak Hellesøy removed from Cucumber the step definitions that allowed writing Cucumber imperative scenarios "out of the box." Hellesøy called these steps "training wheels" since they were mostly thin wrappers around Capybara's API, such as "When I click on..." calling Capybara's `click`, or thin wrappers around assertions, such as "Then I should see..." calling `expect`. His rationale for removing the "training wheels" was that Cucumber scenarios should be higher-level and declarative, essentially serving as a per-application domain-specific language for user stories, whereas the low-level step definitions encouraged a lower-level imperative style of scenario.

Although we agree with his motivation, we chose to introduce Cucumber using the low-level steps anyway, because we felt that imperative scenarios provide a "kinder, gentler" introduction to this new tool precisely because of the small conceptual leap ("I'm scripting the user's actions on the browser UI"). Once the low-level scenarios are written, they can be used as subroutines in declarative scenarios. Indeed, step definitions that call other step definitions are arguably easier to read, for the same reasons we advocate sticking to a single level of abstraction within a method (one of the SOFA principles in Chapter 9).

### Knowing What You Don’t Know

Each chapter of the book covers a topic that could itself be the subject of many books. The challenge for a textbook author is what to leave out. Or, put another way: if the chapter on TDD is the _only_ material on TDD the student will ever encounter, what belongs in those \~40 pages? We describe enough to (hopefully) sketch the landscape and provide the basis for some learning by doing, but also indicate areas where much more detail would be possible, so that in the future the student will be aware that there is work in those areas (such as automatic test case generation and program synthesis) should they find themselves in situations where bringing those areas to bear would be useful.