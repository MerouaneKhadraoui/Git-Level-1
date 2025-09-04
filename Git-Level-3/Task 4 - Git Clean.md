# Task 4: Git Clean

## Question

The Nautilus application development team was working on a git repository `/usr/src/kodekloudrepos/cluster` present on `Storage server` in `Stratos DC`. One of the developers mistakenly created a couple of files under this repository, but now they want to clean this repository without adding/pushing any new files. Find below more details:

**Task:**

Clean the `/usr/src/kodekloudrepos/cluster` git repository without adding/pushing any new files, make sure `git status` is clean.

---

## Solution

1. **Switch to Storage Server**

(Usually in KodeKloud you select the "Storage Server" from the terminal options.)

```bash
ssh natasha@ststor01
# password: Bl@kW
```

---

2. **Go to the repo path**

```bash
cd /usr/src/kodekloudrepos/cluster
```

---

3. **Check the current status**

```bash
git status
```
👉 You will see some untracked files listed.

---

4. **Clean the repository**

To remove **untracked files**:

```bash
git clean -f
```

If there are **untracked directories** too, use:

```bash
git clean -fd
```

If you want to check what will be deleted before actually deleting:

```bash
git clean -fdn
```
(`-n` = dry run, nothing removed)

---

5. **Verify**

```bash
git status
```
👉 It should now say:
```sql
nothing to commit, working tree clean
```

---

✅ **Final Answer:**
Use `git clean -fd` inside `/usr/src/kodekloudrepos/cluster` to remove all untracked files and directories so that `git status` is clean.