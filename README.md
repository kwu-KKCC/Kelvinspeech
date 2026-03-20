# Kelvinspeech - AID Japan × 95% AI Presentation

A modern, AI-powered presentation about AID Japan's vision combining luxury hospitality with AI-native ventures.

**Live Demo**: https://speechslides-0324.vercel.app

---

## 📋 Table of Contents

1. [Getting Access](#getting-access)
2. [Project Setup](#project-setup)
3. [Development Workflow](#development-workflow)
4. [Making Changes](#making-changes)
5. [CI/CD Pipeline](#cicd-pipeline)
6. [Project Structure](#project-structure)
7. [Troubleshooting](#troubleshooting)

---

## 🔐 Getting Access

### Step 1: Request Repository Access

Ask the repo owner (Kelvin) to add you as a **Collaborator**:
- Go to: https://github.com/kwu-KKCC/Kelvinspeech/settings/access
- Click "Add people"
- Enter your GitHub username
- Select **Collaborator** role

### Step 2: Verify Access

Once added, you'll receive an invitation email. Accept it and verify you can see:
- https://github.com/kwu-KKCC/Kelvinspeech

---

## 🚀 Project Setup

### Prerequisites

- Git (install from https://git-scm.com)
- A text editor (VS Code, Sublime, etc.)
- GitHub account (https://github.com)

### Clone the Repository

```bash
# Copy and run in your terminal
git clone https://github.com/kwu-KKCC/Kelvinspeech.git
cd Kelvinspeech
```

### Verify Setup

```bash
# Check git is configured
git status
git log --oneline
```

You should see:
- ✅ On branch `main`
- ✅ 2 commits visible

---

## 💻 Development Workflow

### 1. Start a New Task

```bash
# Make sure you're on main and updated
git checkout main
git pull origin main

# Create a new branch for your changes
git checkout -b feature/your-feature-name
# Examples:
# git checkout -b feature/add-new-slide
# git checkout -b feature/fix-text-alignment
# git checkout -b feature/update-styling
```

### 2. Make Changes

Edit `index.html` or other files in your editor:
- Open the file
- Make your changes
- Save the file

### 3. Test Locally

Open `index.html` in your browser:
- **Option A**: Double-click `index.html` in file explorer
- **Option B**: Right-click → Open with Browser
- **Option C**: Use VS Code Live Server extension

Navigate through slides to verify changes look good.

### 4. Commit Your Changes

```bash
# Check what changed
git status

# Stage your changes
git add index.html
# Or add multiple files:
git add .

# Create a commit with a descriptive message
git commit -m "feat: add new slide about [topic]

- Describe what you changed
- Add more details here
- Include why you made the change"

# Examples of good commit messages:
# git commit -m "feat: add Yamato Anime slide"
# git commit -m "fix: improve text readability on Slide 10"
# git commit -m "style: update color scheme for consistency"
```

### 5. Push to GitHub

```bash
# Push your branch to GitHub
git push origin feature/your-feature-name
```

### 6. Create a Pull Request (PR)

1. Go to: https://github.com/kwu-KKCC/Kelvinspeech
2. You should see a notification suggesting to create a PR
3. Click **"Compare & pull request"**
4. Fill in:
   - **Title**: Short description of changes
   - **Description**: What did you change and why?
5. Click **"Create pull request"**

### 7. Review & Merge

- Team members will review your changes
- Make updates if requested: `git add .` → `git commit --amend` → `git push origin feature/your-feature-name`
- Once approved, click **"Merge pull request"**
- Delete the branch after merging

### 8. Sync Your Local Copy

```bash
# Switch back to main
git checkout main

# Pull the latest changes from GitHub
git pull origin main
```

---

## ✏️ Making Changes

### Example: Adding a New Slide

1. **Create a branch**:
   ```bash
   git checkout -b feature/add-new-slide
   ```

2. **Edit `index.html`**:
   - Find the last `</section>` tag
   - Add your new slide HTML before the closing `</div></div>` of the slides container
   - Copy styling from similar slides for consistency

3. **Test in browser** - refresh and check your slide

4. **Commit and push**:
   ```bash
   git add index.html
   git commit -m "feat: add new slide about [topic]"
   git push origin feature/add-new-slide
   ```

5. **Create PR** and request review

### Example: Fixing Text on a Slide

1. **Create a branch**:
   ```bash
   git checkout -b fix/improve-slide-8-text
   ```

2. **Edit the text** in `index.html`

3. **Test and commit**:
   ```bash
   git add index.html
   git commit -m "fix: improve text alignment on Slide 8"
   git push origin fix/improve-slide-8-text
   ```

4. **Create PR**

---

## 🔄 CI/CD Pipeline

### How It Works

Every time you push to `main`:

1. **GitHub Actions** automatically triggers
2. **Vercel** builds and deploys the site
3. **Live site** updates at: https://speechslides-0324.vercel.app

### What This Means

- ✅ **No manual deployment** - changes go live automatically
- ✅ **No waiting** - typically live in 30-60 seconds
- ⚠️ **Test before merging** - bad code goes live immediately!

### Monitoring Deployments

1. Go to: https://github.com/kwu-KKCC/Kelvinspeech/actions
2. You'll see a workflow run for each push
3. Green ✅ = success, Red ❌ = failed

If deployment fails:
- Check the error in the Actions tab
- Fix the issue locally
- Commit and push again

---

## 📁 Project Structure

```
Kelvinspeech/
├── index.html              # Main presentation file
├── assets/                 # Images and media files
│   ├── 1898-niseko.jpg
│   ├── image-2-1.png
│   ├── image-9-1.png
│   └── page-*.png
├── .github/
│   └── workflows/
│       └── deploy.yml      # CI/CD automation (DO NOT EDIT)
├── .gitignore              # Files to ignore in git
└── README.md               # This file
```

### Key Files

- **`index.html`** - The entire presentation (slides, styling, scripts)
  - Edit this for any content changes
  - Slides are wrapped in `<section>` tags
  - CSS is in `<style>` tag at the top

- **`.github/workflows/deploy.yml`** - GitHub Actions configuration
  - ⚠️ Don't edit unless you know what you're doing
  - Controls auto-deployment to Vercel

---

## 🐛 Troubleshooting

### Problem: "Permission denied" when pushing

**Solution**: Check that you have collaborator access
```bash
# Verify remote is correct
git remote -v

# Should show:
# origin  https://github.com/kwu-KKCC/Kelvinspeech.git (fetch)
# origin  https://github.com/kwu-KKCC/Kelvinspeech.git (push)
```

### Problem: "Merge conflict" when pulling

**Solution**: Ask for help or resolve conflicts:
```bash
# See conflicts
git diff

# Abort if unsure
git merge --abort

# Then ask another developer for help
```

### Problem: Changes don't appear on live site

**Solution**: Check deployment status
1. Go to: https://github.com/kwu-KKCC/Kelvinspeech/actions
2. Look for red ❌ indicating failed deploy
3. Click on the failed workflow to see error details

### Problem: Accidentally committed to main

**Solution**: Create a proper branch next time:
```bash
# Create a new branch from main
git checkout -b fix/your-fix

# Continue work from there
```

### Problem: "index.html has uncommitted changes"

**Solution**: Commit or discard changes:
```bash
# See what changed
git diff index.html

# Commit if changes are good
git add index.html
git commit -m "your message"

# Or discard if not needed
git checkout index.html
```

---

## 📞 Getting Help

### Common Commands Quick Reference

```bash
# Update your local copy from GitHub
git pull origin main

# See your local changes
git status
git diff

# Create a branch and switch to it
git checkout -b feature/name

# Switch back to main
git checkout main

# Undo changes to a file
git checkout index.html

# Delete a local branch
git branch -d feature/name

# See commit history
git log --oneline

# Undo last commit (keep changes)
git reset --soft HEAD~1
```

### Need Help?

1. **Git questions**: Check git documentation at https://git-scm.com/doc
2. **GitHub questions**: Check GitHub Docs at https://docs.github.com
3. **Presentation issues**: Ask Kelvin or check the existing code structure

---

## 📝 Slide Reference

The presentation currently has **12 slides**:

1. Title - AID Japan × 95% AI
2. Two Companies, One Vision
3. AID Japan in Niseko
4. The 1898 Niseko
5. Hospitality Ecosystem
6. Realty & Consultancy
7. Section Break - 95% AI / Introducing Samantha
8. The Samantha Experience
9. One Ecosystem, Two Horizons
10. Yamato — AI Film Studio
11. Yamato Anime — Storytelling for Everyone
12. The Road Ahead

Each slide uses consistent styling with gold accents (`--gold: #C9A84C`).

---

## ✅ Your First Contribution Checklist

- [ ] Fork/clone the repository
- [ ] Create a branch (`git checkout -b feature/something`)
- [ ] Make changes to `index.html`
- [ ] Test locally in your browser
- [ ] Commit with clear message (`git commit -m "..."`)
- [ ] Push to GitHub (`git push origin feature/something`)
- [ ] Create a Pull Request (PR)
- [ ] Wait for review and feedback
- [ ] Make requested changes if needed
- [ ] PR gets merged and automatically deployed! 🎉

---

**Happy coding! 🚀**
