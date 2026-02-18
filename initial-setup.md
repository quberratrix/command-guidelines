# ✅ Option 1 (BEST): Change origin to company repo

Since this project now belongs to the company, just replace the remote.

## 1️⃣ Remove old remote
```
git remote remove origin
```

## 2️⃣ Add company repo as new origin
```
git remote add origin https://github.com/quberratrix/qubemusic-api.git
```

Check:
```
git remote -v
```

Now it should show the new repo.

## 3️⃣ Pull company README commit (important)

Because company repo already has an initial commit:
```
git pull origin main --allow-unrelated-histories
```

If merge editor opens → just save & close.

## 4️⃣ Create a branch (recommended)
```
git checkout -b initial-setup
```

## 5️⃣ Push your code
```
git push origin initial-setup
```

Then create Pull Request → initial-setup → main.

✅ Done — clean history, correct workflow.
