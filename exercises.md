# Git and GitHub - exercises
## 1 Git
These exercises should take you 15-20 minutes to finish.
### 1.1 Committing
Let's start with the basics!
#### 1.1.1
- Create a repository using GitHub.
- Clone the repository.
#### 1.1.2
- Add a file to the repository. Call the file `clang-format`.
- Fill the files with these lines:
```
# This file is an example configuration for clang-format 5.0.
#
# Note that this style definition should only be understood as a hint
# for writing new code. The rules are still work-in-progress and does
# not yet exactly match the the style we have in the existing codee.

# Use tabs whenever we need to fill whitespace that spans at least from one tab
# stop to the next one.
UseTab: Always
TabWidth: 8
IndentWidth: 8
ContinuationIndentWidth: 8
ColumnLimit: 80
```
#### 1.1.3
- Stage the file and commit it. You can add the following commit message:
```
added clang-format
```
#### 1.1.4
There seems to be a mistake in the file.
- Fix the duplicate "the" in line 5
- Stage and commit the files

### 1.2 Branches
You will now get into branching.
- Go ahead and check out the first commit you made to the repository.

    **HINT**: You can check out a commit by using it's commit hash instead of a branch name.
    
It seems like the original file contained another mistake at line 5.
- You want to fix a mistake inside the file, so think of a good branch name, create a new branch and check it out.
#### 1.2.1 
- Change the "codee" at line 5 to "code"
- Stage and commit your changes

Take a look at the history, you will already see some commits!
#### 1.2.2
You've just fixed a major mistake in the file.
The correction should be part of the master branch, don't you think?
- Check out the master branch
- Merge the branch you created into the master
- Explain what is happening using your own words. If you are having trouble, try to draw a history containing both branches and all the commits.
#### 1.2.4
Time to clean this mess up!
- Fix the merge conflict you created
- Finish the merge
### 1.3 Pushing
- Push your repository to the remote. Take a look at it at GitHub to see if it worked.
Take a look at the history, a lot has changed over there...
## 2 GitHub
Now that you are a Git expert, you want to spread the word by improving other people's projects. 
### 2.1
- Find a partner to do the following exercises with:
- Add your partner as a collaborator (Settings -> Collaborators -> add him as collaborator) to the repository you created earlier.
- Clone the repository your partner created. It should look quite familiar.
### 2.2
It seems like your partner is trying to be silly. He set the TabWidth to 8 in the `clang-format` file!
- Add an issue to your partners repository describing the problem:
```
Title:      TabWidth too small
Comment:    The TabWidth should be set to 32. A TabWidth of 8 is too small for a clang document.
```
While your partner is working on something else, you will just fix his mistake yourself.
- Create and checkout a branch, give it a meaningful name.
- Edit the file so that the TabWidth is correct.
- Commit your changes.

    **HINT**: You can close the issue by adding `closes #<issue ID>` to your commit message.
    
- Close the issue.
### 2.3
- Push your changes to the remote.
- Create a pull request for the branch you just created.
### 2.4
- Wait until your partner is finished with the exercise. You should receive a pull request.
- Review the changes your partner made to your files.
- Accept the merge request your partner proposed to you if you think his changes improved the file.
## 3 Best practices
- Describe how you would handle the following situations (describe the branches and commits that you would create):
    - It is monday, and the project owner tells you to do the following:
        - Implement a major feature (~20KLOC)
        - Replace every tab with 4 spaces
        - Refactor two function names
    - You stopped working on a task to fix a bug. You didn't fix the bug, but you don't want to lose your changes, so you are going to push them.
    - After you implemented a database connection, you are looking at 154 commits in your history. It seems that you also forgot to add a comma to the previous commit message.
