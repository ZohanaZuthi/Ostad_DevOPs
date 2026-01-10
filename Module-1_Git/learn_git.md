# Git Command Short Descriptions

- **git status**  
  Shows the current state of the repository: branch, staged files, unstaged changes, and untracked files.

- **git add .**  
  Stages all changes in the current directory and subdirectories, excluding ignored files.

- **git diff**  
  Shows unstaged changes compared to the last commit.

- **git diff --staged**  
  Shows changes that are staged and ready to be committed.

- **git commit -m "message"**  
  Saves staged changes to the repository with a commit message.

- **git log**  
  Displays the commit history.

- **git push**  
  Uploads local commits to the remote repository.

- **git push -u origin <branch>**  
  Pushes a branch and sets it as the upstream branch.

# How to get back to previous commit

## 1. Go back to a previous commit (temporary)

Use this when you only want to view or test an older version.

after this you will see all the commits hash, then take 5-6 character from the hash

```bash
git log
```

```bash
git checkout <commit-hash>
```

Check where you are:

```bash
git status
# HEAD detached at <commit-hash>
```

---

## 2. Return to the current (latest) state

If you came from an old commit using `checkout`:

```bash
git checkout master
```

This brings you back to the latest commit on the branch.

---

## 3. Make a previous commit the new latest (remove newer commits)

Use this when you want the project to end at an older commit.

```bash
git checkout master
git reset --hard <previous-commit-hash>
```

If the newer commits were already pushed:

```bash
git push --force
```

---

## 4. Remove all commits before a certain commit

Keeps only commits after the specified point.

```bash
git reset --hard <commit-after-the-one-you-want-to-remove>
```

````md
# Git Reset

## Soft Reset

```bash
git reset --soft <commit>
```
````

- Moves HEAD
- Keeps changes staged
- Use to redo a commit

Example:

```bash
git reset --soft HEAD~1
```

---

## Hard Reset

```bash
git reset --hard <commit>
```

- Moves HEAD
- Deletes all changes
- Use to discard commits

Example:

```bash
git reset --hard HEAD~1
```

---
