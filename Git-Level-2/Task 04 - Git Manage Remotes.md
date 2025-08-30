# Day 26: Git Manage Remotes

## Question

The xFusionCorp development team added updates to the project that is maintained under `/opt/ecommerce.git` repo and cloned under `/usr/src/kodekloudrepos/ecommerce`. Recently some changes were made on Git server that is hosted on `Storage server` in `Stratos DC`. The DevOps team added some new Git remotes, so we need to update remote on `/usr/src/kodekloudrepos/ecommerce` repository as per details mentioned below:

**Task:**

a. In `/usr/src/kodekloudrepos/ecommerce` repo add a new remote `dev_ecommerce` and point it to `/opt/xfusioncorp_ecommerce.git` repository.

b. There is a file `/tmp/index.html` on same server; copy this file to the repo and add/commit to master branch.

c. Finally push `master` branch to this new remote origin.

---

## Solution

1. **Switch to Storage Server**

(Usually in KodeKloud you select the "Storage Server" from the terminal options.)

```bash
ssh natasha@ststor01
# password: Bl@kW
```

---

2. **Go to the repository**

```bash
cd /usr/src/kodekloudrepos/ecommerce
```

---

3. **Add the new remote**

Add the remote `dev_ecommerce` pointing to `/opt/xfusioncorp_ecommerce.git`:

```bash
git remote add dev_ecommerce /opt/xfusioncorp_ecommerce.git
```
👉 You can verify with:

```bash
git remote -v
```
You should see something like:

```bash
dev_ecommerce   /opt/xfusioncorp_ecommerce.git (fetch)
dev_ecommerce   /opt/xfusioncorp_ecommerce.git (push)
```
---

4. **Copy the file**

Copy `/tmp/index.html` into the repository:

```bash
cp /tmp/index.html .
```

---

5. **Add and commit**

```bash
git add index.html
git commit -m "Add index.html file"
```

---

6. **Push changes to the new remote**

Push the `master` branch to the new remote `dev_ecommerce`:

```bash
git push dev_ecommerce master
```

---

✅ Done!

This will satisfy all requirements:
1. Remote dev_ecommerce added.
2. index.html added and committed.
3. Pushed to the new remote.

---