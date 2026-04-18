# How to populate this folder for GitHub

Run these commands from the workspace root to copy all files:

```bash
# Copy frontend files
cp -r web/* gedamu-electronics-github/frontend/

# Copy backend files
cp server/index.js gedamu-electronics-github/backend/
cp server/db.js gedamu-electronics-github/backend/
cp -r server/middleware gedamu-electronics-github/backend/
cp -r server/routes gedamu-electronics-github/backend/
cp -r server/services gedamu-electronics-github/backend/
```

Then push to GitHub:
```bash
cd gedamu-electronics-github
git init
git add .
git commit -m "Initial commit — Gedamu Electronics"
git remote add origin https://github.com/YOUR_USERNAME/gedamu-electronics.git
git push -u origin main
```
