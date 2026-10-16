# PRD Outline — Wedding Website / App for David & Devon

**Status:** Draft v0.2 — Oct 15, 2026 (updated with open-question answers)
**Author:** Max (with Muse)
**Purpose of this doc:** Learning vehicle for the full PM loop: requirements → PRD → clickable prototype → GitHub commit. Hypothetical wedding, not a real event.
**Wedding date:** November 8, 2027 — 4:00 PM
**Venue:** The Lucy by Cescaphe, 231 S Broad St, Philadelphia, PA 19107
**Vibe:** Classic / elegant

---

## 1. Problem & Opportunity

Guests need one trusted place for everything about the wedding: when/where, schedule, travel, RSVP, registry, and answers to common questions. Today that info is scattered across texts, calls, and emails, which creates repeat questions for the couple.

This project is also Max's practice product for learning modern PM craft: turn fuzzy requirements into a crisp PRD, feed the PRD to an AI model for a clickable prototype, and ship the prototype to GitHub.

## 2. Goals & Success Metrics

**Product goals (v1):**
- A guest can find event details and RSVP in under 2 minutes on their phone.
- The couple (admin) can update details without touching code.

**Learning goals:**
- Produce a PRD that is clear enough for an AI model to generate a clickable prototype with no extra clarification.
- Commit the prototype to a GitHub repo following a real ship flow.

**Success metrics (hypothetical):**
- 90%+ of invited guests RSVP through the site (vs. texting the couple).
- Zero "where do I go / what time?" messages the week of the wedding.
- Prototype usability: 5/5 test guests complete RSVP unassisted.

## 3. Users

| Persona | Needs |
|---|---|
| **Guest** (primary) | Find date/time/venue, see schedule, RSVP, book travel, view registry, get FAQ answers — all on mobile. |
| **Couple — David & Devon** (admin) | Publish updates, track RSVP list, answer FAQs once instead of 50 times. |
| **Wedding party / family** (secondary) | Same as guest, plus maybe photo sharing (deferred to later). |

## 4. Scope

### V1 — Must-haves (confirmed)
1. **Event details & schedule** — The Lucy by Cescaphe, 231 S Broad St, Philadelphia, PA 19107. Ceremony 4:00 PM. Timeline: 4pm ceremony, 5pm cocktail hour, 6pm dinner, 8pm dancing.
2. **RSVP form** — name, attending yes/no, plus-one, meal choice (Chicken, Fish, Steak, Vegetarian), dietary restrictions. Confirmation screen after submit.
3. **FAQ** — dress code, plus-ones, kids, parking, etc.
4. **Travel & hotels** — Cambria Hotel, booking code David&Devon, book by October 1, 2027. Map/directions, parking & transport notes.
5. **Registry** — Crate & Barrel (link TBD).

Explicitly **not** in v1: Our Story page (you confirmed: keep it out), photo gallery / guest uploads, countdown timer, real backend (prototype will fake RSVP submission).

### Later / nice-to-haves
- Guest photo upload / gallery
- Countdown, live updates

### Platform decision
You confirmed **both website + native app**. PM note (unchanged): for a real wedding, a mobile-friendly website is almost always the right call — guests won't install an app for one event. For this learning project, we'll prototype a **responsive website that feels app-like on mobile** as the primary surface. That satisfies "both" for learning purposes without doubling the build. If you want a true native prototype too, we can do it as a stretch goal.

## 5. Functional Requirements

### 5.1 Home
- Hero with couple names (David & Devon), date (November 8, 2027, 4:00 PM), venue (The Lucy by Cescaphe), and one elegant photo.
- Clear CTAs: "RSVP" and "View Details".

### 5.2 Event Details & Schedule
- Venue: The Lucy by Cescaphe, 231 S Broad St, Philadelphia, PA 19107.
- Ceremony: 4:00 PM.
- Timeline: 4pm ceremony → 5pm cocktail hour → 6pm dinner → 8pm dancing.

### 5.3 RSVP (core flow)
User stories:
- As a guest, I can RSVP yes/no so the couple has a headcount.
- As a guest bringing a plus-one, I can add their name.
- As a guest with dietary needs, I can note them and choose a meal.
- As a guest, I see a confirmation after submitting so I know it worked.

Fields (v1): full name, email/phone (for confirmation), attending (yes/no), plus-one name (optional), meal choice (Chicken / Fish / Steak / Vegetarian), dietary restrictions (free text).
Behavior: on submit → confirmation screen. Prototype fakes the backend (no real data storage yet).

### 5.4 FAQ
- Accordion or list. Starter questions: dress code, plus-ones, kids, parking/transport, gifts, contact.

### 5.5 Travel & Hotels
- Cambria Hotel — booking code David&Devon, book by October 1, 2027.
- Map embed or directions link to The Lucy by Cescaphe, parking & shuttle notes.

### 5.6 Registry
- Crate & Barrel — card linking out (URL TBD). External link opens in new tab.

## 6. Design & UX

- **Vibe:** Classic / elegant — serif headlines, generous whitespace, muted palette (ivory, charcoal, gold accent), no clutter.
- **Mobile-first:** most guests will open this on their phone. Touch targets ≥ 44px, single-column layout, sticky RSVP CTA.
- **Accessibility:** sufficient color contrast, semantic headings, form labels, keyboard-navigable FAQ.

## 7. Non-Functional Requirements

- Loads fast on mobile connections (prototype: static site is fine).
- Works in modern browsers; responsive from 360px phones to desktop.
- Content editable without code (v1 prototype can hardcode; note CMS as future).

## 8. Assumptions & Resolved Questions

Assumptions:
- Hypothetical wedding — details above are placeholders for learning.
- RSVP backend is faked in the prototype; real storage comes later.
- One language (English).

Resolved (Oct 15):
1. Venue: The Lucy by Cescaphe, 231 S Broad St, Philadelphia, PA 19107 ✓
2. Ceremony time + timeline: 4:00 PM; 4pm ceremony, 5pm cocktail hour, 6pm dinner, 8pm dancing ✓
3. Meal options: Chicken, Fish, Steak, Vegetarian ✓
4. Registry: Crate & Barrel (URL TBD) ✓
5. Hotel: Cambria Hotel, code David&Devon, book by Oct 1, 2027 ✓
6. Our Story: confirmed out of v1 ✓
7. Platform: confirmed both; prototyping responsive website first (app-like on mobile) ✓

Remaining TBD for prototype content: registry URL, FAQ answers, one hero photo.

## 9. Next Steps

1. Fill in open questions above (or keep placeholders for the prototype).
2. Feed this PRD to the prototype builder with a prompt like: "Build a mobile-first, multi-page clickable prototype for this wedding PRD. Classic/elegant style. Pages: Home, Details, RSVP, FAQ, Travel, Registry. Fake the RSVP backend with a confirmation screen."
3. Review the clickable prototype, run a quick usability check (can a guest RSVP unassisted?).
4. Commit the prototype to GitHub.

---

*This is a learning PRD — meant to be clear enough that a model can build from it without follow-up questions. Tighten any vague requirement before the prototype step and you'll feel the payoff immediately.*
