# Submission: Landing Page + Synthetic Testing

**Due:** Tuesday, February 24, 2026
**Submit via:** GitHub (public repo)

---

## What to Submit

Create a folder `20260224/` inside your team folder in the public repo:

```
teams/your-team-name/20260224/
```

Include the following:

### 1. Polished Brand Position

Your final brand position document, updated from the draft you started in class on Feb 19. Use the template: [template_brand-position.md](../resources/template_brand-position.md)

This should reflect any revisions from synthetic testing feedback.

### 2. V1 Landing Page Copy

The written copy for your landing page, organized by section. Common sections include:

- **Hero** — pain point headline + your reframe
- **How It Works** — what your product is, concretely
- **Social Proof** — why someone should believe you
- **Objection Handling** — why people say no, and your answer
- **CTA** — what you're asking them to do

Your page doesn't need all of these, and it may have sections not listed here. Structure it around what makes sense for your product.

### 3. Synthetic Testing Results

Evidence of at least **2 rounds** of synthetic user testing iteration (V1 → V2 minimum, V3 if possible). Include:

- The copy versions you tested (V1, V2, etc.)
- Feedback summaries from each round
- What you changed between rounds and why

Use the synthetic testing skill from class: `exercise/synthetic-user-testing/SKILL.md`

### 4. Deployed Landing Page URL

A real URL, live on the internet, using your best copy version from synthetic testing.

**Platforms:** Carrd, Framer, Webflow, raw HTML — whatever works.

**Must include at minimum:** headline, value prop, and a CTA (sign-up, waitlist, quiz, etc.)

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
mkdir 20260224
# add your files to the folder
git add 20260224/
git commit -m "Add landing page and synthetic testing results"
git push origin main
```

### Step 4: Open a pull request

1. Go to the **original repo** on GitHub (not your fork)
2. Click **Pull Requests** → **New Pull Request**
3. Click **"compare across forks"**
4. Set **base** to the original repo's `main` and **head** to your fork's `main`
5. Title your PR: `[Your Team Name] Landing Page + Synthetic Testing`
6. Submit the pull request

---

## Folder Structure Example

```
teams/your-team-name/
├── 20260206/          ← divergent thinking
├── 20260217/          ← interview materials
├── 20260219/          ← synthesis, brief, brand position
├── 20260224/          ← this submission
│   ├── brand_position.md
│   ├── landing_page_copy.md
│   ├── synthetic_testing/
│   │   ├── v1_copy.md
│   │   ├── v1_results.md
│   │   ├── v2_copy.md
│   │   └── v2_results.md
│   └── README.md          (include your live URL here)
└── README.md
```

File names and organization are flexible. Just make sure all four deliverables are represented.
