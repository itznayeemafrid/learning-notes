
#### 📝 **Git Basics**
- `git --version` _Check if Git is installed and view the current version._
	
- `git config --global user.name "My Name"`  _Set your global Git username._
	
- `git config --global user.email "whatever@mail.com"`  _Set your global Git email._
	
- `git config --list` _Display the current Git configuration._

#### 🛠 **Working with Repositories**

- `git init` _Initialize a new Git repository in the current directory._
    
- `git clone <repo_url>` _Clone an existing repository from a URL._
    
- `git status` _Show the current status of your repository (which files are staged, modified, etc.)._
    
- `git add <filename>` _Stage a specific file for commit._
    
- `git add .` _Stage all changes in the current directory for commit._
    
- `git commit -m "commit message"` _Commit staged changes with a message._
    
- `git push origin <branch_name>` _Push your local commits to the remote repository on the specified branch._
    
- `git pull` _Fetch and merge changes from the remote repository._
    
- `git fetch` _Fetch changes from the remote repository without merging them._
    
- `git remote add origin <repo_url>` _Add a remote repository with a URL to your local repository._
    
- `git remote -v` _View the remote repositories associated with your local repository._
    

#### 🔄 **Branching and Merging**

- `git branch` _List all local branches in the current repository._
    
- `git branch <branch_name>` _Create a new branch._
    
- `git checkout <branch_name>` _Switch to a different branch._
    
- `git checkout -b <branch_name>` _Create a new branch and switch to it immediately._
    
- `git merge <branch_name>` _Merge changes from the specified branch into the current branch._
    
- `git branch -d <branch_name>` _Delete a branch that has been merged._
    

#### 🛠 **Viewing History**

- `git log` _View the commit history for the current branch._
    
- `git log --oneline` _View a simplified commit history (one line per commit)._
    
- `git diff` _Show changes between the working directory and the staging area._
    
- `git diff <file>` _Show changes for a specific file._
    

#### ⏳ **Undoing Changes**

- `git restore <file>` _Restore a file from the last commit (undo changes in the working directory)._
    
- `git checkout -- <file>` _Discard changes in the working directory for a specific file (same as restore)._
    
- `git reset <file>` _Unstage a file (keep changes in the working directory)._
    
- `git reset --hard` _Reset the repository to the last commit (discard local changes completely)._
    
- `git revert <commit>` _Revert a commit by creating a new commit that undoes the changes of the specified commit._
    

#### 🖥 **Terminal Basics**

- `ls` _List the files and directories in the current directory._
    
- `ls -a` _List all files, including hidden files._
    
- `pwd` _Print the current working directory._
    
- `cd <directory>` _Change the current directory to the specified path._
    
- `cd ..` _Go up one directory level._
    
- `clear` _Clear the terminal screen._
    
- `mkdir <directory_name>` _Create a new directory._
    
- `rm <file>` _Remove a file._
    
- `rm -r <directory>` _Remove a directory and its contents._
    
- `touch <file>` _Create a new empty file._
    
- `cat <file>` _Display the contents of a file._
    
- `echo <text>` _Print text to the terminal._
    
- `man <command>` _View the manual (help) for a command._
    

#### ✨ **Advanced Git Commands**

- `git stash` _Save your uncommitted changes temporarily and revert to the last commit._
    
- `git stash pop` _Apply stashed changes back into the working directory._
    
- `git rebase <branch>` _Rebase your current branch on top of another branch._
    
- `git tag <tag_name>` _Create a tag for a specific commit._
    
- `git tag -d <tag_name>` _Delete a tag._
    
- `git show <commit_id>` _Show detailed information about a specific commit._
    

#### 💡 **Git Aliases**

- `git config --global alias.co checkout` _Create an alias for `git checkout` (use `git co` instead)._
    
- `git config --global alias.st status` _Create an alias for `git status` (use `git st` instead)._
    
- `git config --global alias.ci commit` _Create an alias for `git commit` (use `git ci` instead)._
    
- `git config --global alias.br branch` _Create an alias for `git branch` (use `git br` instead)._