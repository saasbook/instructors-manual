# Quizzes, Exams, Practice Problems

As of 2021, we’ve moved all summative assessments (quizzes/exams) and all non-CHIPS formative assessments (practice problems, practice questions not involving code-writing) to use the [PrairieLearn](https://prairielearn.org) (PL) assessment authoring system. Besides allowing us to create rich interactive exercises, PL allows randomizing elements of the questions, making them suitable for summative assessments as well as practice.

PL is open source and you can download and run it yourself (not trivial), or contact the nice folks at [PrairieLearn.com](https://prairielearn.com) to host it for you; they will usually offer a free trial period so you can try out the system for a semester before using it. **Disclaimer:** While we love PrairieLearn, we have no formal connection to PL so you'll need to contact them directly for support (except, of course, for bugs in the ESaaS questions themselves).

## How to get the ESaaS PrairieLearn content

See below for how PL organizes content for a course. In short, you'll need a GitHub repo representing your course, which you'll populate with questions and assessments.

Email Armando for a Zipfile that you can unpack that includes _most_ of our PL questions.

_Why can't I just clone your (Berkeley's) repo?_ Our repo includes at least some questions we'd like to keep private (so they don't escape into the wild) and a few files containing Berkeley-specific information.

## Overview of ESaaS Content in PL

The `questions/` subdirectory in the PL archive contains questions organized by chapter of the textbook. There are 3 broad categories of question types:

1. "Simple" questions that could be made to work with other (non-PL) platforms, such as:
   * multiple-choice or select-all-that-apply questions. In a few cases, the answer choices will be randomized in the sense that the choices displayed to the student (both the correct answer(s) and distractors) are drawn from a longer list of correct answers and distractors.
   * “Put these steps in order” questions, in which the students drag-and-drop a set of steps into a correct partial or total order. In a few cases, the steps shown will be a subset drawn from a longer list of possible steps (and distractors).
   * Short-answer/fill-in-blank/numeric answer questions, in which the answer must match a regular expression or fall within a numeric error of a correct answer. In a few cases, the specific numeric or string parameters in the question will be randomized.
2. **Practice questions** for topics such as constructing and parsing routes, writing regular expressions, and so on. Many of these questions feature randomization_._ For example, a question on database joins and Cartesian products will generate a set of random-but-plausible data constructed from a large corpus of real data each time the question is repeated. These could in principle be used on exams or quizzes to take advantage of the randomization, but are also excellent for practice.
3. **“Artisan” exam questions** that are more involved and appropriate for longer exams, but have little or no randomization.

## Per-Chapter Quizzes in PL

In the directory `courseInstances/TEMPLATE/assessments`, you'll find subdirectories `ModuleQuiz01`, etc. each of which contains a collection of suggested questions for reviewing that chapter grouped into an `infoAssessment.json` file. These are only suggestions!

## Questions Suitable for Skills Practice (formative assessments)

Some questions are particularly well suited to "skills building" because there's enough randomness that students can generate many question instances and get instant feedback while practicing the skill repeatedly. For example, the questions on regular expressions are like this. Using the PL UI, search for questions tagged "practice" to find more of these.

## Connecting questions to competencies

The latest version of the book (2.0b9) lists one or more _competencies_ associated with each chapter section. The file `competencies_map.<bookversion>.html` at the top level of the PL archive maps a subset of the competencies listed in the book to one or more PL question IDs (QIDs) that check that competency. We don't claim that the given questions are an exhaustive test of the competency, but it's somewhere to start to make sure you're getting the coverage you want on your summative assessments.
