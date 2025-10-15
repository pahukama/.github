# Development Practices

## Feature Communication Should be Handled in Github Issue Projects & Pull Requests

The issue summary should be used to easily identify what the story relates to (ex. implement performers endpoint, add oauth sso, etc ...). If possibile, the description should include a detailed explanation of the business requirements as well as any preliminary documents or links that help team members understand what needs to be done.

##### Although there are Github actions that will be assisting the process, each developer is ultimately responsible for managing the status of issues they are assigned. Keeping them as up to date as possible will always make it as clear as possible what your working on, this is critical in a remote/distributed team.


### What Should be Included in Comments
* Questions relating to issue requirements
* Architectural diagrams
* Communication between developers (? and business stakeholders)
* Notes explaining blockers
* Notes explaining why additional work has been added to the issue after the issue is in progress
* Notes explaining time estimation changes
* Other important information that makes it easy for everyone to follow the issues's progression

## Branching

Branches should consist of one unit of work per branch and should comply with the following naming convention:<br>

**Regex:** `^(feature|fix|task|refactor|revert){1}(\([\w\-\.]+\))?(!)?: ([\w ])+([\s\S]*)`<br>

**Allowed Prefixes:** [feature,fix,task,refactor,refactor]<br>

**Examples:**

* feature/user-orders-module-implementation
* task/update-opam-dependencies
* refactor/new-user-account-verification-email
* fix/search-returning-incorrect-matching-results-from-cache

#### After making at least one one commit, you can push it your branch upstream. Github will recognize correctly formatted branch names and generate a pull request draft with a template filled out for you. It is recommended to check in as soon as you have some commits to track your work.

## Pull Requests

Pull request names must comply with the [convential commit](https://www.conventionalcommits.org/en/v1.0.0/) standards, as the rest of your PR makes up the commit into ```main```.

**Merging Strategy:**

Devloper Branches => main(Staging) -> master(Production)

* Feature branches get squash merged into Dev
* Stage gets a standard a merge commit into and master

**Automated Checks:**

Github actions run automated checks on PRs to make sure they're good to go. Review request actions triggered when you transition a draft PR to open, and once a PR is approved CI/CD actions will run for the final step.

* Branch Names
* PR Name
* CI/CD: Unit/Integration Tests, Linting, and a Coverage Report in the comments
* CODEOWNER approval

### Template Sections

**Describe Your Changes:**

First part of your PR, an overview should be provided at a high feature level. Possibly including a summary of the issue/story/bug being worked on.
##### Good to include include the issue # as well.

**Current behavior:**

In this section we want to capture important details about the applications current behaviour, mostly relevant when dealing with fixes, refactors, or targeted feature enhancements.

**New behavior:**

Go over the new behaviour this PR introduces, good place to highlight any relevant technical details to be reviewd.

**Testing:**

Unit? Integration? E2E? Sanity checks? Testing that needs to be done after deployment?

**Breaking PR:** 

Is this going to break something somewhere? Are you sure? Do we mean to do it? Check again!

**Checklist:** 

Crossing our i's and dotting our t's.

## One Commit Per Day / One PR per week (or 2)

* Team members should attempt to commit their code once per day (or each day they write code). Incomplete, barely readable, and utterly nonsensical code does not have immunity from this requirement. We are not here to judge your code, we are here to get things done. It is important to get our work off of our machines as often as possible. Frequent commits also helps keep everyone up to date on our current works in progress. It's better to see a half-built car on the line than no car at all.

* And ideally team members should aim to submit a PR every 1-2 weeks. This is less about feature/development velocity and more about maintaing an [iterative and incremental development](https://en.wikipedia.org/wiki/Iterative_and_incremental_development) process. So meeting this requirement is more about actively breaking down issues into small code changes that are easier to test, review, and verify.

## Communication Guidelines

* Sound the alarms and comment in Github as soon as you run into a blocker
* Communicate early, communicate often

***
##### *We can only see a short distance ahead, but we can see plenty there that needs to be done. - Alan Turing*
