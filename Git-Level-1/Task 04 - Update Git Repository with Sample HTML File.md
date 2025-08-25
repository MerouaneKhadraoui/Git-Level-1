# Task 4: Update Git Repository with Sample HTML File

## Question

The Nautilus development team has initiated a new project development, establishing various Git repositories to manage each project's source code. Recently, a repository named `/opt/games.git` was created. The team has provided a sample `index.html` file located on the `jump host` under the `/tmp` directory. This repository has been cloned to `/usr/src/kodekloudrepos` on the `storage server` in the `Stratos DC`.

**Task:**

1. Copy the sample `index.html` file from the `jump host` to the `storage server` placing it within the cloned repository at `/usr/src/kodekloudrepos/games`.

2. Add and commit the file to the repository.

3. Push the changes to the `master` branch.

---

## Solution

1. **Copy the index.html file to the cloned repo**

From the **jump host**:

```bash
scp /tmp/index.html natasha@ststor01:/home/natasha
sudo mv index.html /usr/src/kodekloudrepos/games/
ssh natasha@ststor01
# password: Bl@kW
```

Then SSH into the storage server:

```bash
ssh natasha@ststor01
# password: Bl@kW
```

---

2. **Go to the cloned repository**

```bash
cd /usr/src/kodekloudrepos/games
```

---

3. **Verify the file is there**

```bash
ls -l index.html
```

---

4. **Add the file to Git staging area**

```bash
sudo git add index.html
```

---

5. **Add the file to Git staging area**

```bash
sudo git commit -m "Add sample index.html file"
```

---

6. **Push the changes to the master branch**

```bash
sudo git push origin master
```

---

## Verification

- Check commit history:

```bash
sudo git log --oneline
```

- Ensure `index.html` is in the repo:

```bash
sudo git ls-files
```