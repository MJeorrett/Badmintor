# Badmintor - Features & Milestones

## Milestones

### MVP - Personal Drill Library ⭐ PRIMARY VALUE

**Goal**: Create a searchable personal drill library with foundation for future collaboration.
**Success Criteria**: Single coach can add, search, and discover drills effectively. Basic AI deduplication and tag suggestions prevent duplicates and maintain quality. Foundation for collaborative coaching wiki established.

### Milestone 2 - Session Planning

**Goal**: Enable coaches to build coaching sessions from the drill library.
**Success Criteria**: Coaches can create structured sessions (typically 2 toolbox exercises + 3 drills) and save them for use on court.

### Milestone 3+ - Future Enhancements

**Goal**: Advanced AI features, session insights, and multi-coach and player coordination.
**Success Criteria**: Enhanced coaching experience with intelligent suggestions and coordination tools.

---

## Features

### MVP - Collaborative Drill Library

#### F01 - User Authentication 🔐

- User registration and login system.
- Single user access (multi-user features in future milestones).

**Implementation TODOs:**

- [ ] Implement Firebase Auth integration
- [ ] Create login/registration UI components

#### F02 - Drill Library Core 📚

- Create, edit, and delete drills.
- Personal drill library with cloud storage (Firebase Firestore).
- Drill variants support (different approaches + progression levels).
- Foundation for future multi-coach collaboration.

**Implementation TODOs:**

- [ ] Drill data model definition - **BLOCKED: Requires UX spike results (see Spikes.md - SP02)**
- [ ] Drill variant structure and relationships (different ways vs progression variants)
- [ ] Player level classification system design
- [ ] Implement CRUD operations for drills
- [ ] Create drill entry/editing UI components

#### F03 - Hierarchical Tagging System 🏷️

- Four main categories: Shot production, Footwork, Tactics, Physical.
- Sub-tags within each category (e.g., Shot production: high clear, drop, smash).
- Curated tag structure with AI-assisted tag management.
- **AI Tag Curation**: AI suggests appropriate existing tags, validates new tag requests, identifies similar tags for consolidation, and recommends hierarchy placement for new sub-tags.

**Implementation TODOs:**

- [ ] Hierarchical tagging system detailed structure (Shot production, Footwork, Tactics, Physical sub-tags)
- [ ] Tag/category data relationships
- [ ] Tag selection/creation UI components
- [ ] AI tag suggestion integration

#### F04 - Drill Search & Discovery 🔍

- Search drills by name, description, and tags.
- Filter drills by player level and categories.
- Browse and discover existing drills.

**Implementation TODOs:**

- [ ] Drill search and filtering interface design
- [ ] Implement search functionality (Firestore queries)
- [ ] Create filter UI components
- [ ] Implement drill discovery/browsing views

#### F05 - Progressive Web App (PWA) 📱

- Offline drill browsing and session viewing (Firebase offline sync).
- Multi-device synchronization across laptop and mobile.
- Installable on mobile devices (Firebase Hosting).
- Optimized for on-court usage without internet connectivity.

**Implementation TODOs:**

- [ ] Offline functionality scope and limitations - **DEFERRED: Not MVP priority**
- [ ] PWA manifest and service worker setup
- [ ] Mobile-responsive design implementation
- [ ] App installation prompts and UX

#### F06 - Basic AI Deduplication 🤖

- Suggest similar existing drills when creating new ones to prevent duplicates.
- AI-powered similarity detection using Google Gemini via Firebase Cloud Functions.
- Triggered automatically when new drills are created in Firestore.
- **AI Tag Intelligence**: Suggest appropriate tags during drill creation, prevent tag duplication (e.g., "footwork" vs "foot work"), and recommend tag improvements.

**Implementation TODOs:**

- [ ] Basic AI deduplication for MVP - scope and implementation approach - **SPIKE NEEDED: AI deduplication PoC (see Spikes.md - SP04)**
- [ ] Firebase Cloud Function for drill similarity detection
- [ ] Integration with drill creation workflow
- [ ] UI for displaying similar drill suggestions

### Milestone 2 - Session Planning

#### F07 - Session Planning 📋

- Build sessions from selected drills.
- Session structure: 2 "toolbox" exercises + 3 drills.
- Add notes to sessions.
- Save and reuse session plans.

**Implementation TODOs:**

- [ ] Session data model definition
- [ ] Session creation workflow (2 toolbox + 3 drills structure)
- [ ] Session builder UI components
- [ ] Session notes and management features

### Milestone 3+ - Future Enhancements

#### F08 - Advanced AI Coaching Assistant 🧠

- Enhanced drill suggestions and improvements.
- **Advanced Tag Analytics**: Monitor tag usage patterns, suggest tag system improvements, and provide intelligent tag consolidation recommendations.

**Implementation TODOs:**

- [ ] AI-assisted drill creation workflow and similarity detection algorithms
- [ ] Enhanced AI coaching suggestions and pattern recognition
- [ ] Advanced tag analytics and recommendations

#### F09 - Court Diagrams & Visual Elements 🏸

- Visual court layouts and player positioning tools.

**Implementation TODOs:**

- [ ] Court diagram data structure and storage approach
- [ ] Visual court layout interface design
- [ ] Diagram creation and editing tools

#### F10 - Session Analytics & History 📊

- Historical analysis and coaching pattern insights.
- Month-long themed training support with drill variety suggestions.
- AI recommendations for different drills that train the same skills to prevent player boredom.

**Implementation TODOs:**

- [ ] Session history and theme analysis features
- [ ] Analytics dashboard and insights UI
- [ ] AI-powered training variety recommendations

#### F11 - Multi-Coach Coordination 👥

- Player progress tracking across coaches and sessions.

**Implementation TODOs:**

- [ ] Collaborative editing workflow for shared drill library
- [ ] Version control approach for drill changes
- [ ] User roles and permissions structure
- [ ] Cross-coach coordination features design
- [ ] Data privacy and sharing permissions for multi-coach environment
- [ ] Player progress tracking across multiple coaches

---

## User Stories

### MVP - Collaborative Drill Library

#### F01 - User Authentication 🔐

**As a badminton coach, I want to:**

- **US01**: Create an account so that I can access my drill library.

#### F02 - Drill Library Core 📚

**As a badminton coach, I want to:**

- **US02**: Add new drills to my personal library to build my coaching knowledge base.
- **US05**: Edit my drills to improve them as I refine my coaching approaches.
- **US06**: See drill variants so that I can adapt activities for different skill levels.

#### F03 - Hierarchical Tagging System 🏷️

**As a badminton coach, I want to:**

- **US04**: Tag drills with categories so that they are easy to find and organize.
- **US04a**: Get AI suggestions for appropriate tags when creating drills so that tagging is consistent and accurate.

#### F04 - Drill Search & Discovery 🔍

**As a badminton coach, I want to:**

- **US03**: Search for drills by skill focus so that I can find appropriate activities for my sessions.

#### F05 - Progressive Web App (PWA) 📱

**As a badminton coach, I want to:**

- **US07**: Browse the drill library offline so that I can review drills when I'm on court without internet.

#### F06 - Basic AI Deduplication 🤖

(No specific user stories - this is a background feature that supports other functionality)

### Milestone 2 - Session Planning

#### F07 - Session Planning 📋

**As a badminton coach, I want to:**

- **US08**: Build a session from selected drills so that I have a structured plan for coaching.
- **US09**: Follow the 2 toolbox + 3 drills structure so that my sessions are well-balanced.
- **US10**: Add notes to my session plan so that I remember key coaching points.
- **US11**: Save session plans so that I can reuse successful structures.
- **US12**: View my session plan offline on my mobile so that I can reference it during coaching.

### Milestone 3+ - Future Enhancements

#### F08 - Advanced AI Coaching Assistant 🧠

**As a badminton coach, I want to:**

- **US13**: Get advanced AI suggestions for drill improvements and coaching patterns.

#### F09 - Court Diagrams & Visual Elements 🏸

**As a badminton coach, I want to:**

- **US14**: Use visual court diagrams to illustrate drill setups.

#### F10 - Session Analytics & History 📊

**As a badminton coach, I want to:**

- **US15**: Analyze my coaching history and discover theme patterns.
- **US15a**: Get AI suggestions for different drills that train the same theme so that I can maintain focus while providing variety to prevent player boredom.

#### F11 - Multi-Coach Coordination 👥

**As a badminton coach, I want to:**

- **US16**: Coordinate with other coaches working with the same players.

---

## Notes

See planning/TODO.md for detailed technical decisions and implementation details.
