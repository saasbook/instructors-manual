# Modifying CHIPS

## The CHIPS Monorepo

All CHIPS are kept in a single private repo (the "[monorepo](https://github.com/saasbook/chips)"; instructor verification required for access, but most instructors shouldn't need it). The repo has workflows that do the following whenever a CHIP is modified or added:

1. Automatically (re-)generate a student-facing public template repo containing starter code and such, that the student can make a copy of and pull into Codio or clone locally
2. Automatically generate Codio "guides" pages corresponding to the scaffolding
3. Push the necessary changes to the ESaaS Template course in Codio, including any guides pages, changes to the autograder script, etc.

{% hint style="info" %}
Note: the old individual _hw-\*-ci_ repos are deprecated. The monorepo contains everything needed for every CHIP—starter code, guides/scaffolding, reference solution, Codio autograder files.
{% endhint %}

## Reporting Problems with CHIPS

Open an issue against the monorepo.

## Editing an Existing CHIP

**Scaffolding (Codio guides).** In the CHIP's subdirectory, `scaffolding/content/README.md` is the "root" of the scaffolding; you can also link to additional scaffolding `.md` files that you place in the same directory.&#x20;

**"Submit" button.** The `submission-xxx.md panel is a "Submit & grade"`button. The `xxx`  must match what is referenced in `book.json` or `metadata.json`

**Assignment settings.** The JSON files encode assignment settings such as stacks, submission metadata, etc., but these are best changed manually using Codio's UI (see "Codio course organization"), and then copying the new JSON settings wholesale into these files.

`chip_config.yml`. The `codio_id` value must match Codio's assignment ID in the TEMPLATE course. The `public_repo` is the URL of a public repo that will be overwritten by auto-generated files when you publish your changes.

**Auto-generated files.** Don't touch the `gen` subdirectory, as it contains files that will be overwritten by the generator.

## When you're ready to publish

`bundle exec rake assignment:gen chip=3.7` (or whatever CHIP number, based on subdirectory name) generates the derived files in `gen`. Then commit and open a PR.

When the PR is merged, a Git workflow will publish the new public repo, push the necessary changes to the Codio TEMPLATE course only, including new guides, autograder files, etc.

Login to Codio and **your** course instance,  click the pencil <img src="https://lh5.googleusercontent.com/MHNLd79XBFTrK04Ywui2l-J5CoN4otKCIfRA541kiwsRZcP3DqCr2oT5PSVarfYKruY7yYGTt_WL-h40N4n10KAPYdXOqz3hAFsfd2lAGQSzXxfAqjbJ2-xN_CawAXYIq_VryH0uOd4aZ6nznjaJSS57ILMSCh0SCQGnyVeZf1aHoR4SSmKe4Xnc" alt="" data-size="line"> to go to Teaching Mode to edit assignments, and click the "pull" (refresh) button on any assignment that has one.

You must Publish from course overview page; "content only" just updates the content, "content and stack" also replaces the stack (but see "Codio Course Organization" at left—it's probably better to modify the stack using the Codio GUI and reflect the corresponding changes to the JSON files here).
