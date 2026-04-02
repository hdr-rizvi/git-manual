If you’re continuously updating your code and want to keep one **stable checked version** plus another **actively developing version**, the best practice is to use a proper **branching strategy** in GitHub.

Here’s a clean and professional workflow 👇

---

# ✅ Recommended Setup: `main` + `dev` Branch Strategy

### 1️⃣ `main` branch → Stable / Final / Checked Version

* Always contains **tested and working code**
* Only updated when you are confident
* Represents production-ready state

### 2️⃣ `dev` (or `develop`) branch → Active Development

* Where you continuously update
* Can be unstable
* Experimental changes go here

---

# 🔁 Typical Workflow

### Step 1: Create a development branch (once)

```bash
git checkout main
git pull
git checkout -b dev
git push -u origin dev
```

Now you have:

* `main` → stable
* `dev` → development

---

### Step 2: Work normally on `dev`

```bash
git checkout dev
# make changes
git add .
git commit -m "Add new feature"
git push
```

You can commit as often as you want.

---

### Step 3: When development is stable → Merge into `main`

```bash
git checkout main
git pull
git merge dev
git push
```

Now `main` becomes updated and stable again.

---

# 🚀 Even Better: Use Feature Branches (Professional Way)

If your project grows, use:

```
main
 └── dev
      ├── feature-ml-model
      ├── feature-new-plot
      └── bugfix-power-balance
```

Workflow:

1. Branch from `dev`
2. Develop feature
3. Merge back into `dev`
4. When ready → merge `dev` → `main`

---

# 🏷️ Tag Stable Releases (Very Important)

When `main` is stable:

```bash
git tag -a v1.0 -m "First stable physics model"
git push origin v1.0
```

Tags allow you to always return to specific versions.

---

# 🧠 Best Practice Summary

| Purpose            | Use                  |
| ------------------ | -------------------- |
| Stable code        | `main`               |
| Ongoing updates    | `dev`                |
| Individual feature | `feature-*` branches |
| Official release   | Git tags             |

---

# 🔥 If You Work Alone

Simple structure is enough:

```
main  (stable)
dev   (work here daily)
```

No need to overcomplicate.

---


# FAQs

## Q-1. To revert to back to current commit and delete all new changes.

### Method-1

```bash
git status

# To undo all edits in a file
git checkout -- <file>

# To undo all edits in current dir
git checkout -- .


# Remove new untracked files 
## dry run to see what would be deleted without actually deleting it.
git clean -n
## To delete untrack files and dir
git clean -fd

```

### Method-2

To discard local changes to all files, permanently:

```bash
# Wipe everything at once (Tracked+staged)
git reset --hard
```


For detals
https://docs.gitlab.com/topics/git/undo/