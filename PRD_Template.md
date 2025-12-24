# PRD Template: [Feature Name]

**Date:** [Date]  
**Owner:** [Your Name]  
**Status:** [Draft / In Review / Approved / In Development / Shipped]  
**Priority:** [P0 / P1 / P2 / P3]

---

## Executive Summary

**One-line description:** [What is this feature in one sentence?]

**Problem:** [What user problem does this solve?]

**Solution:** [How will this feature solve it?]

**Success Metric:** [How will we measure success?]

---

## Background & Context

### Why Now?
[Why is this the right time to build this feature?]

### User Research
[What have we learned from users? Include quotes, data, or observations.]

### Related Work
- Link to existing features this builds on
- Competitor analysis if relevant
- Prior attempts or related discussions

---

## Goals & Non-Goals

### Goals
1. [Primary goal]
2. [Secondary goal]
3. [Tertiary goal]

### Non-Goals (Explicit Scope Limitations)
- [What we're NOT doing in this version]
- [Future enhancements we're deferring]
- [Related problems we're not solving]

---

## User Stories

### Primary User Stories
1. **As a** [user type]  
   **I want** [feature/capability]  
   **So that** [benefit/value]  
   **Acceptance criteria:**
   - [ ] [Specific, testable criteria]
   - [ ] [Another criteria]

2. **As a** [user type]  
   **I want** [feature/capability]  
   **So that** [benefit/value]  
   **Acceptance criteria:**
   - [ ] [Criteria]

### Edge Cases & Error States
1. [Edge case scenario and expected behavior]
2. [Error state and how we handle it]

---

## User Experience

### User Flow
```
[Start State]
    ↓
[User Action 1]
    ↓
[System Response 1]
    ↓
[User Action 2]
    ↓
[End State]
```

### Mockups/Wireframes
[Include screenshots, Figma links, or ASCII art for simple flows]

### Key Interactions
1. **[Interaction 1]:** [Description]
2. **[Interaction 2]:** [Description]

### Error Handling
| Error Scenario | User Experience | Technical Handling |
|---------------|-----------------|-------------------|
| [Scenario] | [What user sees] | [How system handles] |

---

## Technical Requirements

### Functional Requirements
1. [Requirement 1 with acceptance criteria]
2. [Requirement 2 with acceptance criteria]

### Non-Functional Requirements

**Performance:**
- [Load time requirement]
- [Response time requirement]

**Security:**
- [Security considerations]
- [Data privacy requirements]

**Accessibility:**
- [WCAG compliance level]
- [Keyboard navigation requirements]

**Browser/Device Support:**
- [Supported browsers]
- [Mobile requirements]

### Data Model Changes
```typescript
// New or modified interfaces
interface NewDataStructure {
  // fields
}
```

### API Changes
[If applicable: new endpoints, modified responses, etc.]

### Dependencies
- [External library needed]
- [Another feature this depends on]
- [Third-party service integration]

---

## Technical Approach (High-Level)

### Architecture Changes
[How does this fit into existing architecture?]

### Key Components
1. **[Component Name]:** [What it does]
2. **[Component Name]:** [What it does]

### Migration Plan
[If changing existing features: how do we migrate users/data?]

### Rollout Strategy
- [ ] Feature flag for gradual rollout?
- [ ] Beta testing with subset of users?
- [ ] A/B test different variants?

---

## Success Metrics

### Primary Metrics
1. **[Metric Name]:** [Target] → [How we measure]
2. **[Metric Name]:** [Target] → [How we measure]

### Secondary Metrics
1. **[Metric Name]:** [Target] → [How we measure]

### Baseline (Current State)
- [Metric]: [Current value]
- [Metric]: [Current value]

### Target (Post-Launch)
- [Metric]: [Target value]
- [Metric]: [Target value]

### Timeline for Measurement
- Day 1: [What we expect to see]
- Week 1: [What we expect to see]
- Month 1: [What we expect to see]

---

## Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| [Risk description] | High/Med/Low | High/Med/Low | [How we mitigate] |
| [Risk description] | High/Med/Low | High/Med/Low | [How we mitigate] |

---

## Open Questions

1. [Question that needs answering before development?]
2. [Design decision that needs input?]
3. [Technical uncertainty to resolve?]

---

## Timeline & Resources

### Estimated Timeline
- **Design:** [X days/weeks]
- **Development:** [X days/weeks]
- **Testing:** [X days/weeks]
- **Launch:** [Target date]

### Required Resources
- **Engineering:** [X developers for Y time]
- **Design:** [X designers for Y time]
- **Testing:** [X testers for Y time]
- **Other:** [PM, Marketing, etc.]

### Milestones
- [ ] PRD approved - [Date]
- [ ] Design complete - [Date]
- [ ] Development complete - [Date]
- [ ] Testing complete - [Date]
- [ ] Launch - [Date]

---

## Launch Plan

### Pre-Launch Checklist
- [ ] Feature complete and tested
- [ ] Documentation updated
- [ ] Analytics instrumented
- [ ] Error monitoring in place
- [ ] Rollback plan ready
- [ ] Support team briefed

### Communication Plan
- [ ] Announcement blog post
- [ ] In-app notification
- [ ] Email to users
- [ ] Social media posts
- [ ] User guide/tutorial

### Support Plan
- [ ] FAQ prepared
- [ ] Support team trained
- [ ] Escalation path defined

---

## Post-Launch

### Monitoring Plan
- Monitor [metric] daily for first week
- Weekly review of [metrics] for first month
- Respond to user feedback within 24 hours

### Iteration Plan
- Gather feedback for 2 weeks
- Review metrics after 1 month
- Plan improvements for v2

### Success Review
- [ ] 1 week post-launch review
- [ ] 1 month post-launch review
- [ ] Decision: iterate, maintain, or deprecate

---

## Appendix

### Research & References
- [Link to user research]
- [Link to competitive analysis]
- [Link to technical spike]

### Change Log
| Date | Change | Author |
|------|--------|--------|
| [Date] | [What changed] | [Who] |

---

## Sign-Off

**PRD Author:** [Name] - [Date]  
**Tech Lead Review:** [Name] - [Date]  
**Design Review:** [Name] - [Date]  
**Final Approval:** [Name] - [Date]
