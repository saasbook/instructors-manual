# Coding Exams

{% hint style="warning" %}
We're in the process of moving these to Codio and will make them available as part of the Codio resources for instructors using Codio. The tools described below for running these exams are no longer supported, though the questions (and solutions) themselves may still be useful.
{% endhint %}

We've given exams where part of the exam is spent writing actual code. We have developed an infrastructure for doing this that allows students full read-only access to the Internet via Google's cache, so they can look up any existing information they want but cannot post a question or send email/messages to ask for the answers. However, you can also use these as homework assignments since they include test cases.

The repos contain solutions and test cases as well as questions; instructions are provided in each repo's `README-instructor.md` for creating just the student-facing part of the package.

In our setup, since the questions are multiple parts with later parts building on the results of earlier ones, each question subpart is associated with a hint and/or with the answer (i.e. code that if copy-pasted in the right place will solve that subpart). Students can "reveal" these hints if they accept a penalty of a substantial fraction of the points the exam question is worth. The hints are part of each repo; our [reveal](https://github.com/saasbook/reveal) script is installed in the exam environment (described in this paper to record which hints were used and calculate the penalty. We [found](https://dl.acm.org/authorize?N680629) that weaker students do not request more hints than stronger students, even though they would sometimes benefit more from doing so; weaker students are more likely to request hints on lower-scoring coding questions than higher-scoring ones; and all students are equally well able to use hints once provided.

* [Interview Scheduler](https://github.com/saasbook/exam-interviewscheduler-associations): Modify an existing app to add the correct associations among Interviews, Candidates, and Recruiters. Factor out some common code among the models and mix it back in, to DRY out the code. [Solutions](https://github.com/saasbook/exam-interviewscheduler-associations-ci)
* **(Incomplete)** [Ruby Iterators](https://github.com/saasbook/exam-ruby-iterators) Create Ruby iterators for a new `Matrix` class.
* [Can I Stream It?](https://github.com/saasbook/exam-rottenpotatoes-canistreamit) Enhance RottenPotatoes by adding a view that displays information retrieved from the `CanIStream.it` API.
* [Encryption Demo](https://github.com/saasbook/exam-encrypty) Create this [simple app](https://encrypty.herokuapp.com/) ([source](https://github.com/saasbook/encrypty)) that allows users to specify a key for symmetric encryption and to encrypt/decrypt text with that key.
