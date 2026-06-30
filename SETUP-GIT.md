# Publishing This Repo to GitHub (Beginner Guide)

You only do steps 1–3 once on your machine. Steps 4 onward are the repo setup.

## 1. Install Git
Check first by opening a terminal and running:
```
git --version
```
If there's no version, install from https://git-scm.com/downloads (default options).

## 2. Tell Git who you are
```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## 3. Create a GitHub account
Sign up at https://github.com using the same email as above.

## 4. Create the empty repo on GitHub
On github.com: click **+** (top right) > **New repository**.
- Name: `sentinel-kql-hunting-library`
- Visibility: **Public**
- Do NOT add a README, .gitignore, or license (this folder already has them)
- Click **Create repository**, then copy the repo URL shown.

## 5. Open a terminal inside this folder
```
cd path/to/sentinel-kql-hunting-library
```
(Tip: type `cd ` then drag the folder into the terminal and press Enter.)

## 6. Initialise and make the first commit
```
git init
git add .
git commit -m "Initial scaffold: repo structure, docs, and Identity domain queries"
```

## 7. Connect to GitHub and push
Replace the URL with the one you copied in step 4:
```
git branch -M main
git remote add origin https://github.com/<your-username>/sentinel-kql-hunting-library.git
git push -u origin main
```
The first push will prompt you to sign in — follow the browser pop-up.

## 8. The everyday cycle after that
Each time you add more queries:
```
git add .
git commit -m "Add Endpoint domain: LOLBin and process tree queries"
git push
```

## Before you publish — fill in placeholders
Search the project for `<Your Name>` and replace it (in `LICENSE`, `README.md`,
and each `.kql` header). Also update the `[LinkedIn]` and `[GitHub]` links in
`README.md`.
