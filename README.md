# SimpleCoop
This is for project 1 in web programming Spring 2024
Create new directory for repo on local machine:

mkdir SimpleCoop

Enter the directory
Clone central repository to local machine inside your new directory:

git clone https://github.com/TuckerGMcDonald/SimpleCoop.git

Create a Feature Branch:

git checkout -b <feature-branch-name> main

Use whatever name you'd like, but attach your name to it so we know who's branch is who's. This is where you will edit your code and push your changes to the remote repository.
Regularly Pull Updates:

git checkout main
git pull origin main

Always keep your local main branch updated, but don't make changes in here, use your feature-branch.
Keep Local Feature Branch Updated:

git checkout <feature-branch-name>
git checkout origin/main

Keeping your local feature branch updated with the remote repository's main branch limits conflicts.
Stashing (in case you forgot to pull updates before you started working):

git add <file_name>
git commit -m "message here"
git stash
git checkout -b <new-branch-name>

You can later apply your changes using git stash apply or git stash pop. Use the new branch to pull the most recent changes from the remote repository like before:

git checkout <new-branch-name>
git checkout origin/main

Then apply your changes to it from stash:

git stash apply

You can now add, commit, and then push your newly created branch to the remote repo. If you don't want to keep the new-branch you made in your local repository, you can always update your feature-branch with the changes you pushed to the remote repo and then later delete the new-branch on your local repository. Do not delete any branches in the remote repository.
Rebase Feature Branch (Optional but Recommended):

git checkout <feature-branch-name>
git rebase main

Before pushing changes, you can rebase your feature branch onto the main branch to incorporate any recent changes and minimize merge conflicts
Resolve Conflicts (If Any):

If there are merge conflicts during the rebase process, resolve them manually. Git will indicate the conflicting sections in the affected files. You can edit these files to resolve conflicts, then add and commit the changes.
Add and Commit:

git add <file_name>
git commit -m "short message to describe what you changed/added"

Push Changes:

git push origin <feature-branch-name>

Create a Pull Request:

    Go to the repository on GitHub.
    Click on the "Pull requests" tab.
    Click "New pull request."
    Select the base branch (main) and the compare branch (the feature branch).
    Review the changes, add a description, and request reviews from other teammates.
    Once approved, merge the pull request.
