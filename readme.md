# Git commands

### Terminology 

    Commit a state of the code base
    Branch a reference to a commit; can have a tracked upstream
    Tag a reference (standard) or an object (annotated)
    HEAD a place where your working directory is now

### Git Configuration

1.Set the name that will be attached to your commits and tags.

    git config --global user.name “Your Name” 

2.Set the e-mail address that will be attached to your commits and tags.

    git config --global user.email “you@example.com”

### Starting a Project

1.Create a new local repository in the current directory. If [project name] is provided, Git will create a new directory named [project name] and will initialize a repository inside it.

    git init [project name]

2.Downloads a project with the entire history from the remote repository.

    git clone <project url>

### Day to Day Work

1.Displays the status of your working directory. Options include new, staged, and modified files. It will retrieve branch name, current commit identifier, and changes pending commit.

    git status

2.Add a file to the staging area. Use. in place of the full file path to add all changed files from the current directory down into the directory tree.

    git add [file]

3.Show changes between working directory and staging area.

    git diff [file]

4.Shows any changes between the staging area and the repository.

    git diff --staged [file]

5.Revert some paths in the index (or the whole index) to their state in HEAD.

    git reset <path>...]

6.Create a new commit from changes added to the staging area. The commit must have a message! 

    git commit

### Storing your work

1.Put current changes in your working directory into stash for later use.

    git stash

2.Apply stored stash content into working directory, and clear stash.

    git stash pop

3.Clear the stashed changes

    git stash clear

### Git Branching

1.List all branches

    git branch

2.Create new branch

    git branch [branch_name]

3.Switch working directory to the specified branch. With -b: Git will create the specified branch if it does not exist.

    git checkout [-b][branch_name]

4.Join specified [branch_name] branch into your current branch (the one you are on currently).

    git merge [branch_name]

5.Remove selected branch, if it is already merged into any other.-D instead of -d forces deletion.

    git branch -d [branch_name]

### Inspect History

1.List commit history of current branch. -n count limits list to last n commits.

    git log [-n count]

### Reverting Changes

1.Switches the current branch to the target reference, leaving a difference as an uncommitted change. When --hard is used, all changes are discarded. It's easy to lose uncommitted changes with --hard.

    git reset [--hard][target reference]

2.Create a new commit, reverting changes from the specified commit. It generates an inversion of changes. 

    git revert [commit sha]

3.Restores the staged work back into the working directory.

    git restore --staged [file_name]



### Synchronizing Changes

1.Fetch changes from the remote, but not update tracking
branches.

    git fetch [remote]

2.Fetch changes from the remote and merge current branch with its upstream.

    git pull [remote]

3.Push local changes to the remote. Use --tags to push tags.

    git push [--tags][remote]

4.Push local branch to remote repository. Set its copy as an
upstream.

    git push -u [remote][branch]

### Fork

1.Setting the upstream
    git remote add upstream <project url>

### Misc

1.Squashing commits

    git remote -i [commit sha]

### Resources 

    https://www.simplilearn.com/tutorials/git-tutorial/merge-conflicts-in-git

    https://marklodato.github.io/visual-git-guide/index-en.html