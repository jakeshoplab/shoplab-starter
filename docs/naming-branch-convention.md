# 🌿 Naming Branch Convention

## ✨ Creating a New Feature

Use the prefix: `feat`

---

## 🐞 Updates or Bug Fixes

Use the prefix: `fix`

---

## 🧱 Branch Name Format

Format:  
`<type>/<ticket-id>`

Examples:
- `feat/scm-2`
- `fix/scm-2`

---

## 🔎 Where to Find the Ticket ID

Go to **Jira** and look for the ticket assigned to you.  
Here are a few examples:

**Backlogs:**  
> ![Backlog Ticket ID Location](../images/backlog-ticket-id-locations.webp)

**Sprint Kanban:**  
> ![Active Sprint Kanban Ticket ID](../images/active-sprints-kanban-ticket-id-location.webp)

**Sprint Kanban Modal:**  
> ![Sprint Modal Ticket ID](../images/active-sprints-kanban-modal-ticket-id-location.webp)

---

## 🚀 Creating the Branch

```bash
# Make sure you're on the master branch first
git checkout master
git pull

# For features
git checkout -b feat/scm-2

# For fixes or updates
git checkout -b fix/scm-2
