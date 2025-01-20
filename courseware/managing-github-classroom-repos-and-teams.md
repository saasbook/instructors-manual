# Managing GitHub Classroom Repos & Teams

The [`scripts/github-repos`](https://github.com/saasbook/courseware/tree/main/scripts/github-repos) script manages the creation, deletion, and access of GitHub repos for both individual students and teams, for those classes using GitHub Classroom.\
Specifically, given a list of students' email addresses/GitHub usernames and which team number each student belongs to, the script creates/destroys a GitHub repo accessible to all (and only) the members of that team, plus the course staff, for team projects such as CHIPS 10.5 or for an open-ended team projects course.

This works with either GitHub Classroom or a regular non-Classroom GitHub org of which the course staff is/are the owner(s)/admin(s).
