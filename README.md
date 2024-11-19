 

# Git Basics: 1-Hour Learning Agenda

## Objective
Learn the fundamentals of Git, including version control, local repositories, and working with remote repositories.

---

## Agenda

### **0:00 - 0:05: Introduction to Git**
- **What is Git?**
  - A version control system to track changes in code.
  - Helps collaborate with others and maintain code history.
- **Key Concepts**:
  - **Repository**: A folder tracked by Git.
  - **Staging Area**: Temporary area for changes.
  - **Commit**: A saved snapshot of changes.
  - **Remote Repository**: A cloud-hosted repository (e.g., GitHub).

---

### **0:05 - 0:15: Initial Setup**
1. Check if Git is installed by running:
   ```bash
   git --version
   ```
   This will display the installed version of Git.

2. Configure Git with your name and email:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "you@example.com"
   ```

3. Verify the configuration:
   ```bash
   git config --list
   ```
   This will list all the global Git settings.

---

### **0:15 - 0:25: Creating and Using a Local Repository**
1. Create a new folder and navigate into it:
   ```bash
   mkdir my-first-repo
   cd my-first-repo
   ```

2. Initialize a Git repository in this folder:
   ```bash
   git init
   ```

3. Create a new file named `README.md` and add some text to it:
   ```bash
   echo "This is my first Git repository." > README.md
   ```

4. Check the current status of the repository:
   ```bash
   git status
   ```

5. Add the file to the staging area:
   ```bash
   git add README.md
   ```

6. Commit the file to the repository:
   ```bash
   git commit -m "Initial commit"
   ```

---

### **0:25 - 0:40: Making Changes**
1. Modify the `README.md` file by adding more text. For example:
   ```bash
   echo "Adding more content to the README file." >> README.md
   ```

2. Check the status to see the changes:
   ```bash
   git status
   ```

3. View the changes made to the file:
   ```bash
   git diff
   ```

4. Add the modified file to the staging area:
   ```bash
   git add README.md
   ```

5. Commit the changes:
   ```bash
   git commit -m "Updated README file"
   ```

6. View the commit history:
   ```bash
   git log --oneline
   ```

---

### **0:40 - 0:50: Working with Remote Repositories**
1. Create a new repository on GitHub (or GitLab).

2. Link the local repository to the remote repository:
   ```bash
   git remote add origin https://github.com/username/my-first-repo.git
   ```

3. Push your code to the remote repository:
   ```bash
   git push -u origin main
   ```

4. Pull updates from the remote repository (if any):
   ```bash
   git pull
   ```

---

### **0:50 - 1:00: Quick Collaboration**
1. Clone a remote repository:
   ```bash
   git clone https://github.com/username/some-repo.git
   ```

2. Create a new branch:
   ```bash
   git branch new-feature
   ```

3. Switch to the new branch:
   ```bash
   git checkout new-feature
   ```

4. Merge the branch back into the main branch:
   ```bash
   git checkout main
   git merge new-feature
   ```

### **1:00 - 1:15: Working with stash**

   - ### What is git stash?

      git stash allows you to temporarily save changes in your working directory without committing them. (To switch branches or work on something else)

      When you use git stash, Git saves the changes in a special stash area and reverts your working directory to the last committed state.

   - ### Common Use Cases

      - Switching branches

      - Pulling updates


### **1:15 - 1:40: How to Use git stash**

   - ### 1. Stash Changes

      To stash your uncommitted changes:

      ```bash
      git stash
      ```
      This stashes both tracked and staged changes, and reverts your working directory to a clean state.

   - ### 2. List Stashed Changes

      To see all stashed changes:

      ```bash
      git stash list
      ```
      Each stash is listed with an identifier, like stash@{0}.

   - ### 3. Apply Stashed Changes

      To apply the most recent stash:

      ```bash
      git stash apply
      ```
      To apply a specific stash (e.g., stash@{2}):

      ```bash
      git stash apply stash@{2}
      ```

   - ### 4. Pop Stashed Changes

      To apply the most recent stash and remove it from the stash list:

      ```bash
      git stash pop
      ```
   - ### 5. Drop a Stash

      To delete a specific stash (e.g., stash@{0}):

      ```bash
      git stash drop stash@{0}
      ```

   - ### 6. Clear All Stashes

      To remove all stashes:

      ```bash
      git stash clear
      ```
---

## Recap: Key Git Commands

| Command                   | Purpose                          |
| ------------------------- | -------------------------------- |
| `git init`                | Initialize a new repository      |
| `git status`              | Check the current status         |
| `git add <file>`          | Add file to staging area         |
| `git commit -m "message"` | Save changes to history          |
| `git log`                 | View commit history              |
| `git push`                | Upload changes to remote repo    |
| `git pull`                | Fetch changes from remote repo   |
| `git clone`               | Clone a remote repository        |
| `git branch <name>`       | Create a new branch              |
| `git checkout <branch>`   | Switch to a branch               |
| `git merge <branch>`      | Merge a branch into another      |
| `git stash`               | Stash tracked and staged changes |


---

## Tips
- Practice with small projects to build confidence.
- Refer to the Git cheat sheet for additional commands.
- Explore advanced features like branching, merging, and conflict resolution as you progress.
