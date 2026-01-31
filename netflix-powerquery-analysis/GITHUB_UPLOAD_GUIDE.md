# GitHub Upload Guide

Follow these steps to upload your Netflix Power Query Analysis project to GitHub.

## Method 1: Using GitHub Website (Easiest for Beginners)

### Step 1: Create a New Repository on GitHub

1. Go to [GitHub.com](https://github.com) and log in
2. Click the **"+"** icon in the top right corner
3. Select **"New repository"**
4. Fill in the repository details:
   - **Repository name**: `netflix-powerquery-analysis` (or your preferred name)
   - **Description**: "Netflix data cleaning and analysis project using Power Query - Week 4 Mentorship Project"
   - **Visibility**: Choose "Public" (recommended for portfolio) or "Private"
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
5. Click **"Create repository"**

### Step 2: Prepare Your Local Files

1. Download the complete `netflix-powerquery-analysis` folder from this conversation
2. Extract it to a location on your computer (e.g., Desktop or Documents)

### Step 3: Install Git (if not already installed)

**Windows:**
- Download from [git-scm.com](https://git-scm.com/download/win)
- Run the installer with default settings

**Mac:**
- Open Terminal and run: `git --version`
- If not installed, follow the prompts to install

**Linux:**
```bash
sudo apt-get install git  # Ubuntu/Debian
sudo yum install git      # CentOS/RHEL
```

### Step 4: Upload Using Git Commands

Open Terminal (Mac/Linux) or Git Bash (Windows) and navigate to your project folder:

```bash
# Navigate to your project folder
cd path/to/netflix-powerquery-analysis

# Initialize git repository
git init

# Add all files
git add .

# Create your first commit
git commit -m "Initial commit: Netflix Power Query Analysis project"

# Add your GitHub repository as remote
# Replace YOUR_USERNAME with your actual GitHub username
git remote add origin https://github.com/YOUR_USERNAME/netflix-powerquery-analysis.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 5: Verify Upload

1. Go to your GitHub repository URL
2. Verify all files and folders are present
3. Check that README.md displays correctly on the main page

---

## Method 2: Using GitHub Desktop (User-Friendly GUI)

### Step 1: Install GitHub Desktop

1. Download from [desktop.github.com](https://desktop.github.com)
2. Install and sign in with your GitHub account

### Step 2: Create Repository

1. Click **"File"** → **"New Repository"**
2. Fill in:
   - **Name**: netflix-powerquery-analysis
   - **Local Path**: Choose where to save
   - **Git Ignore**: None (we already have .gitignore)
   - **License**: MIT (already included)
3. Click **"Create Repository"**

### Step 3: Add Your Files

1. Copy all files from the downloaded `netflix-powerquery-analysis` folder
2. Paste them into the repository folder GitHub Desktop created
3. GitHub Desktop will automatically detect the changes

### Step 4: Commit and Push

1. In GitHub Desktop, you'll see all files in the "Changes" tab
2. Add a commit message: "Initial commit: Netflix Power Query Analysis project"
3. Click **"Commit to main"**
4. Click **"Publish repository"**
5. Choose visibility (Public/Private)
6. Click **"Publish Repository"**

---

## Method 3: Drag and Drop (Simple but Limited)

### For Small Files Only

1. Create new repository on GitHub (as in Method 1, Step 1)
2. Click **"uploading an existing file"** link
3. Drag and drop files/folders
4. Add commit message
5. Click **"Commit changes"**

**Note:** This method has file size limits and can be slower for many files.

---

## After Uploading

### 1. Verify Your Repository

Check that all these items are present:
- ✅ README.md (displays on main page)
- ✅ data/ folder with netflix_titles.csv
- ✅ outputs/ folder with Excel and Power BI files
- ✅ docs/ folder with report
- ✅ presentations/ folder with PowerPoint
- ✅ LICENSE file
- ✅ .gitignore file
- ✅ SETUP.md
- ✅ CONTRIBUTING.md
- ✅ DATA_DICTIONARY.md

### 2. Customize Your Repository

**Edit README.md** (if needed):
- Click on README.md
- Click the pencil icon (Edit)
- Make changes
- Commit changes

**Add Topics** (tags for discoverability):
1. Click the gear icon next to "About"
2. Add topics like: `power-query`, `data-cleaning`, `netflix`, `data-analysis`, `excel`, `power-bi`

**Pin Repository** (to show on your profile):
1. Go to your GitHub profile
2. Click "Customize your pins"
3. Select this repository

### 3. Share Your Work

Your repository URL will be:
```
https://github.com/YOUR_USERNAME/netflix-powerquery-analysis
```

Share this on:
- LinkedIn (great for portfolio)
- Resume/CV
- Mentorship program submissions
- Portfolio website

---

## Troubleshooting

### Problem: "Git is not recognized..."
**Solution:** Git is not installed or not in PATH. Reinstall Git and restart your terminal.

### Problem: "Permission denied (publickey)"
**Solution:** Set up SSH keys or use HTTPS with username/password or personal access token.

### Problem: Files too large to upload
**Solution:** 
- GitHub has a 100MB file size limit
- Use Git LFS for large files: `git lfs track "*.pbix"`
- Or provide download links to large files instead

### Problem: "Repository already exists"
**Solution:** 
- Choose a different repository name, or
- Delete the existing repository first (if it's yours)

---

## Best Practices

1. **Write descriptive commit messages**
   - Good: "Add data cleaning documentation"
   - Bad: "Update"

2. **Keep repository organized**
   - Use clear folder structure
   - Document everything
   - Remove unnecessary files

3. **Update regularly**
   - Add improvements as you learn
   - Keep documentation current
   - Respond to issues/questions

4. **Protect sensitive data**
   - Never commit passwords or API keys
   - Use .gitignore for sensitive files
   - Review files before committing

---

## Need Help?

- [GitHub Documentation](https://docs.github.com)
- [Git Tutorial](https://git-scm.com/docs/gittutorial)
- [GitHub Community](https://github.community)

---

**Congratulations!** 🎉 Your Netflix Power Query Analysis project is now on GitHub!
