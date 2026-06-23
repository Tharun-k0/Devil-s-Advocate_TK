# Devil's Advocate

A high-stakes lawyer-themed game featuring a unique **Spin** rebuttal mechanic — spin to surface three dialogue routes, then pick the one that turns the case in your favor.

---

## Table of contents

- [Overview](#overview)
- [Tech stack](#tech-stack)
- [Getting started](#getting-started)
- [Workflow guidelines](#workflow-guidelines)
  - [Branching](#branching)
  - [Commits](#commits)
  - [Pull requests](#pull-requests)
  - [Assets](#assets)
- [Team](#team)
- [Pro-tips for team sanity](#pro-tips-for-team-sanity)

---

## Overview

**Devil's Advocate** is a 2.5D courtroom drama where dialogue isn't just chosen — it's *spun*. Every key exchange triggers the Spin mechanic: three random rebuttal routes are rolled, and the player selects one to push the case forward.

## Tech stack

| Layer | Choice |
|---|---|
| Engine | Godot `4.x` |
| Language | GDScript |
| Dialogue | [Dialogic](https://github.com/dialogic-godot/dialogic) addon |

## Getting started

This repo uses a **fork-based workflow** — nobody pushes directly to this repo except for approved PR merges. Every contributor works from their own fork.

1. **Fork the repo**
   Click `Fork` at the top of [prradyun56/Devil-s-Advocate](https://github.com/prradyun56/Devil-s-Advocate) on GitHub. This creates a copy under your own account.

2. **Clone your fork** (not this repo)
   ```bash
   git clone https://github.com/YOUR-USERNAME/Devil-s-Advocate.git
   cd Devil-s-Advocate
   ```

3. **Add this repo as `upstream`**
   ```bash
   git remote add upstream https://github.com/prradyun56/Devil-s-Advocate.git
   git remote -v
   ```
   You should see:
   ```
   origin     https://github.com/YOUR-USERNAME/Devil-s-Advocate_NAME.git   (fetch/push)
   upstream   https://github.com/prradyun56/Devil-s-Advocate.git      (fetch/push)
   ```

4. **Open in Godot**
   Launch Godot → `Import` → select `project.godot` in the root folder.

5. **Environment**
   Make sure the **Dialogic** addon is installed. It should auto-sync as long as the `addons/` folder is committed.

### Staying in sync

Before starting any new feature, pull the latest changes from upstream into your fork's `main`:

```bash
git checkout main
git fetch upstream
git merge upstream/main
git push origin main
```

> Skipping this step before branching is the #1 cause of avoidable merge conflicts. Sync first, branch second.

## Workflow guidelines

### Branching

Create a new branch for every feature. Never push directly to `main`.

```bash
git checkout -b feature/spin-mechanic
```

### Commits

Keep messages clear and conventional:

```
feat: add spin mechanic
fix: resolve dialogue box alignment
```

### Pull requests

When a feature is done, push your branch to **your fork** (`origin`), not upstream:

```bash
git push origin feature/spin-mechanic
```

Then open a PR on GitHub from your fork's branch into this repo's `main`, and **tag at least one teammate** for code review before merging.

### Assets

| Type | Location |
|---|---|
| UI assets | `res://assets/ui/` |
| Scripts | `res://scripts/` |

## Team

| Name |
|---|
| Prradyun Bhattacharjee |
| Tharun Krishna |
| Panav Gupta |
| Maulik Jain |

## Pro-tips for team sanity

- **Git LFS (Large File Storage)** — If you start adding high-quality music, video cutscenes, or large texture files, plain Git will choke. Set up Git LFS for any file over 50MB.

- **The "one-at-a-time" rule** — Godot scenes are just text files under the hood. If two people edit the same `Character.tscn` at the same time, Git will struggle to merge it.
  > **The fix:** communicate. "I'm working on the Courtroom UI scene" means nobody else touches that file until you push.

- **Commit often** — Don't wait until the end of the week. Small, broken-but-working commits beat one massive, unmergeable one.
