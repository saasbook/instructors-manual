# Supporting course operations

ESaaS was developed and is actively taught at [UC Berkeley](https://www.cs.berkeley.edu), where we routinely deal with very large course enrollments.

So we developed a handful of scripts to support operating an ESaaS course at large scale (many hundreds of students), which you'll find in the GitHub repo [esaas/courseware](https://github.com/esaas/courseware). The following pages describe how to use them.

In general, these scripts understand that ESaaS includes both individual student work and team projects. Therefore, for example, the Heroku script can create or delete Heroku app containers both for each student and one per team, plus access for course staff; the GItHub script can manage repos by organizing access according to teams, plus access for course staff; and so on.

**Contributions of additional scripts are welcome,** in the form of pull requests creating a new subdirectory under `scripts/` in the above repo!
