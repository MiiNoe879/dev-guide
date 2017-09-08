# Development Best Practices
This guide summarizes best practices we have developed and should be followed for all projects.

## 1. General
- Communication is key and avoids lost time. If anything is unclear, ask for clarification in the right place. After some work was done, send a short summary, so we know the current state. Problems, delays and unexpected issues should be communicated as well.
- Do the required research before writing code. How will the change integrate with the existing code? Any libraries already being used that can solve this problem? What's the overhead when adding a new library?
- Keep `README.md` updated. This file should at a minimum have a short description of the project, what it does, how to install and how to build it. This will help us learn faster and avoids having to solve the same problem more than once.

## 2. Git Usage
`git` version controlling provides a way to collaborate on complex code bases, while documenting all changes. Here some general tips and the workflow we are using.

### 2.1 Issues
We use Github issues to structure changes that need to be applied to code. Often they will have a checklist and further details on how to implement the feature. New information or clarifications should be added to the issue directly, even if details were discussed somewhere else. Some useful tips on working with issues:

- When commiting fixes for issues directly to the master/stable branch, [reference the issue](https://github.com/blog/957-introducing-issue-mentions). E.g. `Change sidebar behavior and title #33`. When working on a feature branch, this is not necessary because the commits will be summarized later anyways.
- When done, immediately push your changes, so others can keep working on them. Be sure to add new files.
- Before starting work, pull the latest changes from the repo. Use `git log` and `git show <commit ID>` to see what has happened. This also avoids merge conflicts later.


### 2.2 Feature branch workflow
We follow the [feature-branch workflow with interactive rebasing](https://www.atlassian.com/git/tutorials/comparing-workflows#feature-branch-workflow). The rough steps are:

- Create new feature branch. Use a distinct name and mentione the issue it will address. Like `git checkout -b issue/120-twitter-sidebar`.
- Add commits as usual. 1 significant change = 1 commit.
- When most work is done, do interactive rebase with master (or other stable) branch: `git rebase -i master`. This will allow you to summarize multiple commits and clean up your work.
- When the new feature is tested, reviewed and approved, merge into master-branch (after `git checkout master`): `git merge issue/120-twitter-sidebar`

## 3. Coding Style
- Where feasible, the coding conventions for that particular language should be followed.
- Use white-space. It doen't add real overhead and makes your code much easier to read later. Code is only written once, but read often.

## 4. Payment
For payment, an invoice is required from you. There are free tools to quickly generate invoices. E.g. https://invoice-generator.com/#/3

Add your own details and the company details you received. Then description of the project and work done and your bank details.
