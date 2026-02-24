# Submission: Product Brief, Brand Position & Synthetic User Testing

**Due:** Tuesday, February 24, 2026
**Submit via:** GitHub (public repo)

---

## What to Submit

Create a folder `20260219/` inside your team folder in the public repo:

```
teams/your-team-name/20260219/
```

Include the following:

### 1. Product Brief

One-page document covering what you're building, who it's for, and what problem it solves. Use the template: [template_product-brief.md](template_product-brief.md)

**Use AI to help draft this.** Feed your synthesis and interview notes into an LLM and ask it to help you fill out the template. Edit and refine the output — don't just submit raw AI output, but don't do this by hand either.

### 2. Brand Position

Internal document capturing your brand's thesis, identity, and canonical language. Use the template: [template_brand-position.md](template_brand-position.md)

**Use AI to help draft this.** Same approach: feed your synthesis into an LLM, use the template as a structure, and refine what it gives you. The brand position builds directly on your synthesis and product brief.

### 3. Synthetic User Testing (In-Class Exercise)

Run at least **5 rounds** of synthetic user testing on your landing page copy. Include:

- The copy versions you tested (V1 through V5+)
This will be included teams/4CUz/20260219/synthetic-user-testing/docs/user_testing/synthetic_testing
- Feedback summaries from each round
Command-output highlights:

Round 1:
Skeleton command output: 60 profiles, 12 per bucket
Baseline stats: resonance 23%, intent 13%, conversion 12%, dealbreakers 33%
V6 stats: resonance 77%, intent 55%, conversion 52%, dealbreakers 5%
Stats files: stats_baseline.txt, stats_v6.txt

Round 2:
Baseline: resonance 13%, intent 12%, conversion 10%, dealbreakers 42%
V6: resonance 70%, intent 72%, conversion 62%, dealbreakers 5%
Stats files: stats_baseline.txt, stats_v6.txt
Run 3: High-Need Only

Round 3:
Folder: 20260224.04_noticeme-landing-copy-r3-high-need
Final report: report_v6.html
V6 stats: resonance 68%, intent 73%, conversion 57%, dealbreakers 3%
Stats file: stats_v6.txt
Run 4: 20 Profiles

Round 4:
Folder: 20260224.05_noticeme-landing-copy-r4-20-profiles
Final report: report_v6.html
Constraint check: 20 profiles confirmed in audience.json
V6 stats: resonance 85%, intent 75%, conversion 55%, dealbreakers 5%
Stats file: stats_v6.txt
Run 5: Students Only (No Young Professionals)

Round 5:
Folder: 20260224.06_noticeme-landing-copy-r5-students-only
Final report: report_v6.html
Constraint check: occupations are only Student, Graduate student, Teaching assistant, Research assistant, Campus club lead in audience.json
V6 stats: resonance 70%, intent 58%, conversion 50%, dealbreakers 15%
Stats file: stats_v6.txt

- What you changed between rounds and why
The first 2 ones, I just tell them to repeat itself with new data so that I can see the validity. Now for the third one, only focus on people who really need to get off social media. The fourth one, only generate 20 profiles. The fifth one, only focus on students, and no young professionals. So that I can see more of the diversity and how well they look in the analysis. Looks like a good idea to me.

Use the synthetic testing skill from class: [synthetic-user-testing/SKILL.md](../../classes/20260219_c9w5_thu_synthetic-testing/exercise/synthetic-user-testing/SKILL.md)

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
git commit -m "Add product brief, brand position, and synthetic testing"
git push origin main
```

### Step 4: Open a pull request

1. Go to the **original repo** on GitHub (not your fork)
2. Click **Pull Requests** → **New Pull Request**
3. Click **"compare across forks"**
4. Set **base** to the original repo's `main` and **head** to your fork's `main`
5. Title your PR: `[Your Team Name] Product Brief, Brand Position & Synthetic Testing`
6. Submit the pull request

---

## Folder Structure Example

FOR FULL INSIGHTS synthetic_testing, please go into each run folder inside to check.
```
teams/your-team-name/
├── 20260206/          ← divergent thinking
├── 20260217/          ← interview materials + synthesis
├── 20260219/          ← this submission
│   ├── product_brief.md
│   ├── brand_position.md
│   └── synthetic_testing/
│       ├── v1_copy.md
│       ├── v1_results.md
│       ├── v2_copy.md
│       ├── v2_results.md
│       ├── ...
│       ├── v5_copy.md
│       └── v5_results.md
└── README.md
```

File names are flexible. Just make sure all three deliverables are included.
