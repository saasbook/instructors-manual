# Managing Heroku apps & teams

In 2022, Heroku eliminated their free plan, making it impossible for students to deploy simple ESaaS CHIPS to Heroku without paying a fee.

Heroku/Salesforce is very generous about working with instructors. Although they have a [student program](https://www.heroku.com/students), you may find it easier to contact them to set you up as an instructor by having a special [Heroku team](https://devcenter.heroku.com/articles/heroku-teams) in your account that is used for student coursework. Students still create their (free) Heroku developer accounts, but you can add and remove apps and associated collaborators on your course-related "team" and have those apps centrally billed, and make an arrangement with Heroku to have those charges covered as long as the apps are course-related and you agree to be responsible for the actions of anyone who joins that team.

To make it easier to manage the team, look at [`scripts/heroku-apps`](https://github.com/saasbook/courseware/tree/main/scripts/heroku-apps)for a script that lets you bulk-add and bulk-remove students and apps from your Heroku course-linked team. Its `README.md`has more details.
