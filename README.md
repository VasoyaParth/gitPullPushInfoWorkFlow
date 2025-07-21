# 📘 Git Daily Workflow Guide (Feature Branches + Merge to Main)

This guide shows how to create a clean Git workflow for daily work using a date-named feature branch, and merge it professionally into `main`.

---

## 🛠 Prerequisites

- Git installed
- A GitHub repo created (empty or initialized with README)
- Terminal or Git Bash

---

## 🧭 Step-by-Step Workflow (Day Start to Finish)

### 1. 📂 Initialize your project (only once)
```bash
git init
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
2. 🗂 Create & switch to a new daily branch
bash
Copy
Edit
# Example: for July 21, 2025
git checkout -b feature-2025-07-21
3. ➕ Stage and commit your work
bash
Copy
Edit
git add .
git commit -m "Work done on 2025-07-21: [Your notes here]"
4. 🚀 Push your daily branch to GitHub
bash
Copy
Edit
git push -u origin feature-2025-07-21
5. ✅ Switch to main and pull latest (to avoid conflicts)
bash
Copy
Edit
git checkout main
git pull origin main
6. 🔁 Merge daily branch into main
bash
Copy
Edit
git merge feature-2025-07-21
7. ⬆ Push updated main to GitHub
bash
Copy
Edit
git push origin main
8. 🧹 (Optional) Clean up old feature branches
bash
Copy
Edit
git branch -d feature-2025-07-21              # Delete locally
git push origin --delete feature-2025-07-21   # Delete on GitHub
🧯 Common Issues & Fixes
🔗 “Unrelated histories” (only first time)
If git pull gives this error:

vbnet
Copy
Edit
fatal: refusing to merge unrelated histories
Use:

bash
Copy
Edit
git pull origin main --allow-unrelated-histories
🚫 Push rejected (main is ahead remotely)
bash
Copy
Edit
git pull origin main
# Then resolve, commit, and push again:
git push origin main
💡 Tips
Always commit before switching branches

Use date-based names like feature-YYYY-MM-DD for clarity

Always pull before pushing to avoid rejections

Created with ❤️ by [YourName]

yaml
Copy
Edit

---

## 🔄 You can use this every day like:

```bash
git checkout -b feature-2025-07-22
# do work
git add .
git commit -m "Work for 22 July"
git push -u origin feature-2025-07-22

git checkout main
git pull origin main
git merge feature-2025-07-22
git push origin main
