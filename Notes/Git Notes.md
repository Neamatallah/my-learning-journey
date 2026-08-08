# Git Notes

A personal reference for Git and GitHub concepts, commands, workflows, and common issues learned throughout my backend development journey.

---

# 1. What is Git?

Git is a distributed version control system (DVCS).

It helps developers:

- Track changes in a project.
- Save different versions of their work.
- View the history of changes.
- Return to previous versions when needed.
- Work with branches.
- Collaborate with other developers.

Git works locally on my computer.

---

# 2. Git vs GitHub vs Cmder

## Git

Git is the version control system itself.

It runs on my computer and is responsible for:

- Tracking changes.
- Creating commits.
- Managing branches.
- Maintaining project history.

## GitHub

GitHub is an online platform that hosts Git repositories.

It allows developers to:

- Store repositories remotely.
- Back up projects online.
- Share code.
- Collaborate with others.
- Create Pull Requests.
- Review and merge changes.

## Cmder

Cmder is a terminal emulator for Windows.

It provides a command-line environment where I can run Git and other terminal commands.

Cmder is not a replacement for Git.

---

# 3. Git Repository

A repository is a project that Git tracks.

There are two main types:

## Local Repository

The repository stored on my computer.

## Remote Repository

A repository stored on a remote platform such as GitHub.

A local repository can be connected to a remote repository so changes can be synchronized between them.

---

# 4. Creating a Repository

## `git init`

Initializes Git in the current directory and turns it into a local Git repository.

```bash
git init
```

After running `git init`, Git creates a hidden directory called:

```text
.git
```

The `.git` directory contains the Git metadata and information required for Git to manage the repository.

It is normally hidden in the file system.

To display hidden files in the terminal:

```bash
ls -a
```

---

# 5. Git Configuration

Git can store information about the user who creates commits.

## Configure username

```bash
git config --global user.name "Your Name"
```

## Configure email

```bash
git config --global user.email "your@email.com"
```

## `git config`

`git config` is used to view and modify Git configuration settings.

## `--global`

The `--global` option applies the configuration to all Git repositories for the current user on the computer.

Without `--global`, the configuration can be applied only to the current repository.

---

# 6. Basic Terminal Commands Used with Git

## `pwd`

Pronunciation: **P-W-D**

Shows the current working directory.

```bash
pwd
```

Useful for checking where I currently am in the terminal.

---

## `ls`

Pronunciation: **L-S**

Lists the files and directories in the current location.

```bash
ls
```

---

## `ls -a`

Lists files and directories, including hidden files.

```bash
ls -a
```

This can be used to see the hidden `.git` directory.

---

## `explorer .`

Opens the current directory in Windows File Explorer.

```bash
explorer .
```

The `.` refers to the current directory.

---

# 7. Git Status

## `git status`

Shows the current state of the working directory and staging area.

```bash
git status
```

It can show:

- Modified files.
- Untracked files.
- Staged files.
- The current branch.
- Whether there are changes that have not been committed.

### Important Note

Git only detects changes after the file has been saved.

For example, if I modify a file in Visual Studio Code but do not save it, Git may not show the modification yet.

---

# 8. The Basic Git Workflow

The basic workflow I practiced is:

```text
Edit files
   ↓
Save files
   ↓
git add
   ↓
git commit
   ↓
git push
```

Each command has a different purpose.

---

# 9. `git add`

Adds changes to the staging area.

```bash
git add filename
```

To stage all changes in the current directory:

```bash
git add .
```

The staging area allows me to choose which changes should be included in the next commit.

---

# 10. `git commit`

Creates a snapshot of the staged changes.

```bash
git commit -m "Commit message"
```

The `-m` option allows me to provide the commit message directly.

Example:

```bash
git commit -m "Update README"
```

A commit represents a saved point in the project's history.

---

# 11. `git log`

Displays the commit history of the repository.

```bash
git log
```

It can be used directly from the terminal without opening GitHub.

A shorter version of the history can be displayed with:

```bash
git log --oneline
```

When viewing the log, pressing:

```text
q
```

exits the log view.

---

# 12. Connecting a Local Repository to GitHub

A local repository can be connected to a remote GitHub repository.

## `git remote add origin`

```bash
git remote add origin <repository-URL>
```

`origin` is the conventional default name given to the remote repository.

Example using SSH:

```bash
git remote add origin git@github.com:username/repository.git
```

---

# 13. `git remote -v`

Shows the remote URLs configured for the repository.

```bash
git remote -v
```

The output normally shows URLs for:

```text
fetch
push
```

This is useful for checking which GitHub repository the local repository is connected to.

---

# 14. HTTPS vs SSH

GitHub repositories can be accessed using different authentication methods.

## HTTPS

Uses an HTTPS repository URL.

Example:

```text
https://github.com/username/repository.git
```

## SSH

Uses an SSH repository URL.

Example:

```text
git@github.com:username/repository.git
```

SSH requires an SSH key to be configured and added to GitHub.

After SSH is configured, it provides a convenient way to authenticate with GitHub without repeatedly entering credentials.

---

# 15. SSH Authentication

SSH stands for Secure Shell.

An SSH key pair contains:

- A private key.
- A public key.

The private key stays on my computer and should never be shared.

The public key can be added to GitHub.

## Generate an SSH key

An SSH key pair can be generated using:

```bash
ssh-keygen
```

This creates the key pair on the computer.

## Add the public key to GitHub

The public key is added to the SSH keys section of the GitHub account.

The private key should remain private.

## Test the connection

```bash
ssh -T git@github.com
```

This can be used to verify that the SSH connection to GitHub is working.

---

# 16. `git push`

Uploads local commits to the remote repository.

```bash
git push
```

A common first push can be:

```bash
git push -u origin main
```

The direction is:

```text
Local Repository
       ↓
    GitHub
```

So:

> `push` = send my local commits to the remote repository.

---

# 17. `git fetch`

Downloads information about changes from the remote repository without merging those changes into the current branch.

```bash
git fetch
```

The direction is:

```text
GitHub
   ↓
Local Repository
```

`fetch` lets me see that remote changes exist without immediately applying them to my working branch.

---

# 18. `git pull`

Downloads changes from the remote repository and integrates them into the current branch.

```bash
git pull
```

Conceptually:

```text
git fetch
+
integrate the changes
```

So:

- `fetch` → download remote changes without integrating them.
- `pull` → download and integrate remote changes.
- `push` → upload local commits.

---

# 19. Push vs Fetch vs Pull

| Command | Direction | Purpose |
|---|---|---|
| `git push` | Local → Remote | Upload local commits |
| `git fetch` | Remote → Local | Download remote changes without merging |
| `git pull` | Remote → Local | Download and integrate remote changes |

A useful way to remember them:

```text
push
Local ─────────→ GitHub

fetch
Local ←───────── GitHub
      download only

pull
Local ←───────── GitHub
      download + integrate
```

---

# 20. Cloning a Repository

## `git clone`

Copies a remote repository to the local computer.

```bash
git clone <repository-URL>
```

Example:

```bash
git clone https://github.com/username/repository.git
```

After cloning, the repository exists locally and is already connected to the remote repository.

I practiced cloning a repository from GitHub using Cmder.

---

# 21. Git Clone SSL Issue

During the initial Git setup, I encountered an SSL certificate issue while trying to clone a repository.

Git was using Windows Schannel as its SSL backend.

The issue was resolved by configuring Git to use OpenSSL:

```bash
git config --global http.sslBackend openssl
```

This allowed Git to use OpenSSL for HTTPS connections.

---

# 22. Branches

A branch is an independent line of development within a Git repository.

Branches allow developers to work on changes without directly modifying another branch.

The default branch in many GitHub repositories is:

```text
main
```

---

# 23. `git branch`

Lists the local branches.

```bash
git branch
```

The current branch is marked with:

```text
*
```

For example:

```text
* main
```

The `*` indicates the branch I am currently on.

---

# 24. `git branch -a`

Lists both local and remote branches.

```bash
git branch -a
```

This is useful when I want to see branches that exist on the remote repository as well as branches available locally.

---

# 25. `git checkout`

`git checkout` can be used to switch between branches.

```bash
git checkout branch-name
```

It can also be used to inspect a specific commit.

For example:

```bash
git checkout <commit-hash>
```

When checking out a specific commit, I can inspect the project as it existed at that point in history.

---

# 26. Fork

A Fork creates a copy of another user's repository under my own GitHub account.

It is commonly used when I want to contribute to a repository that I do not own.

Typical workflow:

```text
Original Repository
        ↓
      Fork
        ↓
My GitHub Repository
```

A Fork is different from cloning.

- **Fork** → creates a copy on GitHub under my account.
- **Clone** → copies a repository from a remote location to my local computer.

---

# 27. Pull Request

A Pull Request (PR) is a request to merge changes from one branch or repository into another.

A common contribution workflow is:

```text
Fork repository
      ↓
Clone repository
      ↓
Create changes
      ↓
Commit changes
      ↓
Push changes
      ↓
Create Pull Request
      ↓
Review
      ↓
Merge
```

I learned the concept of Pull Requests and how they are used for collaboration.

Practical usage will be covered later.

---

# 28. Merge

A merge combines changes from one branch into another branch.

For example:

```text
main
  ↑
  |
feature branch
```

After merging, the changes from the feature branch become part of the target branch.

I learned the concept of merging and will practice it later.

---

# 29. Git Reset

`git reset` moves the current branch to another commit.

It can be used to undo commits, depending on the selected option.

Common modes include:

```bash
git reset --soft
git reset --mixed
git reset --hard
```

## `--soft`

Moves the branch to an earlier commit while keeping the changes staged.

## `--mixed`

Moves the branch to an earlier commit and keeps the changes in the working directory, but unstaged.

This is the default mode.

## `--hard`

Moves the branch to an earlier commit and removes the changes from the working directory.

Because `--hard` can permanently discard changes, it should be used carefully.

I learned the concept of `reset`; practical use will be covered later.

---

# 30. Git Revert

`git revert` creates a new commit that reverses the changes introduced by an earlier commit.

It does not simply erase the old commit from history.

Example:

```bash
git revert <commit-hash>
```

Conceptually:

```text
Original commit
      ↓
New commit that reverses it
```

This makes `revert` useful when working with shared repositories because the history remains intact.

---

# 31. Reset vs Revert

| Command | What it does |
|---|---|
| `git reset` | Moves the branch to another commit |
| `git revert` | Creates a new commit that reverses an earlier commit |

A simple way to remember:

> Reset changes where the branch points.

> Revert creates a new commit that undoes previous changes.

---

# 32. Common Git Workflow

A simple workflow for making and uploading changes is:

```bash
git status
git add .
git commit -m "Describe the changes"
git push
```

Before committing:

1. Check the current state.
2. Save the files.
3. Stage the desired changes.
4. Create a commit.
5. Push the commit to GitHub.

---

# 33. Local vs Remote Changes

Git works with both the local repository and the remote repository.

```text
                  GitHub
                (Remote)
                   ↑
                git push
                   |
                   |
Local Repository ──┘
      |
      |
      ↓
  Working Files
```

Commands such as `add`, `commit`, and `log` primarily work with the local repository.

Commands such as `push`, `fetch`, and `pull` involve communication with the remote repository.

---

# 34. Important Notes

## Save files before checking Git

If a file is modified in Visual Studio Code but has not been saved, Git may not detect the change.

Always save the file before checking:

```bash
git status
```

---

## `.git` is hidden

The `.git` directory is normally hidden.

Use:

```bash
ls -a
```

to display it in the terminal.

The `.git` directory contains important Git information and should not be manually deleted unless I intentionally want to remove Git tracking from the project.

---

## `origin`

`origin` is the conventional name for the remote repository created when connecting a local repository to a remote repository.

It is only a name; it can technically be changed.

---

## GitHub is not Git

Git and GitHub are related but different.

```text
Git      → Version control system
GitHub   → Online platform for hosting and collaborating on Git repositories
```

---

## Git does not automatically save my files

Git tracks changes to files, but it does not save unsaved changes inside Visual Studio Code.

The file must be saved first.

---

# 35. Commands Quick Reference

| Command | Purpose |
|---|---|
| `git config` | Configure Git settings |
| `git init` | Initialize a local repository |
| `git clone` | Copy a remote repository locally |
| `git status` | Check repository status |
| `git add` | Stage changes |
| `git commit` | Create a commit |
| `git log` | View commit history |
| `git remote -v` | View remote repository URLs |
| `git push` | Upload local commits |
| `git fetch` | Download remote changes without merging |
| `git pull` | Download and integrate remote changes |
| `git branch` | List local branches |
| `git branch -a` | List local and remote branches |
| `git checkout` | Switch branches or inspect a commit |
| `git reset` | Move the branch to another commit |
| `git revert` | Create a commit that reverses an earlier commit |

---

# 36. Authentication Quick Reference

## HTTPS

```text
https://github.com/username/repository.git
```

## SSH

```text
git@github.com:username/repository.git
```

SSH requires an SSH key pair.

Useful commands:

```bash
ssh-keygen
```

```bash
ssh -T git@github.com
```

---

# 37. Collaboration Concepts

These concepts have been introduced but will be practiced more as I continue learning Git:

- Fork
- Pull Request
- Merge
- Branch-based development
- Reset
- Revert

---

# 38. Key Takeaways

- Git is a version control system.
- GitHub hosts Git repositories online.
- A repository can exist locally and remotely.
- `git init` creates a local Git repository.
- `.git` stores Git's repository information.
- `git add` stages changes.
- `git commit` saves a snapshot to the local history.
- `git push` sends commits to the remote repository.
- `git fetch` downloads remote information without merging it.
- `git pull` downloads and integrates remote changes.
- `git log` allows me to inspect commit history from the terminal.
- Branches allow separate lines of development.
- SSH provides an authentication method for communicating with GitHub.
- Forks, Pull Requests, and Merges are important for collaboration.
- `reset` and `revert` are different ways of dealing with previous changes.
