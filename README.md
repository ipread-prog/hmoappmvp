# 🏠 HMO Viewing MVP

# 🧠 WHERE WE ARE

**Project:** HMO Viewing Link  
**Current step:** **04 — Close the loop**

## 🎯 WHY ARE WE HERE?

A potential tenant wants to view an HMO room. The aim is to replace the back-and-forth with:

**Message → Link → Choose time → Tell Ian**

We are deliberately building the smallest useful thing first.

## 🗺️ ROADMAP

1. **Foundation** ✅ GitHub + project memory
2. **Tenant screen** ✅ Choose a viewing time
3. **Create link** ✅ Ian selects times + copies link
4. **Close the loop** 🔵 **NOW** — tenant choice is turned into a ready-made WhatsApp message
5. **Real shared booking** ⏭️ Store bookings centrally
6. **Collision protection** ⏭️ Prevent double booking
7. **Confirmation** ⏭️ Proper confirmation for both sides
8. **Real-world test** ⏭️ Use with actual applicants
9. **Only then** decide what else is worth building

## 🔵 MAC / BUILD

The MacBook is where the project is built and changed.

## 🟢 iPHONE / TEST

The iPhone is where the experience is tested as a real tenant/user.

## 🟡 YOU / DECIDE

Ian judges what feels useful, awkward or unnecessary. Technical implementation stays with the AI unless Ian explicitly wants to do it.

## 🟢 WHAT WE DID THIS STEP

- Made the tenant page read the viewing details and times from the generated link.
- Added a final **Tell Ian on WhatsApp** button.
- The button creates a ready-made WhatsApp message containing the tenant name, property, day and selected time.
- Kept the existing WhatsApp conversation as the communication channel.

## ⚠️ IMPORTANT LIMITATION

This is **not yet a true shared booking database**. The WhatsApp handoff proves the end-to-end user journey without adding a backend. A central booking system is Step 05.

## 🧪 TEST

1. On Mac: open `create.html` and generate a link.
2. Send/copy that link to the iPhone.
3. On iPhone: choose a time and enter a name.
4. Tap **Tell Ian on WhatsApp**.
5. Check the WhatsApp message before sending it.

## 🧠 RULE

> **Reality before architecture.**

Build → experience → learn → then add infrastructure only when the real problem is proven.

## 🤖 AI-AGNOSTIC

The repository is the source of truth. Any AI should read this README before working. Important changes should be documented here or in the build log so the project can move between ChatGPT, Claude, Grok or another tool.
