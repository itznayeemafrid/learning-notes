
#### 1. Git Not Recognized in VS Code Terminal

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