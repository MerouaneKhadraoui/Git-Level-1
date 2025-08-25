# Task 1: Git Install and Create Repository

## Question

The Nautilus development team shared with the DevOps team requirements for new application development, setting up a Git repository for that project. Create a Git repository on `Storage server` in Stratos DC as per details given below:

**Task:**

1. Install `git` package using `yum` on `Storage server`.

2. After that, create/init a git repository named `/opt/ecommerce.git` (use the exact name as asked and make sure not to create a bare repository).

---

## Solution


**Step 1 - Switch to Storage Server**

In KodeKloud Engineer, you first connect to the Storage Server:

```bash
ssh natasha@ststor01
# password: Bl@kW
```

---

**Step 2 - Install Git**

Update repos and install `git` using yum:

```bash
sudo yum install git -y
```
Check if installed properly:

```bash
git -v
```
---

**Step 3 - Create Git Repository**

Create it in `/opt`:

```bash
sudo git init /opt/ecommerce.git
```

---

**Step 4 - Verify Repository**

Run:

```bash
ls -a /opt/ecommerce.git
```

You should see:
```bash
.  ..  .git
```

---
