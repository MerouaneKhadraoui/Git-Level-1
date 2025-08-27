# Day 24: Git Create Branches

## Question

Nautilus developers are actively working on one of the project repositories, `/usr/src/kodekloudrepos/blog`. Recently, they decided to implement some new features in the application, and they want to maintain those new changes in a separate branch. Below are the requirements that have been shared with the DevOps team:

**Task:**

1. On `Storage server` in Stratos DC create a new branch `xfusioncorp_blog` from `master` branch in `/usr/src/kodekloudrepos/blog` git repo.

2. Please do not try to make any changes in the code.

---

## Solution

1. **Switch to Storage Server**

(Usually in KodeKloud you select the "Storage Server" from the terminal options.)

```bash
ssh natasha@ststor01
# password: Bl@kW
```

---

2. **Go to the repository directory**

```bash
cd /usr/src/kodekloudrepos/blog
```

---

3. **Check git status & current branch**

```bash
git status
git branch
```
You should see you're on `master`.

---

4. **Make sure `master` is up to date**

```bash
git switch master
```

---

5. **MCreate new branch `xfusioncorp_blog` from master**

```bash
git branch xfusioncorp_blog
git switch xfusioncorp_blog
```

---

6. **Verify the branch**

```bash
git branch -a
```
You should now see both `master` and `xfusioncorp_blog`.

---

🎯 **Final Answer (commands only)**

```bash
cd /usr/src/kodekloudrepos/blog
git switch master
git branch xfusioncorp_blog
git switch xfusioncorp_blog
```

---