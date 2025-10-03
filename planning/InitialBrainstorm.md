# Badmintor - Initial Brainstorm Session

## Project Overview

**Working Title**: Badmintor
**Purpose**: App to help plan coaching sessions for badminton with a library of training drills and activities, featuring tagging and searching functionality.

## Questions & Responses

### 1. Target Platform

**Question**: Do you want this as a web application, mobile app (iOS/Android), desktop application, or multiple platforms?

**Response**:

- Knows React well.
- Wants mobile device compatibility and offline functionality eventually.
- Thinking web application to start, then potentially moving to mobile native later.

**Follow-up Questions**:

**1a**: Since you mentioned offline functionality is important, are you thinking of using this primarily when you're on the court/gym where internet might be spotty?

- Yes, exactly that use case. Happy to be challenged on this approach.

**1b**: For the mobile experience, would a Progressive Web App (PWA) work for you initially? This would let you build with React, work offline, and be installable on mobile devices, while keeping a single codebase before potentially going native later.

- Yes, potentially. Definitely interested if PWA is easy to implement and doesn't add much complexity. Happy to explore this option more.

**1c**: Do you need to access this on multiple devices (phone, tablet, laptop) and keep data synced between them?

- Yes, would like to do heavy data entry on laptop and view session plans on mobile.

---

## Platform Decision Summary

- Start with React web application with PWA capabilities for offline use and mobile compatibility.
- Multi-device access with data sync required.
- Potential future migration to native mobile if needed.

---

### 2. User Types

**Question**: Who will be using this app? Just you as a coach, or will players/students also have access? Should there be different user roles with different permissions?

**Response**:

- Initially just for the user themselves.
- Other coaches might use it in the foreseeable future.
- Eventually players might use it.
- Suggests starting with two roles: coach and admin.

**Follow-up 2a**: For the admin vs coach distinction, are you thinking admin would be able to manage user accounts and maybe have access to all drill libraries, while coaches would manage their own drills and sessions?

- Key idea is that the drill library would be shared across all coaches.
- Admin would be able to invite users.
- Collaborative editing of drills needs to be explored further.

---

### 3. Drill Content

**Question**: How extensive is your drill library? Do you already have drills documented somewhere (like in Word docs, spreadsheets, or notes), or will we need to create a system for you to input them from scratch?

**Response**:

- Doesn't have many drills documented currently.
- Bulk input functionality not needed as a priority.

---

### 4. Drill Structure

**Question**: What information do you want to store for each drill? (e.g., name, description, difficulty level, equipment needed, player count, duration, objectives, diagrams/videos?)

**Response**:

- No diagrams or photos needed initially.
- Player level rather than difficulty level.
- Duration should be flexible.
- Learning objectives/skills focus through a tagging system (needs exploration).
- Would like to include variants of a drill.

**Follow-up 4a**: For drill variants, are you thinking of things like "beginner/intermediate/advanced versions" of the same core drill, or more like "different ways to run the same drill"?

- Initially thinking more different ways or additions.
- Loves the idea of progression variants to make drills more advanced.

---

### 5. Tagging System

**Question**: What categories/tags are most important for organizing drills? (e.g., skill areas, player levels, physical aspects, court areas, game situations)

**Response**:

- High level categories: Shot production, Footwork, Tactics, Physical.
- Each category would have several sub-tags (e.g., Shot production: high clear, drop, etc.).
- Exact structure and content of tags needs further exploration.

---

### 6. Session Planning

**Question**: Beyond browsing drills, do you want features to create complete coaching session plans? (e.g., building sessions from drills, warm-up/cool-down, timing, notes, templates)

**Response**:

- Drill library is the main feature to implement first.
- After that, definitely want ability to build sessions from drills.
- Warm-up and cool-down not important (players do this themselves).
- Timing not important - typically do 2 "toolbox" exercises (short, core skills) then 3 drills.
- Adding notes is a good idea but not a priority.
- Saving and reusing templates maybe but not that important.
- Phase 2: Browse history of planned sessions and see themes across time and coaches.
- Phase 3+: Track what kids are doing across all sessions and coaches for coordination (kids join multiple sessions with different coaches, coaches are very independent).

---

### 7. Technical Preferences

**Question**: Do you have preferences for backend/database, state management, UI framework, or hosting/deployment?

**Response**:

- Very experienced in .NET Core and SQL Server, tends towards that but willing to discuss alternatives.
- Recently used Zustand for state management but open to discussion.
- UI framework choice needs further exploration.
- Hosting and deployment in Azure due to familiarity.

---

### 8. Data Storage & Sync

**Question**: Since you want offline functionality and multi-device sync, how do you feel about data being stored locally when offline, then syncing back when online? Are you comfortable with sync conflicts, or prefer simpler approach where some features require being online?

**Response**:

- Simpler approach is fine.
- Most important offline capability is browsing drill library and viewing session plans.
- Editing/creating content can require online connection.

---

### 9. Visual Elements

**Question**: Do you anticipate wanting visual elements later? (court diagrams, sketches, photos, videos)

**Response**:

- Court diagrams showing player positions would be very cool and a simple start.
- Should plan for this sooner rather than later.
- Other visual elements (photos, videos) not that important.

---

### 10. Future Features & Success Vision

**Question**: What would make this app a "must-have" tool for badminton coaches? How would you measure success?

**Response**:

- Main value is coaches collaboratively building the drill library to share ideas.
- Like a "badminton coaching wiki."
- Session planning is secondary.
- Player tracking is a pipedream (nice to have but not core value).
- Would love to leverage AI to facilitate the collaborative drill wiki (e.g., when adding new drill, AI reviews existing drills and suggests similar ones with potential edits instead of creating duplicate).
