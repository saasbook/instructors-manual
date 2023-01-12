# Codio Course Organization

There is a Codio course called **ESaaS 2020 (TEMPLATE)** that is a parent of any given semester's offering of CS(W)169(A) and also the parent of all the edX courses. It may also be the parent of other instructors' instances of the ESaaS course. (There are lots of ESaaS child courses owned by other instructors at other institutions; you can only see the courses you own.)

Changes made in the TEMPLATE course can be "pulled" into children, but not vice versa. So "permanent" changes/fixes to course materials should be made in the TEMPLATE course and then disseminated.

{% hint style="info" %}
(Because a child course is allowed contain a subset of the parent course, each of the three edX courses is a separate child course owned by Berkeley EECS, with 2/3 of the content removed.)
{% endhint %}

## Caveat about configuring LTI for Codio

If you're using another LMS to communicate with Codio via LTI, be aware that Codio autograder grades will _not_ be reported back to the LMS until the student clicks "Mark as complete" in Codio, and in our experience students often forget to do this and are then confused when all their tests pass in Codio but the LMS shows a zero (or no grade) for the assignment. "Mark complete" also has the effect of making that assignment read-only for the student, and if they want to modify their solution before the deadline, you have to manually re-open the assignment for them. An alternative is to use the Codio setting "Disable 'Mark as Complete'" for each assignment, and then as an instructor, use "Mark all as completed" after the assignment deadline passes; then the student can modify the assignment right up until the deadline, and whatever grade they have at that instant becomes the recorded (via LTI) grade when you click Mark All as Completed.

## Modifying or creating an assignment

To change the **content of a CHIP,** modify the Git repo (see "[Modifying CHIPS](modifying-chips.md)").

## Changing the stack used by an assignment

In general, we **do not use** the "certified" Codio stacks. As of Spring 2021, use the stack called "**ESaaS with Gradescope and rvm wrapper**", which is also the default stack for the course.

{% hint style="info" %}
Remember that a stack's Ruby version and Bundler version (at least) need to be consistent with the `Gemfile` and `Gemfile.lock` for the assignment(s) using that stack, or it will create extra steps when starting the assignment.
{% endhint %}

{% hint style="info" %}
Codio stacks are maintained as Ansible playbooks. [This video](https://youtu.be/VWNX0VN0vjE) steps through how to create a stack on Codio from an existing Ansible playbook.
{% endhint %}

To change the **stack used by a CHIP,** it's easier to do it interactively in Codio. If you change the TEMPLATE course, the changes can easily be made available to child courses; if you change a child course, the changes will only be in that course.

1. In the TEMPLATE course or child course, open the desired assignment.&#x20;
2. Manually make any changes to the stack using `sudo apt-get install`, etc.&#x20;
3. When ready, go to **Project > Stack… > Create New…** This will create a new stack based on the existing state of the VM. The stack does not capture stuff in the `.guides` folder or the student-visible `~codio` folder, just the system stack.&#x20;
4. If changing the **TEMPLATE** course, indicate that the new stack should be owned by the `Berkeley EECS` org.&#x20;
5. Once stack creation is done, go to **Project > Stack > Settings…** and ensure this new stack is selected as the project's stack, and that **Use Latest Version** is selected, so that all assignments using that stack will use the latest version.
6. Select **Education > Publish**.

{% hint style="info" %}
For students who have started the assignment - when the stack is modified, student code will not be affected. Specifically, any files outside of the `.guides` directory (which is invisible to students) will be unaffected. But if they installed other stuff using `sudo` etc. in their stack, that **will** be wiped if the stack is changed.
{% endhint %}

## Distributing changes to child courses

1. Go back to Courses list and select the current semester's offering of the course (or whichever course(s) you want to distribute the changes to).&#x20;
2. Scroll down to the CHIPS whose stack you changed and click the "Pull" icon—this updates the staged assignment from the parent course.
3. Once pull is done, click Publish. (NOTE: If the assignment has never been opened before in this child course, you may need to open it first, then return to this page and Publish.)&#x20;
4. Repeat for any other child courses, e.g. the edX MOOCs, to update them.

## Optional: Notify Others

Notify Elise Deitrick at Codio in case she wants to announce to other instructors (owners of child courses) in case they want to pull in the changes.

Notify **esaas-instructors@googlegroups.com** that the assignment(s) have been updated to use a new stack. They will need to "pull" from the TEMPLATE course if they want those changes in their own course.
