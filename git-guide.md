## 1️⃣ One-Time Global Git Setup (Required)

Run once on your system:

```
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

✅ Verify
```
git config --global --list
```

## 2️⃣ Open Project Folder

```
cd path/to/your/project
```

## 3️⃣ Initialize Git Repository

Check if Git is already initialized:

```
git status
```

If you see not a git repository, run:
```
git init
git branch -M main
```

## 4️⃣ Add GitHub Remote
```
git remote add origin https://github.com/<org-or-user>/<repo-name>.git
```

✅ Verify
```
git remote -v
```

## 5️⃣ First Commit (on main)
```
git add .
git commit -m "Initial commit"
```

## 6️⃣ Push main (One Time Only)
```
git push -u origin main
```

⚠️ After this, do not develop directly on main

## 7️⃣ Create and Switch to develop Branch
```
git checkout -b develop
```
✅ Verify
```
git branch
```

## 8️⃣ Push develop Branch (One Time)
```
git push -u origin develop
```

## 9️⃣ Daily Development Workflow (IMPORTANT)
Always confirm branch
```
git branch
```

If not on develop:
```
git checkout develop
```

Make code changes, then:
```
git status
git add .
git commit -m "Meaningful commit message"
git push
```

## 🔟 Common Safety Checks (DO THIS ALWAYS)

Check branch
```
git branch
```

Check uncommitted files
```
git status
```

Check remote
```
git remote -v
```

## 🔁 Optional: Feature Branch Workflow
```
git checkout develop
git checkout -b feature/login-api
```

After work:
```
git add .
git commit -m "Add login API"
git push -u origin feature/login-api
```

Create PR → feature/* → develop

# Pull Request dont do it 
##🚀 Merging Develop to Main (Release)
```
git checkout main
git pull origin main
git merge develop
git push origin main
```
