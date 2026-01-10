## Git Branching and Merge

### Git Branching

A branch is a **separate line of development**. It lets you work on features or fixes without affecting the main code.

**Create a branch**

```bash
git branch feature-1
```

**Switch to a branch**

```bash
git checkout feature-1
```

**Create and switch together**

```bash
git checkout -b feature-1
```

**List branches**

```bash
git branch
```

Use branches when:

- Working on a new feature
- Fixing bugs
- Experimenting safely

---

### Git Merge

Merge combines changes from one branch into another.

**Merge a branch into master**

```bash
git checkout master
git merge feature-1
```

This:

- Brings feature changes into `master`
- Creates a merge commit (if needed)

---

### Merge Conflicts

Conflicts happen when Git can’t auto-merge changes.

Steps to fix:

1. Open conflicted files
2. Resolve conflicts manually
3. Add the fixed files

```bash
git add <file>
```

4. Complete the merge

```bash
git commit
```

---
