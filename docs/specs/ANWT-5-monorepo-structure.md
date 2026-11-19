# ANWT-5: Set up the monorepo structure

**Status:** Approved | **Epic:** ANWT-1 Foundation | **Story points:** 2 | **Owner:** Dev 1 | **Approved by:** Sagar, 20 November 2026

### 1. Goal

Give the project one clear layout so every agent and reader knows where things live and how to run them.

### 2. Scope

**In scope:** the top-level folders, a README that explains the layout and how to run the project, and a records file listing which agent owns which folder when needed. **Out of scope:** any application code, Docker files, CI workflows.

### 3. Behaviour

- Given a fresh clone, when I open the README, then I can see what each folder holds and how to run the project.
- Given the repo, when a pull request is opened, then branch protection requires a review before merging.

### 4. Interfaces

Folders: frontend/, backend/, docs/ and infra/ at the repo root. docs/ contains ai-team/ and specs/. No code interfaces.

### 5. Data

None.

### 6. Edge cases

Empty folders are kept with .gitkeep files until they have real content, then the placeholder is removed. The README must not promise commands that do not work yet; unbuilt parts are marked "coming soon".

### 7. Security and logging

No secrets in the repo. The .gitignore covers .env files, node\_modules, dist and Python caches.

### 8. Test plan

Manual check against both scenarios by the QA agent. A CI check (added in ANWT-10) fails if any of the four top-level folders is missing.

### 9. Open questions

Note: the repo already has the four folders and branch protection from setup, so this story mostly verifies and documents what exists. Confirm with the human before closing.

### 10. Change log

Draft created.
