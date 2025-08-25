# Final Exam

## Question 1 (Weight: 18)

Recently a bare repository was created by one of the developers. Now, they were planning to add some content in this repository so this needs to be cloned somewhere so that one of the developers can start adding data in it. Below you can find more details.

Clone the repository `/opt/story-blog-t1q11.git` under sarah user's home on storage server.

Use below credentials to SSH into the storage server and to complete this task.

`Username`: sarah

`Password`: S3cure321

---

## Question 2 (Weight: 18)

The Nautilus dev team is currently in the process of creating Git repositories, a new requirement has emerged to create a repository on the storage server. Below are the details for this request.

Create and initialise a git repository at `/home/sarah/story-blog-t1q3` on Storage server.

Use below credentials to SSH into the storage server and to complete this task.

`Username`: sarah

`Password`: S3cure321

---

## Question 3 (Weight: 24)

A couple of new Git repositories were created recently and this is still in progress. Recently a new requirement has emerged to create a repository on the storage server. Below are the details for this request.


1. Create and initialize a git repository at `/home/sarah/story-blog-t1q4` on Storage server.

2. Let's add a file named `lion-and-mouse-t1q4.txt` to our project inside `/home/sarah/story-blog-t1q4`, the file content must be `A Lion lay asleep in the forest`.

Use below credentials to SSH into the storage server and to complete this task.

`Username`: sarah

`Password`: S3cure321

---

## Question 4 (Weight: 24)

A new repository named `/usr/src/kodekloudrepos/cluster-t2q5` was created recently and some data was added in it. Now one of the developers wanted to use this repository further to add/update some data.


Checkout the `master` branch under repo `/usr/src/kodekloudrepos/cluster-t2q5`.

Use below credentials to SSH into the storage server and to complete this task.

`Username`: sarah

`Password`: S3cure321

---

## Question 5 (Weight: 16)

The Nautilus application development team has been working on a project repository `/opt/cluster-t2q3.git`. This repo is cloned at `/usr/src/kodekloudrepos/cluster-t2q3` on `storage server` in `Stratos DC`. They recently shared the following requirements with DevOps team:


Create a new branch `nautilus-t2q3` in `/usr/src/kodekloudrepos/cluster-t2q3` repo from `master` and copy the `/tmp/index-t2q3.html` file (present on `storage server` itself) into the repo. Further, `add/commit` this file in the new branch and merge back that branch into `master` branch. Finally, push the changes to the origin for both of the branches.

Use below credentials to SSH into the storage server and to complete this task.

`Username`: sarah

`Password`: S3cure321


---

## Solution 5

1. **SSH into the storage server**

```bash
ssh sarah@ststor01
# password: S3cure321
```

2. **Navigate to the repo**

```bash
cd /usr/src/kodekloudrepos/cluster-t2q3
```

3. **Check current branch**

```bash
git status
git branch
```
Make sure you're on `master`.

4. **Create and switch to new branch**

```bash
git checkout -b nautilus-t2q3
```

5. **Copy the file into repo**

```bash
cp /tmp/index-t2q3.html .
```

6. **Stage and commit the file**

```bash
git add index-t2q3.html
git commit -m "Added index-t2q3.html file"
```

7. **Switch back to master branch**

```bash
git checkout master
```

8. **Merge the new branch into master**

```bash
git merge nautilus-t2q3
```

9. **Push both branches to origin**

```bash
git push origin master
git push origin nautilus-t2q3
```

10. **Verify**

```bash
git log --oneline --graph --all
```

---

