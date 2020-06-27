# Learning GitHub
Steps to follow
1. Forking a repo
2. Cloning a repo
3. Picking up a task
4. Working on a task
5. Creating PR
6. Configuring a remote for a fork
7. Syncing a fork

## Forking a repo
Forking is not always required, and based on each project. Most open source follow forking.
[Read More on Forking](https://help.github.com/en/github/getting-started-with-github/fork-a-repo)


## Cloning a repo
```
$ git clone https://github.com/nimitbhargava/templated-industrious
```

Note: cloning will create a new folder in your local machine
[Read More on Cloning](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)

## Picking up a task
1. Check issues at [issues page](https://github.com/nimitbhargava/templated-industrious/issues)
2. Comment in the task that you are interested in picking up the task
3. When maintainer reply that you can, then you can proceed with the development/fix

## Working on a task
0. Have your origin master sync with upstream master
1. Create a new branch from master `git checkout -b feature/change-logo`
2. Make changes required for the feature
3. Optional - check the files that were changed `git status`
4. Check differences `git diff` (unwated changes shouldn't be there at this stage)
5. Add files to staging `git add filename.js filename2.html` 
6. Commit the changes `git commit -m"meaningful commit message"
7. Push changes to your branch `git push -u origin feature/change-logo`

Note:
- In step 1, the name of the branch depends on wheather it's a `feature`, `fix`, `chore`, etc.
- In step 5, instead of adding each file one by one, you can use `git add .`. This command will add all the file to the staging.

## Creating PR
Developer should push their branch before starting with this step
Steps - 
1. Visit project GitHub repository
2. Click on `New pull request` button
3. Select your branch with which you want to create PR
4. Make sure you mention the issue id in the PR description. This will automatically link the PR with the issue. Example - `Related to #123`

Note: If you prepend `fixes` or `closes` before the issue id, then when the PR is merged, then the issue automatically closes.

## Configuring a remote for a fork
1. Check if upstream exists or not `git remote -v`
2. Add upstream `git remote add upstream https://github.com/nimitbhargava/templated-industrious.git`
3. Confirm newly added remote `git remote -v`

## Syncing a fork
1. `git fetch upstream`
2. `git checkout master`
3. `git rebase upstream/master`
4. `git push origin master` or may need to force push `git push origin master --force`