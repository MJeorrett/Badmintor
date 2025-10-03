# Badmintor - Technical Spikes

## Planned Spikes

This document is used to track all technical validation spikes.

### 🔥 SP01 - Firebase Integration Validation

**Goal**: Validate Firebase as complete backend solution for MVP
**Success Criteria**:

- [ ] Firebase project setup with React app
- [ ] Authentication flow working (sign up/login)
- [ ] Basic Firestore CRUD operations for drill data
- [ ] Firebase Cloud Functions setup and basic function deployment
- [ ] Cloud Function triggered by Firestore changes
- [ ] Offline functionality testing (create/read drills offline)
- [ ] Data sync when comes back online
- [ ] Basic security rules for single user

**Estimated Effort**: 1-2 days
**Priority**: High - blocking other technical decisions

**Deliverables**:

- [ ] Working Firebase + React + Cloud Functions prototype
- [ ] Technical assessment document (pros/cons/gotchas)
- [ ] Decision on whether to proceed with Firebase ecosystem

---

### 🎯 SP02 - Drill Management UX Design

**Goal**: Design the drill creation/editing experience to understand state management needs
**Success Criteria**:

- [ ] Wireframe/mockup of drill creation form
- [ ] Define drill data structure (with variants, tags, etc.)
- [ ] Map out user workflow for creating/editing drills
- [ ] Identify complex UI state requirements
- [ ] Determine if simple React state is sufficient vs needing Zustand/Redux

**Estimated Effort**: 0.5-1 day
**Priority**: High - influences multiple other technical decisions

**Deliverables**:

- [ ] Drill creation workflow documentation
- [ ] Data model definition
- [ ] State management requirements analysis

---

### 📱 SP03 - PWA Implementation Validation

**Goal**: Validate PWA setup and offline capabilities with React + Firebase
**Success Criteria**:

- [ ] PWA setup with service worker for offline functionality
- [ ] App installable on mobile devices
- [ ] Offline drill browsing working
- [ ] Data sync when reconnecting
- [ ] Cross-device testing (laptop/mobile)

**Estimated Effort**: 1 day
**Priority**: High - core requirement for on-court usage

**Deliverables**:

- [ ] Working PWA implementation approach
- [ ] Offline strategy documentation
- [ ] Cross-device sync validation

---

### 🤖 SP04 - AI Deduplication Proof of Concept

**Goal**: Validate basic AI similarity detection for drill deduplication using Google AI
**Success Criteria**:

- [ ] Test Gemini API integration via Firebase Cloud Functions
- [ ] Basic similarity detection between drill descriptions
- [ ] Simple prompt engineering for drill comparison
- [ ] Cost estimation for MVP usage levels with Gemini
- [ ] Cloud Function triggered by drill creation in Firestore

**Estimated Effort**: 1-2 days
**Priority**: Medium - nice to have for MVP, essential for collaboration

**Deliverables**:

- [ ] Working AI similarity detection in Cloud Functions
- [ ] Gemini cost analysis and recommendation
- [ ] Integration approach with Firestore triggers---

## Completed Spikes

(None yet)
