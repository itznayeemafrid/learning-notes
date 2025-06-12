
### 1. Git Not Recognized in VS Code Terminal

**Issue:**  
Git command 'git --version' shows error in VS Code:

**Solution:**

- During Git installation, make sure to **tick**:  ✅ _"Add Git to the system PATH"_

- If you **missed** this step during installation, do the following:
    1. Search for **Edit the system environment variables** in the Windows search bar.
    2. In the **System Properties** window, go to the **Advanced** tab → click **Environment Variables**.
	3. Under **System variables**, select **Path** → click **Edit**.
	4. Click **New** and paste the path: `C:\Program Files\Git\bin`
	5. Click **OK** on all windows.
	6. **Restart VS Code.**

---
### 2. Create Classic Token in Github

**Issue:**  
Creating a Personal Access Token (PAT) instead of password:

**Solution:**

- On Linux, Git does not use Git Credential Manager (GCM) by default & GitHub has disabled password authentication, so you must use a Personal Access Token (PAT) instead of a password.

- Login to your github account and do the following:
	1. Click your profile photo (top-right corner).
	2. Select **“Settings”**.
	3. Scroll down in the left sidebar and click:  **Developer settings → Personal access tokens → Tokens (classic)**
	4. Click “Generate new token (classic)”
	5. Give your token a name, choose expiration time, check all the permissions, click **Generate token** at the bottom.
	6. GitHub will now show you the **token string only once**. **Copy it immediately** and save it in a secure place (like a password manager or encrypted notes).
	7. **Use Credential Helper (Recommended)**
		- This will **temporarily store your token in memory** for 15 minutes (default) & the other method will store for 1 hour (3600 seconds). So that you don't have to paste it every time.
			`git config --global credential.helper cache`  Or
			`git config --global credential.helper 'cache --timeout=3600'`
	8. Now use this instead of password. But if it doesn't work directly as password then:
			`git remote set-url origin https://<the classic token you copied>@github.com/<username>/<repo>`

### 2. Turn Master directory into Main

**Issue:**  
instead of using `* master` as the default directory turn it into `* main` directory:

**Solution:**

- On Linux, sometimes there's only master directory which causes issue while pushing to origin main cause the default in github is main but local repo doesn't have main. It only has master.

- Open the local repo folder in Terminal and follow along:
	1. Initialize Git (if you haven't already) --> `git init`
	2. Check the current branch name --> `git branch`
	3. Rename the `master` branch to `main` --> `git branch -m master main`
	4. Add your files and commit (if not done yet)
	5. Push to GitHub with `main` as the branch --> `git push -u origin main`
	6. If it doesn't work the force overwrite the main brush of remote repo to push --> `git push --force origin main`
	7. If you have more than one branch then like `master` and `main` both, then jump to any branch with --> `git switch main`