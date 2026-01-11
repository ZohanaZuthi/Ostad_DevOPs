Here’s a simple, clean explanation you can drop straight into your notes.

````md
## Git Rebase

`git rebase` moves your branch commits on top of another branch to create a **straight, clean history**.

### Example

```bash
git checkout feature
git rebase master
```
````

This places `feature` commits on top of `master`.

### Why use it

- Keeps history easy to read
- Avoids extra merge commits

⚠️ Do not rebase commits that are already pushed and shared.

---

## Git Tag

A tag is a **label for a specific commit**, usually used to mark releases.

### Create a tag

```bash
git tag v1.0
```

### Push tags to remote

```bash
git push origin v1.0
```

or

```bash
git push origin --tags
```

### List tags

```bash
git tag
```

### Use cases

- Mark release versions
- Save important project milestones

### One-line summary

- **Rebase** = replay commits on another branch
- **Tag** = name a specific commit

```

```
