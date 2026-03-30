# Backlog Refinement Summary - EcoCentre-Org/esave Project

**Generated:** 2026-03-30 19:19:44  
**Repository:** EcoCentre-Org/esave

## Executive Summary

Analysis of 9 backlog items (#32-#41) in the Backlog stage of the esave project. This document identifies key discussion points needed to refine and clarify requirements before development.

---

## Detailed Backlog Analysis

### #32 - Security Review  
**Status:** Open | **Assigned to:** eco-sandeep | **Comments:** 1 | **Sub-issues:** 1

**Current Description:** Security review

**Discussion Points for Refinement:**
- **Scope Definition:** What specific areas require security review? (Authentication, data encryption, API endpoints, database security, third-party integrations?)
- **Acceptance Criteria:** What defines "complete"? (OWASP Top 10 compliance, penetration testing results, code audit checklist?)
- **Timeline & Dependencies:** When is this needed? Does it block other items like #34 (Captcha) and #40 (MySQL upgrade)?
- **Tools & Resources:** Internal review or external audit firm? Budget allocated?
- **Action Item:** Check existing comment (1) for discussion context

---

### #34 - Captcha on Registration  
**Status:** Open | **Assigned to:** Unassigned | **Comments:** 1

**Current Description:** Registering a new account should request captcha

**Discussion Points for Refinement:**
- **Captcha Service:** Which provider? (Google reCAPTCHA v3, hCaptcha, Cloudflare Turnstile?)
- **Integration Point:** When in registration flow? (Before form validation, after email verification, or both?)
- **User Experience:** How to handle accessibility? (Audio challenge alternative, easy refresh option?)
- **Bot Protection Level:** What's the false positive/negative tolerance?
- **Compliance:** GDPR implications for data collection?
- **Action Item:** Review the 1 existing comment for decision history

---

### #35 - Referral Points Earning Logic  
**Status:** Open | **Assigned to:** Unassigned | **Comments:** 0

**Current Description:** Referral points earning logic - Need to discuss requirement with Steve

**Discussion Points for Refinement:**
- **🔴 BLOCKER:** No owner assigned; pending discussion with Steve
- **Points Formula:** 1:1 ratio? Tiered rewards based on referrer level? Bonus for milestones?
- **Caps & Limits:** Maximum points per referral? Daily/monthly earning caps?
- **Expiration:** Do referral points expire? How long are they valid?
- **Redemption:** What can users do with points? (Discounts, premium features, cash out?)
- **Dashboard Integration:** Where/how do users see their referral earnings?
- **Action Item:** Schedule discussion with Steve; clarify requirements before assignment

---

### #36 - Mobile Home Shortcut  
**Status:** Open | **Assigned to:** Unassigned | **Comments:** 0

**Current Description:** Enable user to add website short cut to Mobile Home screen

**Discussion Points for Refinement:**
- **Platform Support:** iOS only? Android? Web-to-app? (Affects implementation significantly)
- **Implementation Method:** PWA Web App Manifest? Native bridge? Intent-based on Android?
- **UX Placement:** Where's the button in the UI? (Settings, menu, after first login?)
- **Icon & Branding:** Use default or custom icon? Logo from brand guidelines (#38)?
- **Error Handling:** What if device doesn't support? Graceful degradation?
- **Analytics:** Track how many users use this feature?
- **Action Item:** Clarify platform requirements; coordinate with #38 (Brand guidelines)

---

### #37 - Update Icons  
**Status:** Open | **Assigned to:** Unassigned | **Comments:** 0

**Current Description:** Update icons to start_saving

**Discussion Points for Refinement:**
- **Icon Set/Library:** Material Design? FontAwesome? Custom design? (Define if using #38 brand guidelines)
- **Scope:** Which icons? All navigation icons? Action buttons? Hero illustrations?
- **Design Guidelines:** Reference design system or style guide?
- **Sizes & Formats:** What resolutions needed? SVG, PNG, or both? Accessibility (alt text)?
- **Implementation:** Replace existing or add new? Breaking change?
- **Timeline:** Does this need to be done before #38 (Brand guidelines)?
- **Action Item:** Wait for #38 brand guidelines clarification; define icon inventory

---

### #38 - Brand Guidelines  
**Status:** Open | **Assigned to:** Unassigned | **Comments:** 0

**Current Description:** Brand guidelines

**Discussion Points for Refinement:**
- **🔴 VERY VAGUE:** Needs immediate decomposition
- **Content Scope:** What should be included?
  - Color palette (primary, secondary, accent colors)?
  - Typography (font families, sizes, weights)?
  - Spacing & grid system?
  - Logo usage & variations?
  - Photography & imagery style?
  - Component library (buttons, cards, forms)?
  - Tone of voice & copy guidelines?
- **Coverage:** Web only? Mobile app too? Marketing materials?
- **Ownership & Maintenance:** Who maintains this? Version control strategy?
- **Design Tools:** Figma file? InVision? Notion? Adobe XD?
- **Rollout:** Is this blocking #36 (Home shortcut) and #37 (Icons)?
- **Action Item:** Create separate epic/stories for each brand guideline component; assign design lead

---

### #39 - Dashboard Savings Ticker  
**Status:** Open | **Assigned to:** Unassigned | **Comments:** 0

**Current Description:** Dashboard - todays savings ticker

**Discussion Points for Refinement:**
- **Data Source:** How is "today's savings" calculated? (Real-time transactions, end-of-day, scheduled jobs?)
- **Refresh Rate:** How often updates? (Real-time, every 5 mins, hourly?)
- **Display Format:** 
  - Show amount only? (e.g., "$45.23")
  - Percentage of goal?
  - Animated counter?
  - Breakdown by category?
- **Positioning:** Where on dashboard? (Hero section, sidebar, card widget?)
- **Mobile Responsiveness:** How does it display on small screens?
- **Edge Cases:** What if no savings today? Show "$0" or hide ticker?
- **Performance:** Any caching needed? Real-time updates performance impact?
- **Action Item:** Get wireframes/mockups from design; clarify calculation logic

---

### #40 - MySQL Upgrade Amazon RDS  
**Status:** Open | **Assigned to:** Unassigned | **Comments:** 0

**Current Description:** MySQL Upgrade Amazon RDS - ES-60

**Discussion Points for Refinement:**
- **🔴 INCOMPLETE SPEC:** Critical details missing
- **Version Target:** Current version → Target version? (5.7→8.0? 5.6→5.7?)
- **Compatibility:** Any breaking changes for application code?
- **Downtime Strategy:** Maintenance window acceptable? Blue-green deployment?
- **Backup & Rollback:** Full backup taken first? Rollback plan if issues?
- **Testing Environment:** Staging environment upgrade first? Regression testing needed?
- **Performance Impact:** Benchmarking plan before/after?
- **Dependencies:** Blocking any features? Related to #32 (Security review)?
- **Timeline:** When? Business hours or off-hours?
- **Action Item:** Get database team input; create detailed upgrade runbook

---

### #41 - Login & Registration Redesign  
**Status:** Open | **Assigned to:** Unassigned | **Comments:** 0

**Current Description:** Login and Registration redesign?

**Discussion Points for Refinement:**
- **🔴 UNCERTAIN:** Question mark suggests this item needs validation
- **Current Issues:** What pain points exist with current design? (User feedback? Analytics?)
- **Design Goals:** What does "redesign" mean? (Visual refresh? UX simplification? New flow?)
- **New Features:** Social login? Passwordless auth? MFA? (Ties to #32 Security)
- **Scope:** Login only? Registration only? Both? Password reset?
- **Mockups/Wireframes:** Do design mockups exist?
- **Mobile-First Approach:** Responsive design required?
- **Accessibility:** WCAG 2.1 AA compliance?
- **Dependencies:** Depends on #32 (Security review) for security requirements?
- **Action Item:** Validate business need; clarify scope; get design mockups

---

## 🔴 Critical Issues Requiring Immediate Attention

| Issue | Problem | Action Required |
|-------|---------|-----------------|
| #35 | Blocked - awaiting Steve discussion | Schedule meeting with Steve |
| #38 | Vague requirements - needs decomposition | Break into component-level stories |
| #40 | Incomplete specs - missing key details | Engage database team; create runbook |
| #41 | Uncertain scope - question mark in title | Validate business need; get design mockups |

## ✅ Issues Ready for Discussion

| Issue | Status | Next Step |
|-------|--------|-----------|
| #32 | Has 1 comment | Review comment for context |
| #34 | Has 1 comment | Review comment; finalize captcha vendor |

## 📋 Refinement Roadmap

### Phase 1: Immediate (This Week)
- [ ] Review comments on #32 and #34
- [ ] Schedule meeting with Steve for #35
- [ ] Validate #41 scope with product owner
- [ ] Get database team input on #40

### Phase 2: Decomposition (Next Week)
- [ ] Break down #38 into component stories
- [ ] Create detailed specs for #40 MySQL upgrade
- [ ] Get design mockups for #41
- [ ] Define icon inventory for #37

### Phase 3: Estimation (Week After)
- [ ] Estimate all refined items
- [ ] Prioritize by business value & dependencies
- [ ] Assign owners
- [ ] Create sprint plan

## Dependencies & Blockers
