# Submission: User Interview Materials

**Due:** Tuesday, February 17, 2026
**Submit via:** GitHub (public repo)

---

## What to Submit

Create a folder `20260217/` inside your team folder in the public repo:

```
teams/your-team-name/20260217/
```

Include the following:

### 1. Interview Scripts / Prep Documents

Your interview guide, question list, or any prep documents you used to run the interviews. This can be a single markdown file or multiple files.

### 2. Raw Interview Notes

The raw text from each interview. These are the notes you took during or immediately after each conversation. One file per interview is ideal, but a single combined file is fine too.

**Suggested naming:**
- `interview_01.md`
- `interview_02.md`
- etc.

### 3. Interview Snapshots (Quick Summaries)

The quick post-interview summaries you wrote after each interview. These are the snapshot documents from the template we provided in class.

---

## How to Submit

Submissions are made via **pull request** on the public repo.

### Step 1: Fork the repo (first time only)

If you haven't already, fork the public repo on GitHub. Click the **Fork** button at the top right of the repo page. This creates your own copy.

### Step 2: Sync your fork

Make sure your fork is up to date with the main repo before starting:

```bash
# If you haven't added the upstream remote yet:
git remote add upstream https://github.com/kenxle/columbia-startup-studio.git

# Sync your fork
git fetch upstream
git checkout main
git merge upstream/main
```

### Step 3: Create your submission

```bash
cd teams/your-team-name
mkdir 20260217
# add your files to the folder
git add 20260217/
git commit -m "Add user interview materials"
git push origin main
```

### Step 4: Open a pull request

1. Go to the **original repo** on GitHub (not your fork)
2. Click **Pull Requests** → **New Pull Request**
3. Click **"compare across forks"**
4. Set **base** to the original repo's `main` and **head** to your fork's `main`
5. Title your PR: `[Your Team Name] User Interview Materials`
6. Submit the pull request

---

## Folder Structure Example

```
teams/your-team-name/
├── 20260206/          ← previous submission
├── 20260217/          ← this submission
│   ├── interview_script.md
│   ├── interview_01.md
│   ├── interview_02.md
│   ├── interview_03.md
│   ├── interview_04.md
│   ├── interview_05.md
│   ├── snapshot_01.md
│   ├── snapshot_02.md
│   ├── snapshot_03.md
│   ├── snapshot_04.md
│   └── snapshot_05.md
└── README.md
```

File names and organization are flexible. Just make sure all three categories are represented.
