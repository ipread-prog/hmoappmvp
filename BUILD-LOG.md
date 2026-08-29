# 🧭 BUILD LOG — HMO Viewing MVP

This file records the build so another AI can reproduce the work and Ian can see exactly how we got here.

## 01 — Repository created

**Goal:** Create a neutral home for the project so the work is not trapped inside one AI.

**Action:** Created GitHub repository `ipread-prog/hmoappmvp` and enabled it as the project source of truth.

**Why:** ChatGPT, Claude, Grok or another AI can all inspect the same files and history.

---

## 02 — Smallest tenant-facing prototype

**Goal:** Prove the tenant journey before adding infrastructure.

**Action:** Built `index.html` as a single-file webpage.

**Behaviour:** Tenant sees viewing times → taps a time → enters name → receives a confirmation screen.

**Deliberately excluded:** AI, database, accounts, calendar integrations, WhatsApp/Messenger integrations and payments.

**Why:** We are testing the core behaviour, not building a platform.

---

## 03 — Zero-friction link creation

**Goal:** Make the MVP useful to Ian, not just clickable for a tenant.

**Action:** Added `create.html`.

**Behaviour:** Ian enters the viewing location, enters two day labels, taps available times, generates a unique URL, then taps **Copy link**.

**Action-link design:** The generated URL carries the viewing details and selected times into the tenant page. No database is used yet.

**Why:** This creates the actual workflow we wanted: **pick slots → copy link → paste into WhatsApp/Messenger/email/SpareRoom**.

**Limitation:** This is still a prototype. Bookings are not yet stored centrally, so two people could theoretically choose the same slot. We will solve that only after the workflow proves useful.

---

## CURRENT STATE

🟢 Tenant-facing page exists.  
🟢 Ian can generate a viewing link.  
🟢 Link can be copied and shared.  
🟡 Booking is simulated locally; no shared booking database yet.  

## NEXT

**Test the complete workflow on iPhone:**

1. Open `create.html`.
2. Create a set of viewing slots.
3. Copy the generated link.
4. Open the link as if you were the tenant.
5. Choose a slot and confirm.
6. Decide what feels wrong or missing.

**Rule:** Do not add features just because they seem useful. Add the next thing because the real workflow proves we need it.
