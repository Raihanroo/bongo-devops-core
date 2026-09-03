# BongoDev DevOps Core - Phase 2: The Engineer's Workflow

This repository contains the practical implementations and hands-on exercises for **Phase 2 (Tasks 06 - 10)** of the BongoDev DevOps & Backend Engineering program. The focus of this phase is mastering advanced Git workflows, history investigation, context switching, clean merging (squashing), conflict resolution, and emergency recovery.

---

## 🛠️ Summary of Completed Tasks

### **Task 06: The "History Detective"**
* **Objective:** Investigate commit histories and trace back modifications to specific configuration files.
* **Implementation:** Created and modified `server.conf` across multiple commits to track changes, utilizing `git log -p` and `git blame` to identify authors and commit hashes.

### **Task 07: The "Safety Net"**
* **Objective:** Manage untracked and modified files during emergency context switches.
* **Implementation:** Used `git stash -u` to safely store incomplete optimization work (`main.py`) while switching contexts to address an urgent production bug (`hotfix.py`), later restoring the workspace seamlessly using `git stash pop`.

### **Task 08: The "Clean Merge"**
* **Objective:** Consolidate messy, incremental commits into a single clean commit on the main branch.
* **Implementation:** Developed optimization steps on `feature/system-optimization` (`kernel_tuning.txt`), merged back using `git merge --squash`, and finalized with a clean, descriptive commit message.

### **Task 09: The "Conflict Resolution"**
* **Objective:** Simulate and manually resolve merge conflicts in collaborative settings.
* **Implementation:** Created concurrent conflicting changes on `app_config.txt` between `main` and `feature/config-update`, triggered a merge conflict, manually resolved conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`), and finalized the merge.

### **Task 10: The "Time Machine"**
* **Objective:** Recover "lost" or deleted commits using Git reflog.
* **Implementation:** Simulated a nuclear command (`git reset --hard HEAD~1`) to discard a temporary commit, investigated the state history via `git reflog`, and successfully recovered the exact commit state using `git reset --hard <commit-hash>`.

---

## 🚀 How to Verify
Run the following git commands to inspect the commit logs and project history:
```bash
git log --oneline --graph --all
git reflog