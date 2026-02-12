# Resolving Merge Conflicts

A merge conflict occurs when Git cannot automatically combine changes from different branches.

---

## 1️⃣ Identify Conflict

When merging, Git will show a message indicating which files have conflicts. You'll see something like "Automatic merge failed; fix conflicts and then commit the result."

---

## 2️⃣ Open the Conflicted File

Open the file with conflicts. You'll see conflict markers like this:

```text
<<<<<<< HEAD
This is the code from the current branch
=======
This is the code from the incoming branch
>>>>>>> feature-name
```

- `<<<<<<< HEAD` marks the start of your current branch's code
- `=======` separates the two versions
- `>>>>>>> feature-name` marks the end of the incoming branch's code

---

## 3️⃣ Fix the Conflict

Manually edit the file:
- Decide which code to keep (or combine both)
- Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
- Keep the correct code

---

## 4️⃣ Stage the Fixed File

```bash
git add file-name
```
This tells Git the conflict is resolved.

---

## 5️⃣ Complete the Merge

```bash
git commit
```
This finalizes the merge. Git will open an editor with a default merge commit message, or you can close it to use the default.
