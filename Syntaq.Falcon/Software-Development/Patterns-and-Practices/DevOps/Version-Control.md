We use Git as our form of version control. Generally speaking, the software development process will follow this general pattern:

#Workflow
* New issue is created on DevOps for a new feature/bug
* Create a new branch for the feature/bug
* Commit changes for that feature/bug to that new branch

Need to agree what the next steps in the process are for this...
* Once complete, submit a pull request to merge that branch into the master branch
* If approved, the changes will be merged into the main branch
* If not approved, fix the raised issues and ping the reviewer/resubmit the pull request.

#Branches 101
While for larger features it is preferable to have a separate branch for each feature to keep things manageable, it is not a requirement that every issue needs it's own branch. For example, if there are a several minor bugs, it is perfectly acceptable to fix them all within the same branch rather than creating 5 different branches.

**Exercise reasonable judgement here.**

Branches should be named sensibly. For large features / feature specific branches, they should be named in the form ```xxx-some-description``` where ```xxx``` is the DevOps ID number. For non-feature specific branches, the branch should be named sensible so that it is easy to discern its purpose.

If you are experimenting with things and require a branch to store your progress, it is preferable to name the branch with the format ```<your-initials>/some-description```. This ensures that it is clear who the branch belongs to, and who to ask should it become stale.

#Commits
Generally it is preferable to keep commits focused and relatively small. This makes it easier to find commits where things may have been changed, and keeps things easier to review.

A notable exception to this is if there are sweeping refactoring changes that need to be made, e.g. fixing formatting of many files in the codebase, in this case it is preferable to have this in a single commit so that other changes do not get hidden in the sea of unrelated changes.

#Commit messages
Commit message are generally of the format:
```<type>(<category>): <short-description>```

For example, if a new feature is being developed for Projects, a commit for those changes would be something like:
```feat(projects): implemented this and changed that for projects```

Whereas if there was a bug in the Document Templates function, then a commit that fixes that bug might be something like:
```fix(document templates): fixed issue with versioning```

The short description should be a concise summary of the change. A longer description may be entered as the "description". This is another reason to keep commits focused and relatively small.

Having indicators of the type and category makes it easier for us to find where things have been changed. The short description further helps us locate changes that impact a specific function of the system should we ever need to.

Consider an alternative scenario where commit messages were generally along the lines of:

```* updated projects```
```* updated```
```* updated document templates```
```* fixed```
```* updated projects, document templates and changed layout```

Finding where something was changed would be much more difficult.