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

1. **Clone the repo**
   ```bash
   git clone https://github.com/prradyun56/Devil-s-Advocate.git
   ```
2. **Open in Godot**
   Launch Godot → `Import` → select `project.godot` in the root folder.
3. **Environment**
   Make sure the **Dialogic** addon is installed. It should auto-sync as long as the `addons/` folder is committed.

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

When a feature is done, open a PR on GitHub and **tag at least one teammate** for code review before merging.

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
