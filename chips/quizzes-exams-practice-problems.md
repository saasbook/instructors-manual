# Quizzes, Exams, Practice Problems

As of 2021, we’ve moved all summative assessments (quizzes/exams) and all non-CHIPS formative assessments (practice problems, practice questions not involving code-writing) to use the [PrairieLearn](https://prairielearn.org) (PL) assessment authoring system. Besides allowing us to create rich interactive exercises, PL allows randomizing elements of the questions, making them suitable for summative assessments as well as practice.

PL is open source and you can download and run it yourself (not trivial), or contact the nice folks at [PrairieLearn.com](https://prairielearn.com) to host it for you. **Disclaimer:** We have no formal connection to PL so you'll need to contact them directly for support.

## Overview of ESaaS Content in PL

There are 3 categories of content we've created for use in PL, all autograded within PL itself:

1. Per-chapter **quizzes** that test basic knowledge. These consist primarily of:
   * multiple-choice or select-all-that-apply questions. In a few cases, the answer choices will be randomized in the sense that the choices displayed to the student (both the correct answer(s) and distractors) are drawn from a longer list of correct answers and distractors.
   * “Put these steps in order” questions, in which the students drag-and-drop a set of steps into a correct partial or total order. In a few cases, the steps shown will be a subset drawn from a longer list of possible steps (and distractors).
   * Short-answer/fill-in-blank/numeric answer questions, in which the answer must match a regular expression or fall within a numeric error of a correct answer. In a few cases, the specific numeric or string parameters in the question will be randomized.
2. **Practice questions** for topics such as constructing and parsing routes, writing regular expressions, and so on. Many of these questions feature randomization_._ For example, a question on database joins and Cartesian products will generate a set of random-but-plausible data constructed from a large corpus of real data each time the question is repeated. These could in principle be used on exams or quizzes to take advantage of the randomization, but are also excellent for practice.
3. **“Artisan” exam questions** that are more involved and appropriate for longer exams, but have little or no randomization.

## Per-Chapter Quizzes in PL

PL content is structured as a _course repo._ This repo can contain a collection of _questions_ organized hierarchically and a collection of _assessments._ An assessment is a group of questions together with grading information: whether single or multiple attempts are allowed, whether there is a time limit, and so on. A single assessment is represented by an `assessment.json` file.

## Getting Started With PL
