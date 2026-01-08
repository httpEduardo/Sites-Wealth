# Git Guide for Beginners

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Documentation](https://img.shields.io/badge/Documentation-Guide-blue?style=for-the-badge)

## Overview

This repository serves as a comprehensive guide for developers who are getting started with Git and GitHub. Whether you're new to version control or need a quick reference for common Git operations, this guide provides clear explanations and practical examples to help you master Git workflows.

Git is a distributed version control system that allows you to track changes in your code, collaborate with other developers, and maintain a complete history of your project's evolution.

## Topics Covered

This guide covers the following essential Git concepts and operations:

- **Repository Initialization**: Setting up a new Git repository
- **Remote Repository Management**: Connecting local repositories to GitHub
- **Staging and Committing**: Preparing and saving changes
- **Pushing Changes**: Uploading commits to remote repositories
- **Branching Strategies**: Creating and managing branches
- **Merging**: Integrating changes from different branches
- **Pull Requests**: Collaborating through code reviews
- **Best Practices**: Professional Git workflows and conventions

## Installation

### Installing Git

**Linux (Debian/Ubuntu):**
```bash
sudo apt-get update
sudo apt-get install git
```

**Linux (Fedora):**
```bash
sudo dnf install git
```

**macOS:**
```bash
brew install git
```

**Windows:**
Download the installer from [git-scm.com](https://git-scm.com/download/win) and follow the installation wizard.

### Verify Installation

After installation, verify that Git is properly installed:

```bash
git --version
```

### Initial Configuration

Configure your Git identity (required for commits):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Basic Commands

### 1. Initialize a Local Repository

Navigate to your project directory and initialize a Git repository:

```bash
cd /path/to/your/project
git init
```

This creates a `.git` directory in your project folder, which Git uses to track all changes.

### 2. Connect Local Repository to Remote Repository

**Step 1: Create a repository on GitHub**
- Go to [GitHub](https://github.com) and sign in
- Click the "+" icon in the top right and select "New repository"
- Follow the prompts to create your repository
- Copy the repository URL (e.g., `https://github.com/username/repository.git`)

**Step 2: Add the remote repository**

Link your local repository to the remote GitHub repository:

```bash
git remote add origin https://github.com/username/repository.git
```

**Verify remote connection:**

```bash
git remote -v
```

### 3. Stage Files for Commit

**Add specific files:**

```bash
git add filename.extension
```

**Add multiple specific files:**

```bash
git add file1.txt file2.js file3.css
```

**Add all modified files:**

```bash
git add .
```

**Add all files with a specific extension:**

```bash
git add *.js
```

### 4. Commit Changes

After staging files, commit them with a descriptive message:

```bash
git commit -m "Add initial project files"
```

**Best practice for commit messages:**
- Use present tense ("Add feature" not "Added feature")
- Be descriptive but concise
- Reference issue numbers if applicable (e.g., "Fix login bug #42")

### 5. Push Changes to Remote Repository

**First push (sets upstream branch):**

```bash
git push -u origin master
```

Or if using `main` as the default branch:

```bash
git push -u origin main
```

**Subsequent pushes:**

```bash
git push
```

### 6. Check Repository Status

View the current state of your working directory:

```bash
git status
```

### 7. View Commit History

```bash
git log
```

**Condensed view:**

```bash
git log --oneline
```

### 8. Pull Changes from Remote

Download and integrate changes from the remote repository:

```bash
git pull origin main
```

## Advanced Topics

### Branching

**Create a new branch:**

```bash
git branch feature-branch-name
```

**Switch to a branch:**

```bash
git checkout feature-branch-name
```

**Create and switch to a new branch (shortcut):**

```bash
git checkout -b feature-branch-name
```

**List all branches:**

```bash
git branch -a
```

**Delete a branch:**

```bash
git branch -d feature-branch-name
```

### Merging

**Merge a branch into the current branch:**

```bash
git checkout main
git merge feature-branch-name
```

**Abort a merge (in case of conflicts):**

```bash
git merge --abort
```

### Resolving Merge Conflicts

1. Git will mark conflicts in the affected files
2. Open the files and look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
3. Edit the files to resolve conflicts
4. Stage the resolved files: `git add resolved-file.txt`
5. Complete the merge: `git commit -m "Resolve merge conflicts"`

### Stashing Changes

Save work in progress without committing:

```bash
git stash
```

**Apply stashed changes:**

```bash
git stash pop
```

**List all stashes:**

```bash
git stash list
```

### Undoing Changes

**Discard changes in working directory:**

```bash
git checkout -- filename.txt
```

**Unstage a file (keep changes):**

```bash
git reset HEAD filename.txt
```

**Undo last commit (keep changes):**

```bash
git reset --soft HEAD~1
```

**Undo last commit (discard changes):**

```bash
git reset --hard HEAD~1
```

## Best Practices

### 1. Commit Frequently
Make small, focused commits rather than large, monolithic ones. This makes it easier to track changes and revert if necessary.

### 2. Write Meaningful Commit Messages
- Use clear, descriptive commit messages
- Follow the conventional commits format when possible
- Examples: `feat: add user authentication`, `fix: resolve login timeout`, `docs: update installation guide`

### 3. Use Branches for Features
- Create a new branch for each feature or bug fix
- Keep the `main` branch stable and deployable
- Use descriptive branch names: `feature/user-auth`, `bugfix/login-error`, `hotfix/security-patch`

### 4. Pull Before Push
Always pull the latest changes before pushing your work to avoid conflicts:

```bash
git pull origin main
git push origin main
```

### 5. Review Changes Before Committing
Use `git status` and `git diff` to review your changes before staging and committing.

### 6. Use `.gitignore`
Create a `.gitignore` file to exclude files that shouldn't be tracked:
- Dependencies (`node_modules/`, `vendor/`)
- Build artifacts (`dist/`, `build/`)
- Environment files (`.env`, `config.local.js`)
- IDE-specific files (`.idea/`, `.vscode/`)

### 7. Keep Repository Clean
- Regularly delete merged branches
- Don't commit sensitive information (passwords, API keys)
- Use environment variables for configuration

### 8. Use Pull Requests
- Always use pull requests for code review before merging to main
- Provide clear descriptions of changes
- Address reviewer feedback before merging

## Additional Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Cheat Sheet](https://training.github.com/downloads/github-git-cheat-sheet/)

## Contributing

If you'd like to improve this guide, please feel free to:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This guide is provided as-is for educational purposes.

---

**Happy Coding! 🚀**
