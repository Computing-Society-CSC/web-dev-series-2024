## **Git Command Cheat Sheet**

> If you are not sure about the function of a certain command, do not use it in a production environment, or you may lose data. Test it first in a tmp repo to understand its function.

### **1. Configuration**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| `git config --global user.name "Your Name"`  | Set your Git username globally.            | `git config --global user.name "Alice"` |
| `git config --global user.email "you@example.com"` | Set your Git email globally.                | `git config --global user.email "alice@example.com"` |

---

### **2. Repository Initialization**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| **`git init`**               | **Initialize a new Git repository in the current directory.** | `git init`                             |

---

### **3. Status and Logs**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| **`git status`**             | **View the status of the working directory and staging area.** | `git status`                          |
| **`git log`**                | **Show the commit history.**                     | `git log`                             |
| `git log --oneline`          | Display a simplified commit history.             | `git log --oneline`                   |

---

### **4. Staging and Committing**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| **`git add <file>`**         | **Stage a specific file for commit.**            | `git add index.html`                  |
| **`git add .`**              | **Stage all changes in the current directory.**  | `git add .`                           |
| **`git commit -m "message"`**| **Commit staged changes with a message.**        | `git commit -m "Initial commit"`      |

---

### **5. Rolling Back Changes**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| **`git restore <file>`**     | **Discard uncommitted changes to a file.**       | `git restore index.html`              |
| `git reset HEAD <file>`  | Unstage a file (keep changes in working directory). | `git reset HEAD index.html`           |
| `git reset --soft <commit-hash>` | Move HEAD to a previous commit; keep changes staged. | `git reset --soft a1b2c3`             |
| `git reset --mixed <commit-hash>` | Move HEAD to a previous commit; keep changes in working directory. | `git reset --mixed a1b2c3`            |
| `git reset --hard <commit-hash>` | Rollback to a specific commit; discard all changes. | `git reset --hard a1b2c3`             |
| `git revert <commit-hash>` | Create a new commit that undoes changes made by a specific commit. | `git revert a1b2c3`                   |

---

### **6. Branching**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| **`git branch`**             | **List all branches in the repository.**         | `git branch`                          |
| **`git branch <branch-name>`** | **Create a new branch.**                        | `git branch feature-login`            |
| **`git checkout <branch-name>`** | **Switch to a specific branch.**             | `git checkout feature-login`          |
| `git checkout -b <branch-name>` | Create and switch to a new branch.             | `git checkout -b feature-logout`      |

---

### **7. Merging**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| **`git merge <branch-name>`**| **Merge a branch into the current branch.**      | `git merge feature-login`             |

---

### **8. Remote Repositories**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| **`git remote add origin <url>`** | **Add a remote repository.**               | `git remote add origin https://github.com/user/repo.git` |
| **`git push origin <branch>`**   | **Push changes to a specific branch on the remote repository.** | `git push origin main`                |
| **`git pull origin <branch>`**   | **Pull updates from a specific branch on the remote repository.** | `git pull origin main`                |
| **`git clone <url>`**            | **Clone a repository into a new directory.**         | `git clone https://github.com/user/repo.git` |

---

### **9. Tagging**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| `git tag <tag-name>`         | Create a lightweight tag.                        | `git tag v1.0`                        |

---

### **10. Miscellaneous**
| **Command**                  | **Function**                                      | **Example**                            |
|------------------------------|--------------------------------------------------|----------------------------------------|
| `git stash`                  | Save changes for later without committing them.  | `git stash`                           |
| `git stash pop`              | Apply the most recent stashed changes.           | `git stash pop`                       |
| `git diff`                   | Show differences between working directory and staging area. | `git diff`                  |

---

### **Most Common Commands Summary**  
- **Repository Setup**: `git init`, `git remote add origin <url>`  
- **Tracking and Committing**: `git add`, `git commit -m`  
- **Branching and Merging**: `git branch`, `git checkout`, `git merge`  
- **Remote Operations**: `git push`, `git pull`, `git clone`

