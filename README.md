# Simple Task Management System Using Git

## Project Steps

### 1. Create a text file `tasks.txt` to serve as your task database.
1. Add initial tasks to `tasks.txt`:
    ```text
    Learn Git basics
    Set up Git repository
    ```

2. Stage and commit these changes:
    ```bash
    git add tasks.txt
    git commit -m "Add initial tasks"
    ```

---

### 2. Create Branches and Work on Features:
1. Create and move to a new branch called `feature/add-tasks` to add new tasks:
    ```bash
    git checkout -b feature/add-tasks
    ```

2. Add more tasks to `tasks.txt` and commit them:
    ```bash
    echo "- Practice Git branching" >> tasks.txt
    git add tasks.txt
    git commit -m "Add practice Git branching task"
    ```

3. Create and move to another branch called `feature/remove-tasks` to remove some tasks:
    ```bash
    git checkout master
    git checkout -b feature/remove-tasks
    ```

4. Remove a task from `tasks.txt` and commit the change:
    ```bash
    sed -i '/Learn Git basics/d' tasks.txt
    git add tasks.txt
    git commit -m "Remove Learn Git basics task"
    ```

---

### 3. Merge Branches and Handle Conflicts:
1. Switch to the `master` branch and merge `feature/add-tasks` and `feature/remove-tasks`:
    ```bash
    git checkout master
    git merge feature/add-tasks
    git merge feature/remove-tasks
    ```

2. If a conflict occurs, resolve it by editing `tasks.txt`, keeping the desired changes, then stage and commit the resolution:
    ```bash
    git add tasks.txt
    git commit -m "Resolve merge conflict"
    ```

---

### 4. Use Git Rebase:
1. Create and move to a new branch `feature/update-tasks` to update some tasks:
    ```bash
    git checkout -b feature/update-tasks
    ```

2. Make changes to `tasks.txt` and commit them:
    ```bash
    echo "- Review Git merge and rebase" >> tasks.txt
    git add tasks.txt
    git commit -m "Add review Git merge and rebase task"
    ```

3. Use rebase to integrate changes from `feature/update-tasks` into the `master` branch:
    ```bash
    git checkout master
    git rebase feature/update-tasks
    ```

---

### 5. Use Git Cherry Pick:
1. Select a specific commit from another branch and add it to the `master` branch using cherry-pick:
    ```bash
    git checkout master
    git cherry-pick <commit-id>
    ```

2. Resolve conflicts if they occur, then stage and commit:
    ```bash
    git add tasks.txt
    git commit -m "Resolve cherry-pick conflict"
    ```

---

### 6. Reverting to Previous Commits:
1. Make an incorrect change to `tasks.txt`:
    ```bash
    echo "- Some incorrect task" >> tasks.txt
    git add tasks.txt
    git commit -m "Add incorrect task"
    ```

2. Use `git revert` to undo the commit:
    ```bash
    git revert <commit-id>
    ```

3. If you want to reset the project to a previous state, use `git reset`:
    ```bash
    git reset --hard <commit-id>
    ```

---

### 7. Working with Remote Repository:
1. Create a remote repository on GitHub.

2. Link and push the local repository to the remote repository:
    ```bash
    git remote add origin <repository-url>
    git push -u origin master
    ```

---

## Final Task
Submit the final repository with a README file explaining what Git commands were used in each part.

<img src="https://drive.google.com/uc?export=view&id=1Q0IYBa-tLbzjk-KekEeCSTFqXxB9EBmN" width="700" />

