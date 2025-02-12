# Development Practices

## Feature Communication Should be Handled in Github Projects

The issue summary should be used to easily identify what the story relates to (ex. implement performers endpoint, add oauth sso, etc ...)

If possibile, the description should include a detailed explanation of the business requirements as well as any preliminary documents or links that help team members understand what needs to be done.

### What Should be Included in Comments
* Questions relating to issue requirements
* Architectural diagrams
* Communication between developers (? and business stakeholders)
* Notes explaining blockers
* Notes explaining why additional work has been added to the issue after the issue is in progress
* Notes explaining time estimation changes
* Other important information that makes it easy for everyone to follow the issues's progression

## Github Conventions and Guidelines

Please read [this excellent article](https://chris.beams.io/posts/git-commit/) on commit messages and adhere to them. It makes the lives of those who come after you a lot easier.

### Branching

Branches should consist of one unit of work per branch and should comply with the following naming convention:<br>

**Regex:** `[a-z]+\/(rp)-\d+((-.*)*)`<br>

**Allowed Prefixes:** [module,feature,bugfix,task,release]<br>

**Examples:**

* module/user-orders-module-implementation
* task/update-opam-dependencies
* feature/new-user-account-verification-email
* bugfix/search-returning-incorrect-matching-results-from-cache

### Pull Requests

Pull requests should comply with the following naming convention:

**Regex:** `(ISSUE REF #)-[0-9]{1,5}: <description>`<br> or branch name, when no issue is associated.

**Merging Strategy:**

Devloper Branches => dev(Beta) -> staging(Stage) -> master(Prod)

* Feature branches get squash merged into Dev
* Stage gets a standard a merge commit into and master

**Examples:**

* 3: My new feature
* 15: Bugfix for bad config
* Module/User Orders Module Implemenation

#### Template Sections

**Describe Your Changes:**

An overview should be provided at a high feature level.

**Changelog:**

The changelog should include any technical changes made as a result of the feature being reviewed. A full technical explanation is not required. However, the changes should be lined out in enough detail that the it can be identified and referred to in the future.

**Github Issue Tickets(s):**

A list of both the Github issue # directly related to the request as well as any relevant issues should be included to provide context around what functionality is being added, changed, or affected.

**Related Pull Requests:**

This section will detail any dependent pull requests or pull requests that might otherwise be affected once the requested branch is merged.

**Note:** PRs can be referenced using Github Links by starting with a `#`

**Screenshots:**

This section should include any relevant screenshots or GIF’s that will help communicate changes to the UI

### One Commit Per Week

Team members should commit AND push their work a minimum of once week before standup(the more the better). Incomplete, barely readable, and utterly nonsensical code does not have immunity from this requirement. We are not here to judge your code, we are here to get things done. It is important to get our work off of our machines as often as possible. Frequent commits also helps keep everyone up to date on our current works in progress. It's better to see a half-built car on the line than no car at all.

## Communication Guidelines

* Sound the alarms and comment in Github as soon as you run into a blocker
* Communicate early, communicate often



*We can only see a short distance ahead, but we can see plenty there that needs to be done. - Alan Turing*
