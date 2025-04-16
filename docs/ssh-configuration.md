# 🔐 SSH Configuration

Set up SSH key access between your local machine and GitHub.

---

## 🧠 Managing Multiple SSH Keys

If you're using more than one SSH key (e.g. for personal and work accounts), here's an example configuration:

![SSH Config](../images/ssh/current%20ssh%20config.png)

### Current SSH Directory Sample

Here’s what my `.ssh` directory look like: ![SSH Directory](../images/ssh/ssh.png)

---

## 🚫 Common Issue: Git Push Error

You might encounter this error when pushing to a repo with incorrect SSH setup:

![Git Push Error](../images/ssh/git%20push%20error.png)

---

## 🛠 Commands to Set It Up

Run the following commands to add your SSH key:

```bash
eval "$(ssh-agent)"
ssh-add ~/.ssh/id_shoplab
```

![commands](../images/ssh/add%20git%20config.png)

## ✅ Test Your SSH Connection

To check if everything is working: ![commands](../images/ssh/git%20check%20connection.png)

## 🚀 Push to GitHub

Once connected, pushing should work as expected: ![push](../images/ssh/git%20push.png)
