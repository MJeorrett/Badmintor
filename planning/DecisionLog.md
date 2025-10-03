# Badmintor - Decision Log

This document tracks all architectural and product decisions made.

## Pending Decisions

- **Azure hosting strategy**: App Service vs Container Apps vs Functions for .NET API
- **Offline data synchronization**: Detailed implementation approach with Firebase
- **Drill data model**: Structure for variants, tags, and future extensibility
- **AI integration**: Azure OpenAI vs alternatives, cost optimization
- **PWA implementation**: Service worker strategy and offline capabilities scope

## Architecture Decisions

### AD-001: Backend Technology Stack

**Date**: October 3, 2025  
**Status**: Pending Validation  
**Decision**: Hybrid Firebase + .NET API approach  
**Rationale**:

- Firebase provides excellent offline sync and real-time capabilities for core drill data
- .NET API leverages existing expertise for complex AI processing logic
- Firebase Admin SDK allows .NET API to integrate with Firebase data
  **Alternatives Considered**: Pure .NET + SQL Server, Pure Firebase, Supabase  
  **Validation**: SP01 - Firebase Integration Validation spike

### AD-002: Frontend UI Framework

**Date**: October 3, 2025  
**Status**: Decided  
**Decision**: Tailwind CSS  
**Rationale**:

- Extensive existing experience with Tailwind
- Lightweight and flexible compared to Material-UI
- Good performance for PWA requirements
- Doesn't constrain design choices
  **Alternatives Considered**: Material-UI, Ant Design, plain CSS

### AD-003: State Management Approach

**Date**: October 3, 2025  
**Status**: Pending UX Design  
**Decision**: To be determined based on drill management UX complexity  
**Rationale**:

- State management needs depend heavily on drill creation/editing workflow
- Firebase handles data persistence, main need is local UI state
- Simple React state may be sufficient for MVP
  **Alternatives Considered**: Zustand, Redux Toolkit, Context API  
  **Validation**: SP02 - Drill Management UX Design spike

## Product Decisions

### PD-001: MVP Scope - Single User

**Date**: October 3, 2025  
**Status**: Decided  
**Decision**: MVP will be single-user focused, not multi-coach collaboration  
**Rationale**:

- Simpler authentication and data model for initial development
- Allows focus on core drill library functionality
- Multi-coach features moved to later milestones
  **Impact**: Simplified user management, no role-based permissions needed initially

### PD-002: Equipment Filtering Exclusion

**Date**: October 3, 2025  
**Status**: Decided  
**Decision**: Remove equipment filtering from MVP drill search  
**Rationale**:

- Badminton equipment is standard and ubiquitous
- Not a useful filtering criterion for drill selection
- Simplifies search interface
  **Impact**: Reduced complexity in search/filtering UI

---

## Decision Template

For future decisions, use this template:

### AD-XXX: Decision Title

**Date**: [Date]  
**Status**: [Decided/Pending/Superseded]  
**Decision**: [What was decided]  
**Rationale**: [Why this decision was made]  
**Alternatives Considered**: [Other options that were evaluated]  
**Impact**: [How this affects the project]  
**Validation**: [If spike or testing needed]
