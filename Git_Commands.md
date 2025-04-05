# General Git Commands for Version Control

---

# Table of Contents

1. [Basic Commands](#basic-commands)
2. [Branching and Merging](#branching-and-merging)
3. [Remote Repositories](#remote-repositories)
4. [Undoing Changes](#undoing-changes)
5. [Working with Tags](#working-with-tags)
6. [Stashing Changes](#stashing-changes)
7. [Configuration and Settings](#configuration-and-settings)
8. [Git Aliases](#git-aliases)

---

# General Git Commands for Version Control

---

## **Basic Commands**

1. **`git init`**  
   **Definition:** Initializes a new Git repository in the current directory. It creates a `.git` directory, which will store all the necessary metadata for version control.  
   **Example:** `git init`

2. **`git clone`**  
   **Definition:** Clones an existing remote repository to your local machine. It copies all files, branches, and commits.  
   **Example:** `git clone https://github.com/username/repository.git`

3. **`git status`**  
   **Definition:** Displays the current state of the repository, including changes to files (modified, added, etc.), staging status, and the current branch.  
   **Example:** `git status`

4. **`git add`**  
   **Definition:** Stages changes (new, modified, or deleted files) to be included in the next commit.  
   **Example:** `git add .` (stages all changes)  
   **Example:** `git add file.txt`

5. **`git commit`**  
   **Definition:** Commits the staged changes to the local repository, recording them as a snapshot with a descriptive message.  
   **Example:** `git commit -m "Initial commit"`

6. **`git push`**  
   **Definition:** Pushes local commits to a remote repository, syncing your local branch with the remote one.  
   **Example:** `git push origin main`

7. **`git pull`**  
   **Definition:** Fetches and merges changes from a remote repository into your local branch.  
   **Example:** `git pull origin main`

8. **`git fetch`**  
   **Definition:** Fetches changes from a remote repository but does not merge them into your local branch.  
   **Example:** `git fetch`

9. **`git merge`**  
   **Definition:** Merges a branch (or changes) into the current branch. This command can cause conflicts if there are discrepancies between the two branches.  
   **Example:** `git merge feature-branch`

10. **`git log`**  
    **Definition:** Displays a list of commits on the current branch, along with details such as commit messages, authors, and dates.  
    **Example:** `git log`

---

## **Branching and Merging**

11. **`git branch`**  
    **Definition:** Lists all local branches or creates a new branch.  
    **Example:** `git branch` (lists branches)  
    **Example:** `git branch new-branch` (creates a new branch)

12. **`git checkout`**  
    **Definition:** Switches between branches or restores files to a previous state.  
    **Example:** `git checkout main`  
    **Example:** `git checkout -b new-branch` (creates and switches to `new-branch`)

13. **`git branch -d`**  
    **Definition:** Deletes a local branch that has already been merged.  
    **Example:** `git branch -d old-branch`

14. **`git merge --no-ff`**  
    **Definition:** Merges a branch into the current branch, forcing a merge commit even if a fast-forward merge is possible.  
    **Example:** `git merge --no-ff feature-branch`

15. **`git switch <branch-name>`**  
    **Definition:** Switches to the specified branch. This command is a more intuitive alternative to `git checkout` for switching branches.  
    **Example:** `git switch bug-fix`

16. **`git log`**  
    **Definition:** Shows the commit history for the current branch.  
    **Example:** `git log`

17. **`git switch master`**  
    **Definition:** Switches to the `master` branch.  
    **Example:** `git switch master`

18. **`git switch -c <branch-name>`**  
    **Definition:** Creates a new branch and switches to it immediately. The `-c` flag is used to create a new branch.  
    **Example:** `git switch -c dark-mode`

19. **`git checkout <branch-name>`**  
    **Definition:** Switches to a specific branch.  
    **Example:** `git checkout orange-mode`

20. **`git checkout <commit-id> -- <file-path>`**  
    **Definition:** Checks out a file from a specific commit.  
    **Example:** `git checkout abc1234 -- README.md`

21. **`git checkout <branch-name> -- <file-path>`**  
    **Definition:** Checks out a specific file from a different branch.  
    **Example:** `git checkout main -- README.md`

22. **`git checkout -- <file-path>`**  
    **Definition:** Restores a file to its last committed state, discarding local changes.  
    **Example:** `git checkout -- README.md`

23. **`git restore --source <branch-or-commit> <file-path>`**  
    **Definition:** Restores a file from a specific branch or commit.  
    **Example:** `git restore --source main README.md`

24. **`git restore <file-path>`**  
    **Definition:** Discards local changes and restores the file to the last committed state.  
    **Example:** `git restore README.md`

25. **`git branch -m <new-branch-name>`**  
    **Definition:** Renames the current branch or a specified branch. The `-m` flag is used to rename the branch.  
    **Example:** `git branch -m new-branch-name` (renames the current branch to `new-branch-name`)  
    **Example:** `git branch -m old-branch-name new-branch-name` (renames `old-branch-name` to `new-branch-name`)

---

## **Remote Repositories**

15. **`git remote`**  
    **Definition:** Shows the remote repositories associated with your project.  
    **Example:** `git remote -v`

16. **`git remote add`**  
    **Definition:** Adds a remote repository to your project.  
    **Example:** `git remote add origin https://github.com/username/repository.git`

17. **`git remote remove`**  
    **Definition:** Removes a remote repository from your project.  
    **Example:** `git remote remove origin`

18. **`git push --set-upstream`**  
    **Definition:** Sets the upstream branch for your current branch, so subsequent pushes go to that branch by default.  
    **Example:** `git push --set-upstream origin main`

---

## **Undoing Changes**

19. **`git restore`**  
    **Definition:** Restores a file to its last committed state, discarding any local changes.  
    **Example:** `git restore file.txt`

20. **`git reset`**  
    **Definition:** Unstages changes or resets the commit history. It can be used with different options for different behaviors.  
    **Example:** `git reset HEAD file.txt` (unstages the file)  
    **Example:** `git reset --hard` (resets everything to the last commit)

21. **`git revert`**  
    **Definition:** Creates a new commit that undoes changes made by a previous commit, preserving history.  
    **Example:** `git revert <commit-hash>`

22. **`git rm`**  
    **Definition:** Removes a file from the working directory and stages its deletion.  
    **Example:** `git rm file.txt`

---

## **Working with Tags**

23. **`git tag`**  
    **Definition:** Lists all tags in the repository. Tags are often used to mark releases or significant milestones in the project.  
    **Example:** `git tag`

24. **`git tag <tag-name>`**  
    **Definition:** Creates a new tag in the repository at the current commit.  
    **Example:** `git tag v1.0`

25. **`git push origin --tags`**  
    **Definition:** Pushes all tags to the remote repository.  
    **Example:** `git push origin --tags`

26. **`git tag -d <tag-name>`**  
    **Definition:** Deletes a tag locally.  
    **Example:** `git tag -d v1.0`

---

## **Stashing Changes**

27. **`git stash`**  
    **Definition:** Temporarily saves changes (that are not ready to commit) so you can work on something else.  
    **Example:** `git stash`

28. **`git stash apply`**  
    **Definition:** Applies the most recent stash, restoring the saved changes.  
    **Example:** `git stash apply`

29. **`git stash pop`**  
    **Definition:** Applies the most recent stash and removes it from the stash list.  
    **Example:** `git stash pop`

---

## **Configuration and Settings**

30. **`git config`**  
    **Definition:** Configures user information for Git, such as name and email.  
    **Example:** `git config --global user.name "Your Name"`  
    **Example:** `git config --global user.email "youremail@example.com"`

31. **`git config --list`**  
    **Definition:** Lists all Git configuration settings.  
    **Example:** `git config --list`

---

## **Git Aliases**

32. **`git config --global alias.<alias-name> "<command>"`**  
    **Definition:** Creates a shortcut (alias) for a Git command.  
    **Example:** `git config --global alias.co "checkout"` (so `git co` is a shortcut for `git checkout`)

---

### How to Save:

1. Copy the above content.
2. Open **VSCode** and create a new file.
3. Paste the content into the file.
4. **Save** the file as `Git_Commands.md` or any name you'd prefer.

---
