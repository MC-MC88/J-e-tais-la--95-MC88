# J'étais là 95

> **A living museum of anonymous words, floating over Earth.**

**J'étais là 95** is an anonymous, map-based digital space inspired by the atmosphere of **Windows 95**.

It is not a social network.  
It is not a feed.  
It is not a platform for building an identity.

It is simply a place where someone can leave a few words behind.

---

## The idea

One day, someone may open the map and discover a sentence left by a stranger.

Another person may come later and leave something nearby.

There is no profile to follow, no name to remember, and no algorithm deciding what deserves attention.

The map becomes an **ocean of human traces**.

Every pin is a small proof that someone was there, thought something, felt something, remembered something, or simply wanted to leave a sentence behind.

The question behind the project is simple:

> **What do anonymous humans do when they are given a place to leave words freely, without having to become someone?**

---

## The philosophy

### No identity

There are no:

- usernames
- profiles
- avatars
- followers
- reputation scores
- karma
- public identities
- social rankings

The project is interested in **words, not identities**.

A message does not need a person attached to it to have meaning.

### No feed

There is no infinite scrolling feed designed to keep people online.

The map is the interface.

You explore places.  
You discover traces.  
You decide where to look.

### No likes

There is no like button.

Instead, if a message affects you, you can leave another trace nearby.

That trace can become a kind of geographical response.

Someone may discover it later without ever knowing who wrote the original message.

### No algorithmic popularity

The project does not try to determine which human thought is the most important.

A profound sentence and a completely ordinary sentence can coexist on the same map.

The visitor decides what matters.

### No expiration

Traces do not automatically disappear after 30 days.

The ocean should accumulate memories.

Content may be manually moderated and cleaned when necessary, but there is no automatic countdown that destroys old traces simply because they are old.

---

## Why Windows 95?

The Windows 95 aesthetic is intentional.

It represents a different relationship with computers:

- simple interfaces
- visible controls
- small windows
- gray surfaces
- blue title bars
- buttons that look like buttons
- a feeling that software was a place rather than an endless stream

The visual language is nostalgic, but the idea is contemporary.

**Old interface. New experiment.**

The project uses the retro aesthetic as a frame for something much more human and much less technological:

**words left by strangers.**

---

## The map

The Earth is the museum.

The map uses a quiet grayscale presentation so that the words remain the focus.

A pin represents a trace.

There is no requirement for the trace to be important, profound, beautiful, or clever.

It can simply say:

> "I was here."

Or anything else the writer wants to leave behind.

---

## A different kind of reply

Traditional social platforms turn replies into conversations attached to profiles.

Here, geography becomes the thread.

If you discover a message you want to answer, you can leave your own message somewhere nearby.

The answer does not have to mention the original author.

It may simply exist beside the original trace.

Someone, someday, may discover both.

This creates a strange form of communication between people who may never know each other.

---

## Privacy

The project intentionally avoids building a traditional identity system.

There are:

- no accounts
- no public profiles
- no email registration
- no usernames
- no follower system
- no public identity attached to a trace
- no frontend analytics or fingerprinting by the project

The **Near Me** feature only requests browser geolocation when the visitor explicitly chooses to use it.

Local preferences such as map position, language, sound, and map visibility can be stored locally in the browser.

### An important distinction

The project does not claim that internet infrastructure can provide absolute anonymity.

Hosting providers, browsers, networks, and other infrastructure may create technical logs outside the project's own identity system.

The goal is therefore not to promise impossible anonymity.

The goal is to **avoid collecting and displaying identity as part of the experience**.

---

## Moderation

An anonymous space needs moderation.

Visitors can report a trace.

Reports are intended for manual review.

The project deliberately does not try to replace human judgment with a popularity system or an automated social reputation mechanism.

The maintainer can review the database and remove inappropriate content manually.

This is part of the experiment:

> Can an anonymous place remain human without becoming a social network?

---

## Current technology

The project is intentionally simple.

### Frontend

- HTML
- CSS
- JavaScript
- Leaflet
- OpenStreetMap
- Windows 95-inspired UI

### Backend

The project migrated from an early Google Sheets / Google Apps Script prototype to **Firebase / Cloud Firestore**.

Firestore currently stores traces and reports.

Anonymous Firebase authentication is used so visitors can interact with the database without creating accounts.

### Hosting

The project is intended to be hosted through **GitHub Pages**.

---

## From prototype to Firebase

The project originally experimented with Google Sheets and Google Apps Script as a lightweight backend.

That approach exposed practical problems around browser form encoding and JSON handling.

The backend was later migrated to Firebase.

The migration keeps the same core philosophy while providing a more appropriate database for the map.

The important lesson from the prototype was:

> The technology should serve the experiment, not become the experiment.

---

## Main features

- 🗺️ Interactive world map
- 📍 Anonymous geographical traces
- 🎲 Random Trace
- 🔦 Lighthouse
- 📍 Near Me
- 🌍 World exploration
- 📝 Leave a Trace
- ❓ Help / Protocol
- ℹ️ About
- ⚙️ Settings
- 🪟 Windows 95-inspired interface
- 📱 Responsive mobile experience
- 🔊 Optional retro static sound
- 🌑 Map ON/OFF mode
- 🕯️ Quiet places where a visitor can become the first trace
- 🚨 Trace reporting
- 🔐 No user account system
- 📊 No likes, followers, karma, or reputation

---

## The "Quiet Place"

An empty location is not an error.

It is an invitation.

When there are no traces nearby, the project can present the idea of a quiet place:

> **You could be the first.**

This turns emptiness into part of the experience.

---

## What this project is not

J'étais là 95 is deliberately **not**:

- Facebook
- Instagram
- X
- Reddit
- a dating application
- a chat application
- a personal diary platform
- a popularity contest
- a content recommendation engine

It does not try to maximize engagement.

It tries to create a place worth visiting.

---

## The experiment

The project is ultimately a social experiment.

Give people:

1. a map,
2. anonymity,
3. a blank space,
4. a few words,
5. no audience they can build,
6. no reputation they can gain,

and see what happens.

Maybe they will write jokes.

Maybe memories.

Maybe confessions.

Maybe poetry.

Maybe coordinates to somewhere important.

Maybe nothing at all.

All of it becomes part of the museum.

---

## A living museum

A traditional museum preserves objects.

This project preserves **moments of anonymous expression**.

The museum has no walls.

Its rooms are cities, roads, forests, deserts, oceans, neighborhoods and places that may never have visitors again.

Someone leaves a sentence.

The sentence waits.

Another person finds it.

And for a moment, two strangers exist in the same place without ever meeting.

---

## Project principles

The project tries to follow a few simple rules:

> **Words before identities.**

> **Discovery before recommendation.**

> **Place before profile.**

> **Anonymity before reputation.**

> **Human judgment before popularity.**

> **A quiet experience before endless engagement.**

---

## Status

The project is currently functional with Firebase and Firestore.

The core experience works:

- traces can be created,
- traces appear as map pins,
- traces are stored in Firestore,
- the database can be manually managed by the maintainer.

Further improvements are tracked separately in the project's GitHub Issues.

---

## Future direction

The project may evolve, but its philosophy should remain stable.

Possible future work includes:

- stronger anti-spam protection
- improved moderation workflow
- email notifications for reports
- better mobile interaction
- performance improvements for large numbers of traces
- additional retro interface details
- accessibility improvements
- careful privacy hardening

New features should be evaluated against one question:

> **Does this make the museum better, or does it turn the museum into another social network?**

---

## Copyright

**Copyright :mohamed005cheikh@gmail.com | by MC88**
