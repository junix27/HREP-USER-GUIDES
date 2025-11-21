# User Guide: Adding a Collaborator to a Private GitHub Repository

## Table of Contents
1. [Adding a Collaborator](#step-1-adding-a-collaborator)
2. [Accepting the Invitation](#step-2-accepting-the-invitation)
3. [Working with the Repository](#step-3-working-with-the-repository)

---

## Step 1: Adding a Collaborator

**⚠️ Important:** For private repositories, you must add someone as a collaborator before they can access it.

### Instructions for Repository Owner:

1. Navigate to your repository on **GitHub.com**

2. Click the **"Settings"** tab at the top of the page

3. In the left sidebar, click **"Collaborators"**

4. Click the **"Add people"** button (green button)

5. In the search box, enter the collaborator's:
   - GitHub username, OR
   - Email address

6. Select the correct person from the dropdown list

7. Choose their **permission level**:
   
   | Permission | What They Can Do |
   |------------|------------------|
   | Read | View and download code only |
   | Write | Push changes, create branches |
   | Admin | Full control including settings |
   
   **Recommended:** Choose **"Write"** for most collaborators

8. Click **"Add [username] to this repository"**

9. ✅ **Done!** GitHub will send them an email invitation

---

## Step 2: Accepting the Invitation

### Instructions for New Collaborator:

1. Check your **email inbox** for an invitation from GitHub

2. Open the email and click **"View invitation"**

3. On GitHub, click the **"Accept invitation"** button

4. ✅ **Success!** You now have access to the repository

---

## Step 3: Working with the Repository

The collaborator now has **two options** for working with the repository:

### Option A: Clone the Repository (Recommended for Team Members)

**Best for:** Regular team members who will contribute frequently

**Steps:**

1. Open your terminal or command prompt

2. Copy the repository URL from GitHub

3. Run the clone command:
   ```bash
   git clone https://github.com/owner-username/repository-name.git
   ```

4. Navigate into the folder:
   ```bash
   cd repository-name
   ```

5. Start working! You can:
   - Create branches
   - Make changes
   - Push directly to the repository

---

### Option B: Fork the Repository (Alternative Method)

**Best for:** Contributors who want their own copy

**Steps:**

1. Go to the repository page on GitHub

2. Click the **"Fork"** button (top-right corner)

3. Select where to create the fork (your account)

4. Wait for GitHub to create your copy

5. Clone **your forked copy**:
   ```bash
   git clone https://github.com/your-username/repository-name.git
   ```

6. To submit changes:
   - Push to your fork
   - Create a **Pull Request** to the original repository
   - Wait for the owner to review and merge

---

## Quick Reference

| Action | Who Does It | When |
|--------|-------------|------|
| Add collaborator | Repository Owner | First step |
| Accept invitation | New Collaborator | After receiving email |
| Clone or Fork | New Collaborator | After accepting invitation |

---

## Troubleshooting

**Problem:** Collaborator can't see the repository  
**Solution:** Make sure they accepted the invitation first

**Problem:** Clone says "repository not found"  
**Solution:** Check that you're using the correct repository URL and have been added as a collaborator

**Problem:** Can't push changes  
**Solution:** Verify you have "Write" or "Admin" permissions (not just "Read")

---
