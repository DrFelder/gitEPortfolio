# Git and GitHub - Handout
## Git
#### What is Git?
Git is a filesystem at heart. 
Git provides a version control system.
#### What is a version control system?
A version control system lets you manage different versions or changes made to documents, code or other collections of information.

#### Git history
Git has been created in 2005 as a successor of BitKeeper for the Linux kernel developers to use during development. 
After BitKeepers free use had been restricted, Linus Torvalds decided to create his own version control system.
Since then, Git has become the overall industry standard.
Torvalds focus laid mostly on a BitKeeper-like Workflow, speed and security.

#### Git areas
In Git, there are three important areas that you should know:

- The working directory:    Contains all your current files and changes.
- The staging area:         Contains all the files and changes that will be part of the next snapshot/commit.
- The repository:           Contains all your commits, all your branches, files, etc.

#### Basic usage
Basic usage is fairly easy.
Once you created or cloned a repository, you can change the files and do some work.
After that, stage whatever changes you want to have as a part of the next version.
Commit to create a new version.
- `git init`:                       initiate a new Git repository. Creates the famous .git folder.
- `git clone <repository URL>`:     downloads a copy of a repository, and sets its remote to the repository that has been cloned.
- `git status`:                     gives valuable information on the current status and the staging area as well as unstaged changes, the current branch etc.
- `git add <file to add>`:          adds the file to the staging area.
- `git commit`:                     creates a new commit object that points to a snapshot of the project. Everything that has been staged is now part of your repository.
- `git push`:                       sends the changes to the remote repository.

Git is famous for its branching.
Branches make it possible for multiple people to work on one project, or to have multiple concurrent versions.
Merging adds the commits of another branch to the HEAD.
- `git checkout -b <new branch name>`:      Create a branch and check it out afterwards.
- `git merge <branch>`:                     Merge a branch into the current HEAD.
If you changed the same part of a file in two branches that you want to merge together, you will encounter a merge conflict.
Git will mark parts in your file where you will have to decide which version results the merge of the two branches.
It will look like this:
```
<<<<<<< HEAD
# This is the HEADs current version
=======
# This is the version of the branch you are trying to merge into the HEAD
>>>>>>> FixingClangFormatSpelling
```
Use your favorite editor to select one of the lines, save the file, stage the file and continue merging by entering `git commit`.

#### Advanced usage
- `git stash`:                              Clear your staging area and stash away your changes.
- `git stash apply`:                        Apply the stash you created.
- `git commit --amend`:                     Amend something to the previous commit.
- `git cherry-pick <commit>`:               Apply a commit to your current branch.
- `git revert <commit>`:                    Revert a commit that you made.
- `git rebase -i`:                          Use the interactive rebasing to rename or squash previous commits etc.
- `git tag -a <version> -m "<message>"`:    Create a tag.
- `git log --graph`:                        Get a fancy version of the git history.

#### Best Practices
Commit whenever you have finished a subtask or a set of similar, small tasks. 
Mark commits as `WIP` if they aren't functional or if they won't provide any help later on.
Try to squash `WIP`-commits into previous commits to keep the master clean.
Choose a short, understandable and precise commit message.

Create a branch for every task you want to work on.
Throw away old branches that are already merged.
Choose a short, understandable UpperCamelCase name for each branch.

#### What to avoid
- Do not spend too much time on Git!
Managing a repository is probably not your job description.
- Do not rely on Git!
Most problems are user-generated. Git won't help you out on it's own if you mess up.
- Do not use Git repositories for backups or file storage. There are tools built for those use-cases. 

## GitHub
#### What is GitHub?
GitHub is a service that hosts Git repositories.
GitHub is free to use, but there are some premium features (private repositories etc.).
Early on GitHub laid its focus heavily on collaborative developing.
GitHub adds some features to the basic Git workflow that you can use to get on with your project:
- Wikis
- Issue tracking
- GitHub Pages (basically free websites)
- Statistics, graphs on repositories and users
- Git Gists (code snippets)
- Pull requests
- CI

GitHub Issues is basically a bare minimum issue tracker.
It is good enough to manage user-submitted bugs etc.

Pull requests are a common feature amongst repository hosting services (e.g. GitLab).
If you want your branch merged into another branch, you can create a pull request.
The repository collaborators will be able to review your changes and merge the branch.

#### How to use GitHub?
Create an account over at [GitHub](https://github.com/), and that's basically all there is to it.
So get an account and get started!

## More information
To get some more information on Git, have a look at the [references](references.md).