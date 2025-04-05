# General Git Commands for Version Control

---

## **Basic Commands**

1. **`git init`**  
   Initializes a new Git repository in the current directory.  
   **Example:** `git init`

2. **`git clone`**  
   Clones a repository from a remote source to your local machine.  
   **Example:** `git clone https://github.com/username/repository.git`

3. **`git status`**  
   Displays the current state of the repository (modified, added, etc.).  
   **Example:** `git status`

4. **`git add`**  
   Stages changes (files) to be committed.  
   **Example:** `git add .` (stages all changes)  
   **Example:** `git add file.txt`

5. **`git commit`**  
   Commits the staged changes to the local repository.  
   **Example:** `git commit -m "Initial commit"`

6. **`git push`**  
   Pushes local commits to a remote repository (like GitHub).  
   **Example:** `git push origin main`

7. **`git pull`**  
   Fetches and merges changes from the remote repository into your local branch.  
   **Example:** `git pull origin main`

8. **`git fetch`**  
   Fetches changes from the remote repository, but does not merge them.  
   **Example:** `git fetch`

9. **`git merge`**  
   Merges a branch into the current branch.  
   **Example:** `git merge feature-branch`

10. **`git log`**  
    Displays a list of commits in the current branch, with their details.  
    **Example:** `git log`

---

## **Branching and Merging**

11. **`git branch`**  
    Lists all local branches or creates a new branch.  
    **Example:** `git branch` (lists branches)  
    **Example:** `git branch new-branch` (creates a new branch)

12. **`git checkout`**  
    Switches to another branch or restores files.  
    **Example:** `git checkout main`  
    **Example:** `git checkout -b new-branch` (creates and switches to `new-branch`)

13. **`git branch -d`**  
    Deletes a branch (locally).  
    **Example:** `git branch -d old-branch`

14. **`git merge --no-ff`**  
    Merges a branch into the current branch, always creating a merge commit.  
    **Example:** `git merge --no-ff feature-branch`

15. **`git switch bug-fix`**  
    Switches to the `bug-fix` branch.  
    **Example:** `git switch bug-fix` (switches to the `bug-fix` branch)

16. **`git log`**  
    Shows the commit history for the current branch.  
    **Example:** `git log` (displays commit history)

17. **`git switch master`**  
    Switches to the `master` branch.  
    **Example:** `git switch master` (switches to the `master` branch)

18. **`git switch -c dark-mode`**  
    Creates a new branch called `dark-mode` and switches to it. The `-c` flag is used to create a new branch.  
    **Example:** `git switch -c dark-mode` (creates and switches to the `dark-mode` branch)

19. **`git checkout orange-mode`**  
    Switches to the `orange-mode` branch.  
    **Example:** `git checkout orange-mode` (switches to the `orange-mode` branch)

---

## **Remote Repositories**

15. **`git remote`**  
    Shows the remote repositories associated with your project.  
    **Example:** `git remote -v`

16. **`git remote add`**  
    Adds a remote repository to your project.  
    **Example:** `git remote add origin https://github.com/username/repository.git`

17. **`git remote remove`**  
    Removes a remote repository from your project.  
    **Example:** `git remote remove origin`

18. **`git push --set-upstream`**  
    Sets the upstream branch for your current branch.  
    **Example:** `git push --set-upstream origin main`

---

## **Undoing Changes**

19. **`git restore`**  
    Restores files to their state at the last commit.  
    **Example:** `git restore file.txt`

20. **`git reset`**  
    Unstages changes or resets the commit history (with different options).  
    **Example:** `git reset HEAD file.txt` (unstages the file)  
    **Example:** `git reset --hard` (resets everything to the last commit)

21. **`git revert`**  
    Creates a new commit that undoes changes made by a previous commit.  
    **Example:** `git revert <commit-hash>`

22. **`git rm`**  
    Removes a file from the working directory and stages the deletion.  
    **Example:** `git rm file.txt`

---

## **Working with Tags**

23. **`git tag`**  
    Lists all tags in the repository.  
    **Example:** `git tag`

24. **`git tag <tag-name>`**  
    Creates a new tag.  
    **Example:** `git tag v1.0`

25. **`git push origin --tags`**  
    Pushes tags to the remote repository.  
    **Example:** `git push origin --tags`

26. **`git tag -d <tag-name>`**  
    Deletes a tag locally.  
    **Example:** `git tag -d v1.0`

---

## **Stashing Changes**

27. **`git stash`**  
    Stashes the current changes (temporary save) to apply later.  
    **Example:** `git stash`

28. **`git stash apply`**  
    Applies the most recent stash.  
    **Example:** `git stash apply`

29. **`git stash pop`**  
    Applies the most recent stash and removes it from the stash list.  
    **Example:** `git stash pop`

---

## **Configuration and Settings**

30. **`git config`**  
    Configures user information for Git.  
    **Example:** `git config --global user.name "Your Name"`  
    **Example:** `git config --global user.email "youremail@example.com"`

31. **`git config --list`**  
    Lists all Git configuration settings.  
    **Example:** `git config --list`

---

## **Git Aliases**

32. **`git config --global alias.<alias-name> <command>`**  
    Creates a shortcut (alias) for a Git command.  
    **Example:** `git config --global alias.co checkout` (so `git co` is a shortcut for `git checkout`)

---

### How to Save:

1. Copy the above content.
2. Open **VSCode** and create a new file.
3. Paste the content into the file.
4. **Save** the file as `Git_Commands.md` or any name you'd prefer.

---
