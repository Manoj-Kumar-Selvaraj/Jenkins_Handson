Freestyle Job setup is done—great progress.

Let’s move to the **next item on the roadmap**:

---

## 🔧 **Step 2: Parameterized Freestyle Job**

This allows users to provide input (like a name, environment, branch, etc.) when running the job. It’s very useful in real CI/CD pipelines.

---

### 🎯 Goal:

Create a job that takes a **name as input**, and prints:

```
Hello, <name>! Welcome to Jenkins.
```

---

### 🛠️ Step-by-Step:

1. Go to your existing job (`first-freestyle-job`) or create a new one like `parameterized-job`.

2. Click **Configure**.

3. Scroll down to **"This project is parameterized"** and check the box.

4. Click **Add Parameter** → **String Parameter**

5. Fill in the details:

   * **Name**: `USERNAME`
   * **Default Value**: `Manoj`
   * **Description**: `Enter your name`

6. Go to **Build** section → Edit your existing **"Execute shell"** step (or add a new one).

7. Replace the command with:

   ```bash
   echo "Hello, $USERNAME! Welcome to Jenkins."
   ```

8. Click **Save**

---

### 🚀 Run It:

1. On the job page, click **“Build with Parameters”**
2. Enter a custom name (e.g., `Manoj Kumar`)
3. Click **Build**
4. Check **Console Output** for:

   ```
   Hello, Manoj Kumar! Welcome to Jenkins.
   ```

---

Once done, take a screenshot and commit it to your repo under:

```
parameterized_job/screenshots/
```

Let me know once you're done, and we’ll move to **GitHub-triggered jobs or Jenkinsfile pipelines** next. Want to go with Git integration or pipeline next?
