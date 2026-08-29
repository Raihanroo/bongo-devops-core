
# Bongo DevOps Core - Phase 1 Documentation

This repository contains the complete implementation of **Phase 1: The Foundations (Basics)** for the bongoDev DevOps & Cloud Engineering course.

---

## 🛠️ Step-by-Step Command Documentation

### Task 01: Identity & Setup
Configured Git global user identity, initialized local repository, created README, and made the initial commit.

```bash
git config --global user.name "Raihan Islam"
git config --global user.email "raihanroo21@gmail.com"
git init
echo "# Bongo DevOps Core" > README.md
git add README.md
git commit -m "chore: initial repository setup"

Task 02: .gitignore (.env Protection)
Created a sensitive environment file and configured .gitignore to prevent tracking secrets.

Bash
echo "DB_PASSWORD=supersecretpassword123" > .env
echo ".env" > .gitignore
git status
git add .gitignore
git commit -m "feat: add gitignore to protect sensitive files"

Task 03: Feature Branching
Created and worked inside a feature branch to keep experimental tuning configurations separate from the production branch.

Bash
git checkout -b feature/system-optimization
echo "kernel optimization settings" > kernel_tuning.txt
git add kernel_tuning.txt
git commit -m "feat: add kernel tuning configuration"
git checkout main

Task 04: Selective Staging
Staged and committed fixes separately to maintain a clean atomic commit history.

Bash
echo "web config" > web_fix.conf
echo "db config" > db_fix.conf

# Commit 1
git add web_fix.conf
git commit -m "fix: resolve web server configuration issue"

# Commit 2
git add db_fix.conf
git commit -m "fix: resolve database configuration issue"


Task 05: GitHub Remote Connection & Push
Linked local repository to remote GitHub repository and pushed all branches.

Bash
git remote add origin [https://github.com/Raihanroo/bongo-devops-core.git](https://github.com/Raihanroo/bongo-devops-core.git)
git branch -M main
git push -u origin main
git push origin feature/system-optimization

Final Merge & Synchronization
Merged feature/system-optimization branch into main via GitHub Pull Request (PR #1) and synchronized local main branch.

Bash
git checkout main
git pull origin main
