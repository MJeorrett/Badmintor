# Badmintor 🏸

_A collaborative drill library and session planning tool for badminton coaches._

> :construction: UNDER DEVELOPMENT :construction:
> Badmintor is currently in the early design phase. The first version will be a personal tool for me to use. The multi-user collaborative features will come later.

### Key Features

- **Collaborative Knowledge Base**: Collaboratively build and search a rich library of badminton drills.
- **AI-Assisted Organization**: Smart suggestions help maintain a well-organized drill library
- **Offline Capability**: Works on court without internet connection - perfect for gym environments
- **Session Planning**: Build structured coaching sessions with intelligent drill recommendations.

## Current Status

🚧 **Project Phase**: Planning & Architecture Design

### ✅ Completed

- Initial brainstorming and requirements gathering
- Feature definition with milestones and user stories
- Technical architecture planning
- Spike identification for key technical decisions

### 🔄 In Progress

- Technical validation spikes (Firebase, PWA, AI integration)
- Data model design
- MVP scope finalization

### 📋 Next Steps

- Execute technical spikes
- Begin MVP development
- Single-user drill library implementation

## :construction: Architecture Overview

This is my current thinking for the architecture but this may evolve based on spike outcomes.

**Frontend**: React + PWA for offline capabilities  
**Backend**: Firebase ecosystem (Firestore, Cloud Functions, Auth, Hosting)  
**State Management**: To be determined based on UX complexity (likely React built-ins)  
**AI Integration**: Google Gemini via Firebase Cloud Functions for drill similarity and suggestions  
**Hosting**: Firebase Hosting (unified ecosystem)

## Milestones

### 🎯 MVP - Personal Drill Library

- Single-user drill management (CRUD operations)
- Hierarchical tagging system
- Search and filtering capabilities
- Basic AI deduplication
- PWA with offline browsing

### 📋 Milestone 2 - Session Planning

- Build sessions from drill library
- 2 "toolbox" exercises + 3 drills structure
- Session notes and reusability
- Offline session viewing

### :family: Milestone 3+ - Collaborative Features & more :robot:

- Multi-coach collaboration
- Advanced AI coaching assistant
- Court diagrams and visual elements
- Session analytics and history
- Cross-coach coordination
