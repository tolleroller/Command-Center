# Command Center — Vision, Status & Handoff Notes

**Last updated:** 2026-08-22  
**Purpose of this file:** Living handoff document. When starting a new Grok thread about Command Center, say “check the repository” or “read VISION-ROADMAP.md” so Grok is quickly on the same page as previous conversations.

---

## Core Direction

Move toward a more **agentic, conversation-driven** dashboard.

**Desired end-state feel:**  
Interact primarily through chat with Grok. The Command Center app is the persistent visual / organized layer. Chat is the input surface; the app is the living dashboard.

---

## Current Architecture (as of 2026-08-22)

- **Live site:** https://tolleroller.github.io  
- **Repo:** public `tolleroller/Command-Center`  
- **Stack:** Single `index.html` + `vision-board.jpeg` + one state file. Tailwind CDN + vanilla JS. Data in browser `localStorage`. No backend.

### Single source of truth

**`command-center-latest.json`** is the only data file that matters.

It is a full backup of everything the app can change:
- Today’s Focus / todos
- Lab ideas + next steps
- Projects + notes
- Goals notes
- Health notes
- Finance + News + Entertainment content
- Theme

### How Sync works (important)

**Sync from repo is one-way only (App ← GitHub).**

- You tap ⋯ → **Sync from repo**
- App downloads `command-center-latest.json` and restores the complete state
- It does **not** upload anything back to GitHub

| Who made the change | What to do |
|---------------------|------------|
| Grok (content, Lab ideas, etc.) | Just tap **Sync from repo** |
| You (in the app: todos, Lab bullets, project notes, etc.) | **Export full backup**, then upload that file as the new `command-center-latest.json` if you want those changes saved on GitHub |

### Protected localStorage keys
`theme`, `jp_command_todos`, `jp_goal_bullets_v1`, `jp_health_bullets_v1`, `jp_command_projects_v3`, `jp_lab_ideas_v3`, `jp_content_update_v1`

---

## Preferred Working Workflow

1. Discuss / draft changes in chat.  
2. Grok proposes the concrete change.  
3. User reviews.  
4. User says “commit it” / “push it”.  
5. Grok writes to the repo (usually updates `command-center-latest.json` or `index.html`).  
6. User taps **Sync from repo** on the phone.

Keep the user in the review loop. Do not write to the repo without clear go-ahead.

**Safety:** Backup branches are created before risky `index.html` changes.

---

## Active Lab / Venture Ideas

**POD Merch / Statement Brand (skizofrenick sage)**  
Low-capital, high-automation print-on-demand brand. Clever, slightly unhinged mantras on T-shirts, stickers, posters. Printify → Shopify. Zero inventory.  
Status: in Lab tab. First designs + sample order still pending.

Other themes (community events, Salient Advisory / AI consulting, app ideas, etc.) remain available.

---

## Practical Next Steps

1. Use the single Sync model as the normal update path.  
2. When user makes personal changes in the app that should persist, Export full backup → replace `command-center-latest.json`.  
3. Weekly content refresh (News / Entertainment / Finance) still happens by updating the content section inside `command-center-latest.json`.  
4. Longer term: explore true two-way sync or a small backend if the manual export step becomes annoying.

---

## Notes for Future Grok Threads

- User is a civil engineer (PE). Treat GitHub commits like issuing a drawing set.  
- User often uses speech-to-text — clarify when wording is unclear.  
- Visual, masculine / non-cute aesthetic.  
- Primary use is the **home-screen PWA** on iPhone (not Safari tab).  
- Goal: dashboard that stays alive so life stays in flow.

This file should be kept current whenever major direction or next-step decisions are made.
