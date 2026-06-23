DEVIL'S ADVOCATE
🎮 Overview
A high-stakes lawyer-themed game featuring a unique "Spin" rebuttal mechanic.

🛠 Tech Stack
Engine: Godot [Insert Version, e.g., 4.x]

Language: GDScript

🚀 Getting Started
Clone the repo: git clone [your-repo-url]

Open in Godot: Launch Godot, click Import, and select the project.godot file in the root folder.

Environment: Ensure you have the Dialogic addon installed (it should auto-sync if you commit the addons/ folder).

📋 Workflow Guidelines
Branching: Create a new branch for every feature (e.g., git checkout -b feature/spin-mechanic). Never push directly to main.

Commits: Write clear, concise messages: feat: add spin mechanic, fix: resolve dialogue box alignment.

Pull Requests: When finished, open a PR on GitHub. Tag at least one teammate for a code review before merging.

Assets: Place all new UI assets in res://assets/ui/ and scripts in res://scripts/.


👥 Team
Prradyun Bhattacharjee

Tharun Krishna

Panav Gupta

Maulik Jain


Pro-Tips for Team Sanity
Git LFS (Large File Storage): If you start adding high-quality music, video cutscenes, or massive texture files, Git will choke. If you exceed 50MB per file, set up Git LFS for your repo.

The "One-at-a-time" Rule: Godot scenes are just text files (YAML-like). If two people edit the same Character.tscn at the same time, Git will freak out trying to merge them.

The Fix: Communicate! "I'm working on the Courtroom UI scene" means nobody else touches that specific file until you push.

Commit Often: Don't wait until the end of the week. Committing small, broken-but-working chunks is better than one massive, unmergeable commit.