Here is the **translated spec to English** as requested:

## 🎯 Purpose

Allow Engineering Managers to **log, review, and follow up on 1:1 agreements simply, quickly, and persistently**, eliminating weekly friction and avoiding forgotten commitments for each report.

---

## 👥 **Common pains for EMs in 1:1s (basis for requirements)**

1️⃣ Forgetting past agreements or commitments between meetings.
2️⃣ Difficulty tracking each report's personal goals.
3️⃣ No quick visibility of each person's history.
4️⃣ Using heavy tools or scattered notes (Google Docs, Notion, paper).
5️⃣ Lack of a **private, portable, simple** space for sensitive notes.
6️⃣ No triggers to review agreements before each 1:1.

---

## ✅ **Functional Requirements**

### 1️⃣ Create 1:1 notes

* Select or enter the **report's name** (dropdown with autocomplete if desired).
* Meeting date (auto-set to “today” with the option to change).
* Free text fields for notes, with suggested structure:

  * Wins
  * Challenges
  * Topics discussed
  * Action items

### 2️⃣ View each report’s history

* See a list of all 1:1s for a report in chronological order.
* Quick access to the latest 1:1.
* Search by keyword within that report’s notes.

### 3️⃣ Track action items

* Each note can have marked action items.
* Ability to “mark as completed” and filter pending action items per report.

### 4️⃣ Export

* Button to export all notes as `.json` for manual backup.
* Ability to import `.json` for restoring data.

---

## 🚫 **Out of scope for v1**

* Automatic notifications or reminders.
* Calendar integration.
* Multi-user or real-time collaboration.

---

## ⚙️ **Non-functional Requirements**

✅ **Single-file `.html`:**

* Must work without a server, simply open in the browser.
* Must embed all CSS and JS.

✅ **Local persistence:**

* Use `localStorage` or `IndexedDB` to store notes and action items persistently in the browser.

✅ **Portable and private:**

* No third-party dependencies (no external APIs).
* Does not send data to any server.

✅ **Lightweight:**

* Fast to open, usable within seconds.
* Ideally < 100KB if possible.

✅ **Accessible on desktop and mobile:**

* Mobile-friendly for reviewing before 1:1s.

✅ **Simple UX:**

* Should be able to add a note in < 15 seconds.
* Should be able to find a past note in < 10 seconds.

---

## ✍️ **Minimal UX Ideas**

* Left panel: report list (add/select).
* Right panel: note history with dates, search, and new note entry.
* Highlight pending action items above the person’s history.
* Ability to mark action items as done with one click.

---

## 🚀 MVP Checklist to build:

* [ ] Data structure: `reports -> 1:1 sessions -> notes + action items`.
* [ ] CRUD for notes per report.
* [ ] Persistence in `localStorage`.
* [ ] Simple filtering and searching of notes.
* [ ] JSON Export/Import.
* [ ] Minimalist UI in embedded HTML/CSS.
* [ ] Cross-browser testing.
* [ ] Prepare screenshot or demo for LinkedIn post.
