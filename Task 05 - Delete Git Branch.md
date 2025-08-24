# Task 5: Delete Git Branch

## Question

The Nautilus developers are engaged in active development on one of the project repositories located at `/usr/src/kodekloudrepos/official`. During testing, several test branches were created, and now they require cleanup. Here are the requirements provided to the DevOps team:

**Task:**

On the `Storage server` in Stratos DC, delete a branch named `xfusioncorp_official` from the `/usr/src/kodekloudrepos/official` Git repository.

---

## Solution

1. **SSH into the Storage server**

```bash
ssh natasha@ststor01
```

2. **Navigate to the repo path**

```bash
cd /usr/src/kodekloudrepos/official
```

3. **Check the branches**

```bash
git branch
```

You should see something like:

```css
* `master`
  xfusioncorp_official
```

4. **Delete the branch**

⚠️ You cannot delete the branch you are currently on.
So first, switch to another branch (e.g., `master`):

```bash
git checkout master
```

Then delete the branch:

```bash
git branch -d xfusioncorp_official
```

If Git refuses because it's not fully merged and you are sure you want it gone, force delete it:

```bash
git branch -D xfusioncorp_official
```

5. **Verify**

```bash
git branch
```

The branch `xfusioncorp_official` should no longer appear.