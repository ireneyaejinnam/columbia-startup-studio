# Submission: Interview Synthesis, Product Brief & Brand Position

**Due:** Thursday, February 19, 2026
**Submit via:** GitHub (public repo)

---

## What to Submit

Create a folder `20260219/` inside your team folder in the public repo:

```
teams/your-team-name/20260219/
```

Include the following:

### 1. Interview Synthesis Comparison Exercise

**Part A: Human Synthesis**

Your team's synthesis of the interviews for your chosen idea. Include:
- Key patterns across interviews
- Top 5 quotes (exact words from interviewees)
- Contradictions and what they might mean
- Surprises — what changed your thinking
- Your overall read on the data

**Part B: AI Synthesis**

Feed your interview snapshots **and** raw interview notes into an LLM (Claude, ChatGPT, or any model). Ask it to synthesize the data. Include the AI's full output.

**Part C: Comparison Reflection** (1-2 paragraphs)
- What did the AI find that you missed?
- What did you notice that the AI didn't?
- Where do you trust the AI's read? Where don't you?

**Important:** Part A is the **only part of this assignment you should do without AI.** Do your own synthesis first, written down, before opening any LLM. The whole point is to develop your own read on the data before seeing what the AI thinks.

### 2. Product Brief

One-page document covering what you're building, who it's for, and what problem it solves. Use the template: [template_product-brief.md](template_product-brief.md)

**Use AI to help draft this.** Feed your synthesis and interview notes into an LLM and ask it to help you fill out the template. Edit and refine the output — don't just submit raw AI output, but don't do this by hand either.

### 3. Brand Position

Internal document capturing your brand's thesis, identity, and canonical language. Use the template: [template_brand-position.md](template_brand-position.md)

**Use AI to help draft this.** Same approach: feed your synthesis into an LLM, use the template as a structure, and refine what it gives you. The brand position builds directly on your synthesis and product brief.

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
mkdir 20260219
# add your files to the folder
git add 20260219/
git commit -m "Add synthesis, product brief, and brand position"
git push origin main
```

### Step 4: Open a pull request

1. Go to the **original repo** on GitHub (not your fork)
2. Click **Pull Requests** → **New Pull Request**
3. Click **"compare across forks"**
4. Set **base** to the original repo's `main` and **head** to your fork's `main`
5. Title your PR: `[Your Team Name] Synthesis, Product Brief & Brand Position`
6. Submit the pull request

---

## Folder Structure Example

```
teams/your-team-name/
├── 20260206/          ← previous submission
├── 20260217/          ← interview materials
├── 20260219/          ← this submission
│   ├── synthesis.md          (Parts A, B, and C)
│   ├── product_brief.md
│   └── brand_position.md
└── README.md
```

File names are flexible. Just make sure all three documents are included.
