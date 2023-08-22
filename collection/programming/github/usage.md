<br>

The following table provides an overview of commonly used Git commands, what they do, and some best practices associated with them.

<br>

| Command | Description | Best Practices |
|---------|-------------|----------------|
| `git init` | Initializes a new Git repository and begins tracking an existing directory. | Run this command only once per project. |
| `git clone [url]` | Clone (or download) a repository from an existing URL. | Be cautious when cloning repositories from unknown sources. |
| `git status` | Shows the status of changes as untracked, modified, or staged. | Use often to check the status of your changes. |
| `git add [file or .]` | Adds changes in the specified file or directory to the staging area. `. `adds all changes. | Be specific about what you add. Avoid `git add .` unless you're sure about all changes. |
| `git commit -m "[commit message]"` | Commits the staged snapshot with a descriptive message. | Write clear, concise commit messages. |
| `git branch` | Lists all local branches. | Use often to know which branch you're on. |
| `git branch [branch-name]` | Creates a new branch. | Name branches descriptively. |
| `git checkout [branch-name]` | Switch to the specified branch and updates the working directory. | Commit or stash changes before switching branches. |
| `git merge [branch-name]` | Merges the specified branch into the current branch. | Resolve conflicts promptly. |
| `git pull` | Fetches and merges changes from the remote repository. | Pull regularly to keep your branch up-to-date. |
| `git pull --rebase` | Fetches and rebases current branch onto the remote branch. | Useful for maintaining a linear history. |
| `git pull --no-rebase` | Fetches and merges (default behavior) without rebasing. | Default behavior unless `pull.rebase` config is set. |
| `git push [remote] [branch]` | Pushes the branch to the specified remote repository. | Pull and merge changes before pushing. |
| `git push -f` | Force pushes changes. This overwrites remote branch with local branch. | Use with caution, especially on shared branches. |
| `git log` | Displays the commit logs. | Use `git log --oneline` for a compact view. |
| `git diff` | Shows differences between the working directory and the last commit. | Review your changes before committing. |
| `git stash` | Temporarily stashes changes made to your working directory. | Use sparingly and remember to apply or discard stashes. |
| `git stash list` | Lists all stashed changes. | Review and apply or drop stashes as needed. |
| `git remote` | Lists all remote repositories connected to the current project. | Prune old or unused remotes regularly. |
| `git remote add [name] [url]` | Adds a remote repository to your project. | Choose descriptive remote names. |
| `git fetch` | Fetches updates from the remote repository without merging them. | Use to inspect changes before merging. |

<br>

---

<br>

### Expanded Best Practices:

1. **Commit Often:** Easier to pinpoint changes and errors.
2. **Branch Thoughtfully:** Use feature, bugfix branches; avoid direct work on main branches.
3. **Descriptive Commit Messages:** Be clear about your changes for the sake of clarity.
4. **Pull Before Pushing:** Helps prevent merge conflicts.
5. **Use `.gitignore`:** Exclude unnecessary files.
6. **Force Pushing (`-f`):** Be very careful. This can overwrite changes on remote branches and is dangerous on shared branches.
7. **Rebasing:** Can create a clean, linear history, but alters commit history. Coordinate with your team before rebasing shared branches.
