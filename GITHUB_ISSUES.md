# J'étais là 95 — GitHub Issues Roadmap

This file contains the project's future tasks and ideas.

The core experience is already functional: traces can be created, displayed as map pins, and stored in Firebase / Firestore.

These issues are intentionally separated from the core philosophy. New features should not turn the project into a conventional social network.

---

## 🔴 Priority / Core

### 1. Add email notifications for reports

**Goal:**  
Send a notification to the maintainer whenever a visitor reports a trace.

**Target email:**  
`med2026etd@gmail.com`

**Requirements:**
- Keep reports stored in Firestore.
- Send an email when a new report is created.
- Do not expose the maintainer's email address to visitors.
- Do not allow visitors to choose the email recipient.
- Keep manual moderation as the final decision.

---

### 2. Strengthen anti-spam protection

**Goal:**  
Prevent automated abuse without introducing accounts or social profiles.

Possible measures:
- rate limiting
- Firebase App Check
- server-side validation
- message creation limits
- suspicious activity protection

**Constraint:**  
Do not introduce usernames, accounts, followers, karma, or reputation.

---

### 3. Review Firestore security rules

**Goal:**  
Continuously verify that visitors can only perform the operations they actually need.

Requirements:
- visitors can read visible traces
- visitors can create valid traces
- visitors can create reports
- visitors cannot modify existing traces
- visitors cannot read private moderation data
- visitors cannot modify reports
- visitors cannot redirect email notifications

---

## 🟠 Moderation

### 4. Improve the moderation workflow

Create a simple way for the maintainer to review:

- reported trace
- report reason
- optional report note
- date
- trace ID
- current status

Possible future statuses:

- `new`
- `reviewed`
- `removed`
- `dismissed`

---

### 5. Add a private moderation interface

Create a small private/admin interface for the maintainer.

Possible features:
- list reports
- open the reported trace
- remove a trace
- mark a report as reviewed
- inspect basic moderation information

**Important:**  
This interface must not become visible or accessible to ordinary visitors.

---

### 6. Add better content validation

Improve validation for:
- empty messages
- excessively long messages
- malformed coordinates
- invalid reason values
- abusive automated submissions

Avoid overly aggressive censorship.

The goal is moderation, not controlling what people are allowed to think.

---

## 🟡 Map & Discovery

### 7. Improve performance with many traces

The project currently loads a limited number of traces.

Investigate scalable loading when the database becomes large.

Possible solutions:
- geographic queries
- clustering
- pagination
- viewport-based loading
- server-side filtering

The map should remain usable even with a large number of traces.

---

### 8. Improve marker clustering

When many traces are close together:

- group markers
- zoom naturally into clusters
- keep individual traces discoverable

Do not hide traces simply because they are unpopular.

---

### 9. Improve "Random Trace"

Random Trace should provide a genuinely interesting discovery experience.

Possible improvements:
- random visible trace
- random geographic area
- avoid immediate repetition
- smooth map movement
- preserve the quiet feeling of the project

---

### 10. Improve "Near Me"

Requirements:
- request geolocation only after the user chooses Near Me
- never request location automatically
- clearly explain why location is requested
- work well on mobile browsers

---

### 11. Improve empty locations

Expand the "Quiet Place / You Could Be First" experience.

An empty area should feel intentional rather than broken.

---

## 🟢 Interface

### 12. Improve mobile UX

Test the complete interface on:
- small phones
- large phones
- tablets
- desktop browsers

Check:
- draggable windows
- buttons
- map controls
- text input
- keyboard behavior
- modal windows
- taskbar
- screen rotation

---

### 13. Improve Windows 95 authenticity

Continue refining:
- title bars
- beveled buttons
- taskbar
- window shadows
- icons
- system dialogs
- boot sequence
- retro typography

Do not sacrifice usability for nostalgia.

---

### 14. Improve theme switcher

Keep the theme switcher immediate and simple.

Requirements:
- one-click theme change
- no page reload if possible
- remember the local preference
- preserve readability and accessibility

---

### 15. Accessibility pass

Review:
- keyboard navigation
- focus states
- text contrast
- screen-reader labels
- button labels
- map controls
- reduced-motion preference
- mobile accessibility

---

## 🔵 Privacy

### 16. Privacy review

Perform a complete privacy review.

Verify that the project does not intentionally collect:
- usernames
- emails from visitors
- profiles
- social graphs
- advertising identifiers
- unnecessary analytics
- fingerprinting data

Also document the distinction between the project's own data collection and technical logs created by hosting/network infrastructure.

---

### 17. Review local storage usage

Document exactly what is stored locally in the browser.

Possible local preferences:
- map position
- zoom level
- language
- sound preference
- map visibility
- theme preference

No personal identity information should be stored unnecessarily.

---

## 🟣 Experience

### 18. Refine the "Ocean of Words" concept

Explore ways to make the map feel like a living ocean of anonymous traces without introducing:

- likes
- followers
- feeds
- rankings
- popularity scores

The experience should encourage discovery rather than engagement farming.

---

### 19. Add more philosophical / contextual text

Review:
- About
- Help / Protocol
- Quiet Place
- Leave a Trace
- first-visit experience

Keep the writing short, mysterious, and human.

---

### 20. Improve the boot sequence

Refine the Windows 95 / DOS-inspired startup experience.

Goals:
- short
- nostalgic
- not annoying
- skippable where appropriate
- mobile-friendly

---

### 21. Optional retro sound improvements

The current static sound is optional.

Possible improvements:
- better 95-style static
- mute persistence
- respect browser autoplay restrictions
- respect reduced-motion / accessibility preferences where appropriate

---

## ⚪ Data & Maintenance

### 22. Create a manual database maintenance routine

Periodically review:
- reports
- inappropriate content
- spam
- malformed traces
- abandoned test traces

Do not automatically delete old traces merely because they are old.

---

### 23. Remove test data before public launch

Before announcing the project publicly:

- remove development/test traces
- verify production Firebase configuration
- verify GitHub Pages deployment
- test the complete visitor flow

---

### 24. Keep a stable backup version

Before major changes:

- keep a known-working `index.html`
- document the current Firebase configuration
- avoid modifying the production version directly without a backup

---

## 🧪 Testing

### 25. End-to-end testing

Test the complete flow:

1. Open the website.
2. Explore the map.
3. Create a trace.
4. Confirm the pin appears.
5. Refresh the page.
6. Confirm the trace remains.
7. Open the trace.
8. Submit a report.
9. Confirm the report reaches Firestore.
10. Confirm moderation workflow works.

---

### 26. Browser compatibility testing

Test on:
- Chrome
- Brave
- Firefox
- Safari
- Edge
- Android browsers
- iOS browsers

---

### 27. Offline / poor connection testing

Test behavior when:
- connection is slow
- connection disappears while writing
- Firebase temporarily fails
- map tiles fail to load

The interface should show understandable error messages rather than silently failing.

---

## 🚫 Product philosophy guardrails

These are not feature requests. They are constraints.

### Do NOT add:
- user profiles
- usernames
- followers
- following
- likes
- dislikes
- karma
- public reputation
- infinite social feed
- advertising
- engagement scoring
- popularity rankings
- unnecessary analytics
- identity-based recommendation systems

The project should remain a **place for anonymous traces**, not become another social network.

---

## Final question for future features

Before implementing any new feature, ask:

> **Does this make J'étais là 95 a better museum of anonymous words, or does it make it more like a social network?**

If the answer is the second one, reconsider the feature.
