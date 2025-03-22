# 🛠️ cp-repo-setup

This repository configures newly created repositories to meet our default GitHub standards.

## 🚀 What It Does

When you run the `Setup New Repository` GitHub Action, it:

✅ Enables:
- Auto-delete merged branches
- Private vulnerability reporting
- Secret scanning & push protection
- Dependabot for GitHub Actions + grouped updates

📜 Optionally applies `.github/rulesets/*` rulesets if it exists in the target repo.

---

## 🧑‍💻 How to Use It

### Option 1: Use the GitHub UI

1. Go to the **Actions** tab of this repo
2. Select the **Setup New Repository** workflow
3. Click **“Run workflow”**
4. Enter the repo name in the format `your-org/your-new-repo`
5. Click **Run** 🎉

---

### Option 2: Use the GitHub CLI

```bash
gh workflow run setup-new-repo.yml \
  --repo your-org/setup-repo-config \
  --field repo=your-org/your-new-repo