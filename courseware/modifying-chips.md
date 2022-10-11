---
description: Making content and autograder changes to individual assignments
---

# Modifying CHIPS

## The CHIPS Monorepo

All CHIPS are kept in a single private repo (the "[monorepo](https://github.com/saasbook/chips)"; instructor verification required for access, but most instructors shouldn't need it). The repo has workflows that do the following whenever a CHIP is modified or added:

1. Automatically (re-)generate a student-facing public template repo containing starter code and such, that the student can make a copy of and pull into Codio or clone locally
2. Automatically generate Codio "guides" pages corresponding to the scaffolding
3. Run validations to try and ensure code correctness.
4. Push the necessary changes to the ESaaS Template course in Codio, including any guides pages, changes to the autograder script, etc.

{% hint style="info" %}
Note: the old individual _hw-\*-ci_ repos are deprecated. The monorepo contains everything needed for every CHIP—starter code, guides/scaffolding, reference solution, Codio autograder files.
{% endhint %}

## Setting up the Monorepo

The monorepo requires the following dependencies.

* [pre-commit](https://pre-commit.com/#installation)
* [rvm](https://rvm.io/rvm/install)
  * Ruby version 3.0.2 & 2.6.6
* A handful of bundled gems (run `bundle` once cloned)

Alternatively, you could use a Codio [pre-made environment](https://codio.com/home/stacks/95ca5e5b-a3ef-4086-b745-a4093a455351?tab=details) that comes with these deps installed. Installing Ruby 2.6.6 might be difficult on M1 mac's. This is not a problem if you are making content changes and not code changes. If making code changes, developing locally might be hard without it, but doable if you are confident enough. Hopefully, the verification flow can catch any egregious errors.

## Reporting Problems with CHIPS

Open an issue against the monorepo. Label it with the CHIP no and assign it to the proper person.

## Editing an Existing CHIP

**Scaffolding (Codio guides).** In the CHIP's subdirectory, `scaffolding/content/README.md` is the "root" of the scaffolding; you can also link to additional scaffolding `.md` files that you place in the same directory.&#x20;

**"Submit" button.** The `submission-xxx.md panel is a "Submit & grade"`button. The `xxx`  must match what is referenced in `book.json` or `metadata.json`

**Assignment settings.** The JSON files encode assignment settings such as stacks, submission metadata, etc., but these are best changed manually using Codio's UI (see "Codio course organization"), and then copying the new JSON settings wholesale into these files.

**`chip_config.yml`**.  Assignments are detected via the presence of this file. The `codio_id` value must match Codio's assignment ID in the TEMPLATE course. The `public_repo` is the URL of a public repo that will be overwritten by auto-generated files when you publish your changes. Note, when adding new chips, only one of these is required. That means you need to opt-in to publish flows (Codio/starter). Note, to publish to a public facing repo, our [bot](https://github.com/orgs/saasbook/people/cs169bot) must be added. This should rarely be modified, and is mainly important for adding new or legacy chips.

**Auto-generated files.** In the root of a chip directory you will find 2 file (`build_codio.json` & `build_starter_files.json`). These 2 files are responsible for defining the generated code. This is because we want to reuse most of our `/solution` code and typically only substitute the files we want students to fill in with the `/starter_code`. The Codio flow has similar logic with the `scaffolding` directory. These are the single source of truth for what get publish and what doesn't. Read them carefully, as the above is an ideal case and sporadically implemented. The parser is very simple and can be found in `lib/parser.rb`. For further details and edge cases, view the `spec/parser_spec.rb`. Don't touch the `gen` subdirectory, as it contains files that will be overwritten by the generator. This is validated by pre-commit, so you won't be able to commit or merge your changes anyway.

## When you're ready to publish

`bundle exec rake assignment:gen chip=3.7` (or whatever CHIP number, based on subdirectory name) generates the derived files in `gen`. Alternatively, you can run `pre-commit run` and `git add` any changed files. Then commit and open a PR. PR's require a review. Please conform with style a **squash** your commits before merging a PR. **Reviewers** should focus on all files changed in the `/gen` directories. Pay careful attention to make sure solutions aren't being leaked. That was one of the driving forces behind implementing the monorepo.&#x20;

When the PR is merged, a Git workflow will publish the new public repo, push the necessary changes to the Codio TEMPLATE course only, including new guides, autograder files, etc.

Login to Codio and **your** course instance,  click the pencil <img src="https://lh5.googleusercontent.com/MHNLd79XBFTrK04Ywui2l-J5CoN4otKCIfRA541kiwsRZcP3DqCr2oT5PSVarfYKruY7yYGTt_WL-h40N4n10KAPYdXOqz3hAFsfd2lAGQSzXxfAqjbJ2-xN_CawAXYIq_VryH0uOd4aZ6nznjaJSS57ILMSCh0SCQGnyVeZf1aHoR4SSmKe4Xnc" alt="" data-size="line"> to go to Teaching Mode to edit assignments, and click the "pull" (refresh) button on any assignment that has one.

You must Publish from course overview page; "content only" just updates the content, "content and stack" also replaces the stack (but see "Codio Course Organization" at left—it's probably better to modify the stack using the Codio GUI and reflect the corresponding changes to the JSON files here).
