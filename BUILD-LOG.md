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

---

## 04 — Close the loop via WhatsApp

**Goal:** Make the tenant's selected time useful to Ian while keeping the existing communication channel.

**Action:** Updated `index.html` so it reads the generated URL parameters and displays only the supplied property/days/times. After the tenant chooses a slot and enters their name, the confirmation screen now has **Tell Ian on WhatsApp**.

**Behaviour:** The button opens WhatsApp with a pre-filled message containing the tenant name, property, day and selected time.

**Why:** This is the smallest next step that tests the full journey without prematurely building a backend.

**Important limitation:** There is still no shared booking database. The WhatsApp message is the handoff, not a central booking record. Double-booking is therefore still possible.

---

# CURRENT STATE

🟢 Tenant-facing page exists.  
🟢 Ian can generate a viewing link.  
🟢 Generated link controls the tenant's available slots.  
🟢 Tenant can choose a slot and hand the choice back to Ian via WhatsApp.  
🟡 Booking is not yet stored centrally.  

# NEXT

**05 — Real shared booking.**

Add only the smallest possible shared storage mechanism so a tenant's selection becomes a booking Ian can see from another device. Preserve the existing WhatsApp workflow unless real-world testing proves it should change.

# REPRODUCTION CONTRACT

When another AI takes over:

1. Read `README.md`.
2. Read this `BUILD-LOG.md`.
3. Inspect the current `index.html` and `create.html` before changing anything.
4. Preserve the working tenant journey.
5. Make one numbered step at a time.
6. Document what changed, why, technical approach and limitations.
7. Keep **Mac = 🔵 BUILD**, **iPhone = 🟢 TEST**, **Ian = 🟡 DECIDE**.
