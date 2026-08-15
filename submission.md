# Project Submission Report

## 1. Student Details

- **Full Name:** Gloria Khalayi Maloba
- **GitHub Username:** GloriaKMaloba
- **Email:** gloria.maloba@strathmore.edu

---

## 2. Deployed Project Link

- **Live GitHub Pages URL:** https://is-project-2026.github.io/portfolio-168878/

---

## 3. Reflection — Grounded in Your Git History

> **Rules:** Every answer below **must include a direct link** to the specific commit, PR, issue, or branch in your repository that demonstrates what you are describing. Answers without working links will not be graded. Generic explanations that could apply to any project will receive zero marks.
>
> **Marks:** A (2 marks) · B (1 mark) · C (1 mark) · D (1 mark) = **5 marks total**

### A. Your Best Commit

Paste the URL of the commit in your history that you think best demonstrates clean conventional commit practice (good type tag, clear subject, meaningful body or footer).

- **Commit URL:** (https://github.com/IS-PROJECT-2026/portfolio-168878/commit/daf8102247675570264c11d116ca23ad515962a2)
- **Why this one?** It uses a clear feat type tag with a concise subject, and a body explaining what was added and why, and a footer that closes out my first issue (#1). This follows the  conventional commits format, making it my best."

### B. A Mistake or Struggle

Link to a commit, PR, or issue where something went wrong — a bad commit message you had to fix, a branch you had to delete and recreate, a PR that needed rework, or a deployment that broke. 

- **Link to the evidence:** (https://github.com/IS-PROJECT-2026/portfolio-168878/commit/a033bf8e9d4c26998f78bef9a43cc5c4c2ebb256)
- **What happened and how did you recover?** While resolving the merge conflict between style/18-header-padding and fix/19-header-color, I resolved it locally and pushed the merge commit directly to main instead of going through the fix/19-header-color pull request. I recovered by treating it as a lesson whereby for the remaining conflicts, I made sure resolution happened inside the pull request itself, keeping main protected as intended.

### C. A Pull Request You're Proud Of

Paste the URL of the PR that best shows your self-review process — one where the description is clear, the issue linkage is correct, and the diff tells a coherent story.

- **PR URL:** (https://github.com/IS-PROJECT-2026/portfolio-168878/pull/30)
- **What did you check before merging?** I reviewed the diff to confirm the README accurately reflected the live deployment link and project details, and verified the PR was correctly linked to close issue #29 before merging into main.

### D. One Thing You Would Do Differently

If you had to restart this project from scratch with everything you know now, name one specific workflow decision you would change (not a code change — a Git/project management decision).

- **What would you change?** I would add every new issue to the Kanban board immediately upon creation, not just the ones planned from the start. Some of the issues after the 3 milestones were completed were created mid-project and never added to the board, so they had to be manually dropped straight into 'Done' instead of moving through the board like the rest of the work. An example is issue 19 (the URL pasted below).
- **Link to the evidence of the original decision:** (https://github.com/IS-PROJECT-2026/portfolio-168878/issues/19)

---

## 4. Screenshots of Key GitHub Features

Demonstrate your workflow mechanics by embedding your screenshots below.

> **CRITICAL FOR WORKING IMAGES:** Do not type manual folder paths. Edit this file directly on the GitHub web interface, click on the blank line below each prompt, and **paste (Ctrl+V / Cmd+V)** your screenshot. GitHub will automatically upload the file and generate a permanent, working image link for you.

### A. Milestones and Issues
*Provide a screenshot showing your active milestone(s) and the granular tracking issues linked directly to them.*

[Milestones screenshot](milestones.png)

* **Caption:** Three milestones: Portfolio structure, Portfolio core xontent, and styling the portfolio. Each contains granular issues tracked to completion.

### B. Project Board
*Provide a screenshot of your GitHub Project Board with your issues organized dynamically across columns (To Do, In Progress, Done).*

![Kanban](board.png)

* **Caption:** Kanban board showing issues progressing through To Do, In Progress, and Done as work was completed. The last issue is still in the 'In Progress' column because I'm currently working on it as I fill in this document. It will move in the 'Done' column once I commit and push it.

### C. Branching Architecture
*Provide a screenshot showing your local or remote Git branch list, highlighting your use of conventional, issue-linked naming patterns (e.g., `feat/`, `fix/`, `style/`).*

![branches screenshot](branches.png)

* **Caption:** Branch list showing conventional, issue-linked naming (feat/, fix/, style/, docs/) tied to specific issue numbers.

### D. Pull Requests & Traceability
*Provide a screenshot of a completed or open Pull Request (PR) on GitHub that clearly shows it is linked to a related development issue.*

![PR example](PR.png)

* **Caption:** PR #30 shows direct issue linkage via 'Closes #29' in the description, and the sidebar confirms the merge automatically updated the linked project board card to Done.

---

## 5. Merge Conflict Evidence

You must engineer **three merge conflicts**, each triggered by a **different cause** from those covered in the lecture. For Conflict 1, document the full resolution lifecycle. For Conflicts 2 and 3, provide the conflict marker screenshot and identify the cause.

> **Marks:** Conflict 1 full chronology (2 marks) · Conflict 2 (1 mark) · Conflict 3 (1 mark) · All three use distinct causes (1 mark) = **5 marks total**

---

### Conflict 1 — Full Chronology

**What cause did you use?** Same-line edit

#### Step 1: Generating the Clash
*Screenshot showing the merge attempt and the conflict warning.*

![same-line edit conflict warning](conflict1.png) 

* **Caption:** Attempted merge between style/18-header-padding and fix/19-header-color produced a conflict warning on style.css, since both branches modified the same lines in the header selector.

#### Step 2: Inside the Code Editor (Conflict Markers)
*Screenshot showing the raw, unresolved conflict markers (`<<<<<<< HEAD`, `=======`, `>>>>>>>`) in your editor.*

![conflict makrers](/evidence/conflict_evidence_1.png)

* **Caption:** The dispute was over the header's padding and background-color values: one branch increased padding, the other darkened the background. I resolved it by keeping the updated padding from one branch and the darker background from the other, merging both intended changes rather than picking just one side.

#### Step 3: Resolution & Clean Merge
*Screenshot of your clean Git history or completed PR showing the conflict was resolved and merged.*

![rseolution 1](resolution1.png)

* **Caption:** Final resolution merged cleanly into main, combining both changes.

---

### Conflict 2 — Different Cause

**What cause did you use?** Delete/modify conflict

**Why does this cause trigger a conflict?** One branch deleted or restructured a section while the other branch modified content inside that same section. Git can't reconcile a deletion against an edit to the same lines.

![alt text](/evidence/conflict_evidence_2.png)

* **Caption:** refactor/21-consolidate-experience restructured the experience section while fix/22-campaign-coordinator-wording edited wording inside the Campaign Coordinator card, causing a delete/modify conflict on index.html.

---

### Conflict 3 — Different Cause

**What cause did you use?** Add/add conflict

**Why does this cause trigger a conflict?** Both branches added a new skill list item at the same position in the skills section, causing an add/add conflict.

![conflict 3](/evidence/conflict_evidence_3.png)

* **Caption:** Both feat/25-add-skill-publicspeaking and feat/26-add-skill-eventplanning added a new skill list item at the same position in the skills section in index.html, causing an add/add conflict. I resolved this by accepting the incoming change (Public Speaking) over my branch's own addition (Event Planning), so the final merged file shows no visible difference from main. This is expected as it reflects how add/add conflicts resolve when one side's addition is chosen over the other.

---
##
## 6. Feedback & Evaluation

To help improve this course for future engineering cohorts, please take 2 minutes to fill out the anonymous feedback form. Your honest review helps shape how this program is taught next semester!
- [ ] **Anonymous Evaluation Form:** [Course & Instructor Evaluation](https://forms.gle/YLybnsyXXErKEg3s9)

---
 
## Final Submission
 
Once your repository is complete, submit your work through the official submission form below. The form will **stop accepting responses after Monday, August 17th, 2026** — no late submissions will be accepted.
 
> **Submission Form:** [https://forms.gle/KrT4VxtFtkU3wtYu8](https://forms.gle/KrT4VxtFtkU3wtYu8)