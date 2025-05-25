# Git Guide for Team GYYKS – Tide Chart Project

This guide explains how to use Git for our CSS 360 Project 3 tide
chart website (https://github.com/zjttyl/project3-TideChart). It’s
designed for Team GYYKS to collaborate on files like `index.html`,
`README.md. Follow these steps to clone the repository, create branches, add files, commit changes, and push to GitHub.

## Prerequisites
- **Git**: Install Git (https://git-scm.com/downloads) on your computer (Windows, macOS, Linux).
- **GitHub Account**: Ensure you’re a collaborator on `zjttyl/project3-TideChart` (check with zjttyl).
- **Authentication**: Set up a Personal Access Token (PAT) or SSH key for GitHub:
  - PAT: Generate at https://github.com/settings/tokens (select `repo` scope). Save it securely.
  - SSH: Follow https://docs.github.com/en/authentication/connecting-to-github-with-ssh.
- **Terminal**: Use Command Prompt (Windows), Terminal (macOS/Linux), or VS Code’s terminal.
- **Text Editor**: Use VS Code, Notepad++, or any editor for editing files.

## 1. Clone the Repository
Clone the tide chart repository to your computer to get a local copy of the project.

1. Open a terminal and navigate to your desired folder:
   ```bash
   cd ~/Desktop/CSS360
   ```
2. Clone the repository:
   ```bash
   git clone https://github.com/zjttyl/project3-TideChart.git
   ```
   - If prompted, enter your GitHub username and PAT (not password) or use SSH (`git clone git@github.com:zjttyl/project3-TideChart.git`).
3. Navigate to the project folder:
   ```bash
   cd project3-TideChart
   ```
4. Verify files (e.g., `index.html`, `README.md`):
   ```bash
   ls
   ```

## 2. Create a Branch
Create a branch for your changes to avoid conflicts with the `main` branch.

1. Check your current branch (should be `main`):
   ```bash
   git branch
   ```
2. Create and switch to a new branch (e.g., `feature/add-ui`, `fix/api-error`):
   ```bash
   git checkout -b feature/your-feature-name
   ```
   - Example: `git checkout -b feature/add-date-picker`
3. Verify you’re on the new branch:
   ```bash
   git branch
   ```
   - The active branch is marked with an asterisk (*).

## 3. Add New Files or Edit Existing Files
Add new files (e.g., `styles.css`) or edit existing ones (e.g., `index.html`).

1. Create a new file (example: `styles.css`):
   - Use your editor (e.g., VS Code) to create `styles.css` in `project3-TideChart`.
   - Add content, e.g.:
     ```css
     body { background-color: #f0f8ff; }
     ```
2. Edit an existing file (example: `index.html`):
   - Open `index.html` in your editor and make changes (e.g., add a new button).
3. Save all changes.

## 4. Stage and Commit Changes
Stage your changes (new or edited files) and commit them with a descriptive message.

1. Check modified files:
   ```bash
   git status
   ```
   - You’ll see files under “Changes not staged” or “Untracked files.”
2. Stage files (e.g., `styles.css`, `index.html`):
   ```bash
   git add styles.css index.html
   ```
   - Or stage all changes:
     ```bash
     git add .
     ```
3. Commit changes with a message (use `[Feature]`, `[Fix]`, or `[Docs]` prefix):
   ```bash
   git commit -m "[Feature] Add styles.css and update index.html" -m "Added background color and new button. Author: YourName"
   ```
   - Example: `git commit -m "[Docs] Add git-guide.md" -m "Author: zjttyl"`

## 5. Push to GitHub
Push your branch to GitHub to share changes with the team.

1. Push your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
   - Example: `git push origin feature/add-date-picker`
   - If prompted, enter your GitHub username and PAT or use SSH.
2. Verify the branch on GitHub:
   - Visit `https://github.com/zjttyl/project3-TideChart/branches` and confirm your branch appears.

## 6. Create a Pull Request (PR)
Create a PR to merge your branch into `main` after team review.

1. Go to `https://github.com/zjttyl/project3-TideChart` and click “Pull requests” > “New pull request.”
2. Select your branch (e.g., `feature/add-date-picker`) as the source and `main` as the target.
3. Add a title (e.g., `[Feature] Add Date Picker to Tide Chart`) and description:
   ```
   - Added date picker to index.html
   - Tested locally with python3 -m http.server
   - Author: YourName
   ```
4. Assign at least one teammate as a reviewer (e.g., zjttyl).
5. Click “Create pull request.”
6. Notify the team in Discord: “Created PR #X for date picker. Please review! 🙌”

## 7. Pull Updates from Main
Keep your local repository updated with the latest `main` branch changes.

1. Switch to `main`:
   ```bash
   git checkout main
   ```
2. Pull updates:
   ```bash
   git pull origin main
   ```
3. Switch back to your branch and merge `main` if needed:
   ```bash
   git checkout feature/your-feature-name
   git merge main
   ```
   - Resolve conflicts if prompted (ask zjttyl for help).

## Common Issues and Solutions
- **Authentication Error**: If prompted for a password, use your PAT (not GitHub password). Regenerate PAT if expired (https://github.com/settings/tokens).
- **Merge Conflicts**: If `git merge main` fails, open conflicting files (e.g., `index.html`), resolve marked conflicts (e.g., `<<<<<<<`), and commit:
  ```bash
  git add index.html
  git commit -m "Resolve merge conflict"
  ```
- **Branch Not Found**: Ensure you pushed your branch (`git push origin feature/your-feature-name`).
- **Permission Denied**: Confirm you’re a collaborator on `zjttyl/project3-TideChart` (ask zjttyl to add you).

## Best Practices
- **Commit Often**: Make small, frequent commits with clear messages (e.g., `[Fix] Update API URL`).
- **Use Descriptive Branches**: Name branches like `feature/add-ui`, `fix/bug-name`, or `docs/readme`.
- **Review PRs**: Always get at least one teammate’s approval before merging.
- **Pull Before Pushing**: Run `git pull origin main` before starting work to avoid conflicts.
- **Communicate**: Post in Discord when creating branches or PRs (e.g., “Pushing feature/add-graph to GitHub. Check it out!”).

## Example Workflow
1. Clone: `git clone https://github.com/zjttyl/project3-TideChart.git`
2. Branch: `git checkout -b feature/add-styles`
3. Edit: Create `styles.css` and update `index.html`.
4. Stage: `git add styles.css index.html`
5. Commit: `git commit -m "[Feature] Add styles.css for UI" -m "Author: YourName"`
6. Push: `git push origin feature/add-styles`
7. PR: Create a PR on GitHub, assign a reviewer.
8. Merge: After approval, merge into `main` via GitHub.

## Questions?
- Contact zjttyl in Discord for Git setup or issues.
- Check Git docs (https://git-scm.com/doc) or GitHub guides (https://docs.github.com/en).

Happy coding, Team GYYKS! 🚀
