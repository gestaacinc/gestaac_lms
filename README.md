## Comprehensive User‑Story Backlog (Markdown Edition)

Below are **all** user stories for every role—**Public Visitor, Learner, Trainer / Mentor, and Administrator**—consolidated into one document. Each story includes its unique ID, narrative, acceptance criteria, and priority tag (`MVP`, `Next`, `Later`).

---

### 🌐 Public‑Visitor Stories

| ID  | User Story | Acceptance Criteria | Priority |
|-----|------------|---------------------|----------|
| **P‑01** | As a visitor, I want a clean home page that explains the LMS and shows a clear “Enroll” CTA so I know what’s on offer. | • Loads ≤ 2 s on 3 G.<br>• Hero tagline, value prop, top 3 courses with “Spots remaining”.<br>• “Get Started” button links to catalog / sign‑up. | **MVP** |
| **P‑02** | As a visitor, I need a searchable course catalog with filters so I can find a program that suits me. | • Search bar (title/keyword).<br>• Filters: NC level, modality, duration.<br>• Lazy‑loaded cards; click → course detail.<br>• “Apply Now” button opens sign‑up. | **MVP** |
| **P‑03** | As a visitor, I want a rolling announcements banner so I stay aware of upcoming classes or deadlines. | • Banner auto‑scrolls 5 latest posts.<br>• Posts auto‑expire after end date.<br>• Click → announcement detail. | **MVP** |
| **P‑04** | As a visitor, I need an FAQ and chatbot so I can get answers outside office hours. | • Accordion FAQ ≤ 50 items.<br>• Chatbot answers ≤ 4 s; escalates if confidence < 70 %. | **MVP** |
| **P‑05** | As a visitor, I want a live events calendar so I can plan my availability. | • Month view; color‑coded events.<br>• “Add to my calendar” (ICS). | **Next** |
| **P‑06** | As a visitor, I want a Student Success Wall so I feel inspired to join. | • Carousel of avatars + badge.<br>• Pulls 20 latest achievements. | **Next** |
| **P‑07** | As a visitor, I’d like an AI course recommender so I’m not overwhelmed by choices. | • 3‑question wizard.<br>• Returns top 3 courses + rationale.<br>• Tracks click‑through. | **Next** |
| **P‑08** | As a visitor, I should be able to switch site language between English and Filipino so I understand content easily. | • Header toggle.<br>• Static pages translated; dynamic content via API.<br>• Cookie remembers choice. | **Later** |
| **P‑09** | As a visitor on mobile, I want the public site to work as a PWA so I can browse offline. | • Install prompt.<br>• Offline cache shell + last pages.<br>• “You are offline” banner. | **Later** |

---

### 🎓 Learner Stories

| ID  | User Story | Acceptance Criteria | Priority |
|-----|------------|---------------------|----------|
| **L‑01** | As a learner, I want a personal dashboard showing progress, badges, and next deadlines so I know where I stand. | • Loads ≤ 2 s.<br>• Progress rings per unit.<br>• Next‑deadline banner links to Kanban.<br>• Badge shelf shows 3 latest. | **MVP** |
| **L‑02** | As a learner, I need a Kanban board per competency unit so I can self‑manage tasks. | • Columns: Backlog, In Progress, Peer Review, Mentor Sign‑Off, Done.<br>• Drag‑drop persists via WebSocket.<br>• Card click opens drawer. | **MVP** |
| **L‑03** | As a learner, I want to upload evidence to a task so mentors can verify my work. | • Accept mp4 ≤ 200 MB, jpg/png ≤ 10 MB, ZIP ≤ 50 MB, repo URL.<br>• Thumbnail preview.<br>• Presigned S3 upload; retry on fail. | **MVP** |
| **L‑04** | As a learner, I want an AI Study Buddy for contextual Q&A so I can unblock myself quickly. | • Chat panel on task drawer.<br>• Response ≤ 5 s, cites TESDA section.<br>• Moderation filter active. | **Next** |
| **L‑05** | As a learner, I want adaptive hints after two failed submissions so I can learn from mistakes. | • Detect two mentor rejections.<br>• < 80‑word hint logged in history. | **Next** |
| **L‑06** | As a learner, I want badges and printable certificates so I feel rewarded. | • Badge engine auto‑awards.<br>• Certificate PDF with QR.<br>• Wallet page lists all. | **MVP** |
| **L‑07** | As a learner, I need an offline mode (PWA) so I can keep working with poor internet. | • “Download pack” caches lectures/tasks.<br>• Evidence queues offline.<br>• Offline status banner. | **Later** |
| **L‑08** | As a learner, I want a portfolio export so I can showcase my work to employers. | • One‑click ZIP or public URL.<br>• Includes badges, evidence, comments.<br>• Revocable link. | **Next** |

---

### 🧑‍🏫 Trainer / Mentor Stories

| ID  | User Story | Acceptance Criteria | Priority |
|-----|------------|---------------------|----------|
| **T‑01** | As a trainer, I need a class dashboard with progress and risk flags so I can intervene early. | • Table of learners with % done, last login, risk score.<br>• Burndown graph.<br>• Click learner → filtered Kanban. | **MVP** |
| **T‑02** | As a trainer, I want to create or import task templates aligned to TESDA so content stays consistent. | • “New unit” wizard maps TESDA code.<br>• Drag‑drop card builder.<br>• Clone library. | **MVP** |
| **T‑03** | As a trainer, I want an AI task generator that drafts cards from a learning outcome so I save prep time. | • Input LO → 4–6 tasks (title, DoD, evidence, hours).<br>• Editable before publish.<br>• Saved to library. | **Next** |
| **T‑04** | As a trainer, I need evidence quick‑view with AI error spotting so assessment is efficient. | • Inline preview.<br>• AI highlights ≥ 0.8 confidence.<br>• Accept/reject hints. | **Next** |
| **T‑05** | As a trainer, I want rubric‑based grading with voice notes for rich feedback. | • 0–4 scale rubric.<br>• Voice ≤ 90 s, auto‑transcribed.<br>• Learner notified instantly. | **MVP** |
| **T‑06** | As a trainer, I want automatic peer‑review pairing so every submission gets feedback without manual effort. | • Auto‑assign within cohort.<br>• Reminder after 24 h.<br>• Mentor override. | **MVP** |
| **T‑07** | As a trainer, I need sentiment analytics from chat so I can detect confusion trends. | • Tag cloud of negatives.<br>• Alert when confusion > 0.6.<br>• Link to threads. | **Later** |
| **T‑08** | As a trainer, I want to launch live showcase events and auto‑issue badges to winners so learners stay motivated. | • Schedule event; join link.<br>• Audience vote; top 3 get badge.<br>• Results posted. | **Later** |

---

### 🛠️ Administrator Stories

| ID  | User Story | Acceptance Criteria | Priority |
|-----|------------|---------------------|----------|
| **A‑01** | As an admin, I need a KPI cockpit with enrollment, completion, and dropout metrics to track goals. | • Dashboard cards + graphs.<br>• Course/date filters.<br>• CSV export. | **MVP** |
| **A‑02** | As an admin, I want bulk user import and role management so onboarding is quick. | • CSV/XLSX upload preview.<br>• Role dropdown.<br>• Deactivate retains data. | **MVP** |
| **A‑03** | As an admin, I need a course & competency manager to create, clone, or archive programs. | • CRUD UI with TESDA mapping.<br>• Archive hides course; keeps data.<br>• Clone copies templates/badges. | **MVP** |
| **A‑04** | As an admin, I want a content approval workflow so only vetted material goes live. | • States: Draft → Review → Published.<br>• Reviewer notifications.<br>• Version diff & rollback. | **Next** |
| **A‑05** | As an admin, I need dropout‑risk prediction and nudge tools to improve retention. | • ML scores daily.<br>• Bulk SMS/email nudges.<br>• Track open/click rates. | **Next** |
| **A‑06** | As an admin, I need full audit logs for compliance audits. | • Immutable entries (timestamp, user, action).<br>• Search/filter.<br>• Export JSON/CSV. | **MVP** |
| **A‑07** | As an admin, I want natural‑language BI queries so non‑technical staff can explore data. | • Text box → chart/table ≤ 10 s.<br>• Supports counts/averages/group‑by.<br>• Respects permissions. | **Later** |
| **A‑08** | As an admin, I need an accessibility audit bot that flags new content issues so the platform stays inclusive. | • Nightly scan.<br>• Severity report.<br>• “Fix now” link to editor. | **Later** |

---

### Priority Legend

* **MVP** — Must be delivered for first public release.  
* **Next** — Planned for Sprints 2–3 after launch.  
* **Later** — Nice‑to‑have; schedule post‑launch.

---

These tables form the master backlog you can paste into Jira, Trello, ClickUp, or any planning tool that supports Markdown.
