Let’s walk through **creating your first Freestyle Jenkins job** step-by-step. 
---

## 🚀 Step-by-Step: Create Your First Freestyle Jenkins Job

### ✅ Prerequisites:

* Jenkins is running at `http://localhost:8080`
* You're logged in as the admin
* You have internet access for pulling from GitHub

---

### 🛠️ Step 1: Create a New Freestyle Project

1. On the Jenkins dashboard, click on **“New Item”** (left menu).
2. Enter an item name:
   👉 e.g., `first-freestyle-job`
3. Select **“Freestyle project”**
4. Click **“OK”**

---

### ⚙️ Step 2: Configure the Job

Once inside the job configuration page:

#### (a) **Description** (Optional)

* Add a short description like:
  *“This job prints Hello World to console”*

#### (b) **Source Code Management**

* Select **Git**
* In the **Repository URL**, enter:

  ```
  https://github.com/Manoj-Kumar-Selvaraj/Jenkins_Handson.git
  ```
* If it prompts for credentials, skip for now (we’re just cloning public content)

#### (c) **Build Triggers**

* Leave it unchecked for now (we’ll learn scheduling later)

#### (d) **Build Steps**

1. Click **“Add build step”**
2. Select **“Execute shell”** (Linux/macOS) or **“Execute Windows batch command”** (Windows)
3. Add this command:

   ```bash
   echo "Hello from Jenkins!"
   ```

---

### 💥 Step 3: Save and Build

1. Click **“Save”**
2. On the project page, click **“Build Now”**
3. Wait a few seconds, then click the build in the **Build History** section (left panel)
4. Click **“Console Output”** and confirm you see:

   ```
   Hello from Jenkins!
   ```

---

### 📸 Step 4: Document and Commit

Take **screenshots** of:

* Job configuration
* Console output
* Build success status

Place them under:

```
freestyle_job/screenshots/
```

Also, save/export your job config as XML:

* Go to `http://localhost:8080/job/first-freestyle-job/config.xml`
* Save it as `job_config.xml`

---

Let me know once you're done, and we’ll move on to using **parameters, GitHub integration, or pipelines** next. Would you like help with Git commit commands too?
