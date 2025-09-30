# IgnitionXGit

This guide is for new Ignition developers using Git for version control with Inductive Automation Ignition projects.  
If you already know Git, you probably don’t need this—but even experienced users may find some overlooked tips here.

---

## Why Use Git with Ignition?

- Roll back safely when experimental changes break something.
- Track all modifications to scripts, views, and tags.
- Collaborate with your team without overwriting each other's work.
- Maintain project history securely, beyond manual backups.

---

## Prerequisites

- **Git**: [Download here](https://git-scm.com/downloads)
- **Visual Studio Code (VS Code)**: [Download here](https://code.visualstudio.com/)
- **GitHub Account**: [Sign up here](https://github.com/)

---

## GitHub vs Bitbucket

- **GitHub** is recommended; cost-effective and beginner-friendly.
- Bitbucket is only worth it if you need advanced Jira features like sprint tracking and detailed bug management.
- Most users on Bitbucket don't actually use these features—stick with GitHub unless you have a specific reason.

---

## Setting Up Ignition Projects with Git

**Step 1: Prepare the Ignition Projects Folder**  
Navigate to:

```
C:/Program Files/Inductive Automation/Ignition/data/projects
```

Make sure the folder is empty before you clone a repository—leftover files may cause issues in Ignition.

**Step 2: Open the Folder in VS Code**  
Launch VS Code and open the above projects folder.

**Step 3: Clone Your Repo (the Essential Dot Trick)**  
Open the VS Code terminal (press `Ctrl + ``) and run:

```
cd "C:/Program Files/Inductive Automation/Ignition/data/projects"
git clone <your_repo_url> .
```

The dot `.` at the end is crucial; it clones *directly* into the projects folder.  
Without the dot, Git creates a subfolder and Ignition Designer won't detect it.

---

## Project Structure Requirements

Ignition requires every project to contain a `project.json` file.  
Example:

```
/projects
   /MyProject
      project.json
```

If `project.json` is missing, the Designer will ignore your project.

---

## Committing Using VS Code UI

1. In VS Code, click the **Source Control** (Git logo) on the left sidebar.
2. Changed files appear in the list:
   - Files marked ‘M’ = Modified
   - Files marked ‘A’ = Added
3. Stage files you want to commit by clicking the **+** icon next to each.
4. Type a descriptive commit message at the top.
5. Click the **checkmark (Commit)** button.
6. Push using the **“…” → Push** menu, or hit **Sync Changes** in the status bar.

**(Attach Screenshot: VS Code Source Control panel with staged Ignition JSON files)**

---

## Git Cycle: Basic Terminal Workflow

The basic workflow for version control in Git:

| Step    | Command                                         | What It Does                                  |
|---------|-------------------------------------------------|-----------------------------------------------|
| Clone   | `git clone <url> .`                             | Copies a remote repository to your local projects folder |
| Add     | `git add .` or `git add MyProject/`             | Stages all (or specific) files for the next commit       |
| Commit  | `git commit -m "message"`                       | Saves a snapshot of staged changes to your local repository |
| Push    | `git push origin main`                          | Uploads your local commits to the remote repository      |
| Pull    | `git pull origin main`                          | Retrieves the latest changes pushed by others           |
| Branch  | `git checkout -b feature/new-feature`           | Creates a separate line of development                 |
| Switch  | `git checkout main`                             | Switches to another branch                            |



---

## Using Branches

- Create a branch for features:  
  ```
  git checkout -b feature/new-dashboard
  ```
- Switch between branches as needed:  
  ```
  git checkout main
  ```
- Branches separate new work so your main code is always stable.

---

## Managing Multiple Repositories

Each Ignition project can have a separate Git repository (`.git` folder).  
For example:
- Project A → Repo A
- Project B → Repo B

Double-check the active repo and branch before pushing.

---

## What’s Not Covered

- Merge conflicts, rebasing, and advanced workflows
- If these come up, check Git documentation or seek help—they’re advanced topics.

---

## Recommended Git Learning Resource

For a practical and clear introduction to Git, check out Hitesh Choudhary’s Git tutorial here:  
[Learn Git by Hitesh Choudhary](https://www.youtube.com/watch?v=8JJ101D3knE)

---

## Contact

For questions or help, feel free to reach out:  

- Email: saifulislam778866@gmail.com  
- LinkedIn: [Your LinkedIn Profile](https://www.linkedin.com/in/saifulislam778866)

---

## Final Notes

Setting up Git with Ignition ensures safe rollback, avoids accidental overwrites, and gives you a trackable record of your changes.  
Start simple—clone, add, commit, push, pull. Branches will come naturally once you're comfortable.

---
