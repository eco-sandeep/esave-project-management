# Project Status Report - EcoCentre-Org/esave

**Repository:** EcoCentre-Org/esave  
**Report Date:** 2026-03-30  
**Language Composition:** Python (55.4%), HTML (43.6%), Other (1%)  
**Reported By:** eco-arpita

---

## 📋 IN PROGRESS (5 items)

| # | Issue | Assignee | Status | Created | Last Updated |
|---|-------|----------|--------|---------|--------------|
| 33 | [DevTracker] REQ-9450f12c - Add password requirement text | BT-EcoCentre | In Progress | 10 days ago | 6 days ago |
| 31 | [DevTracker] REQ-c65d9cab - Document CI/CD pipeline | BT-EcoCentre | In Progress | 10 days ago | 2 days ago |
| 21 | [DevTracker] REQ-d4338848 - Savings screen Redesign - card listing screen | *Unassigned* | In Progress | 12 days ago | 5 days ago |
| 29 | [DevTracker] REQ-de959269 - Add Email Opt-In checkbox on Update profile page | ConorEco | In Progress | 11 days ago | 6 days ago |
| 12 | [DevTracker] REQ-4ac75f6a - Email verification | sudheereco | In Progress | 14 days ago | 1 day ago |

### Details

**#33 – Add password requirement text**
- Add password validation requirements (8+ chars, 1 number, 1 special char) to signup page
- Real-time password validation as user types
- URL: https://stage.esave.org.uk/signup/

**#31 – Document CI/CD pipeline**
- Document deployment workflows for team onboarding
- Cover: local → stage → production environments
- Reference: Django + GitHub + Heroku stack

**#21 – Savings screen Redesign - card listing screen**
- Redesign savings card component with updated visual styling
- Apply across all product listing pages
- Figma reference available
- ⚠️ **UNASSIGNED** – Needs owner

**#29 – Add Email Opt-In checkbox on Update profile page**
- Add email opt-in checkbox above 'Update Profile' button
- Persist user preference to database
- URL: https://stage.esave.org.uk/update-profile/

**#12 – Email verification**
- Implement mandatory email verification for new user accounts
- 72-hour expiry links with unique activation tokens
- Block login until account activated

---

## ✅ READY FOR TEST (3 items)

| # | Issue | Assignee | Status | Created | Last Updated |
|---|-------|----------|--------|---------|--------------|
| 27 | GA4 configuration details | eco-sandeep | ✅ Completed | 11 days ago | 11 days ago |
| 12 | [DevTracker] REQ-4ac75f6a - Email verification | sudheereco | Ready for Test | 14 days ago | 1 day ago |
| 28 | [DevTracker] REQ-768ccb6d - Change font color on Update profile page | ConorEco | Ready for Test | 11 days ago | 6 days ago |

### Details

**#27 – GA4 configuration details** ✅ **CLOSED**
- Google Analytics 4 tracking code successfully added
- Label: "Ready for Code Review"
- Closed: 11 days ago

**#12 – Email verification** (Ready for Test)
- Email verification functionality deployed to staging
- Test account activation flow and link expiry handling

**#28 – Change font color on Update profile page** (Ready for Test)
- Fix: white text → black text on form fields
- Affects: Energy efficiency, Building type, and other fields
- URL: https://stage.esave.org.uk/update-profile/

---

## 📊 SUMMARY

| Metric | Count |
|--------|-------|
| **Total Items** | 8 |
| **In Progress** | 5 |
| **Ready for Test** | 2 |
| **Completed** | 1 |
| **Unassigned** | 1 |

---

## 🎯 NEXT STEPS

1. **Assign #21** – Savings screen redesign needs developer assignment
2. **Prioritize #31** – CI/CD documentation is critical for team onboarding
3. **Begin QA** – Start testing phase for #12 and #28 on staging environment
4. **Monitor #12** – Email verification was updated 1 day ago; ensure latest changes are in staging

---

## 📌 REPOSITORY INFO

- **Repo ID:** 999722687
- **Owner:** EcoCentre-Org
- **Primary Languages:** Python (55.4%), HTML (43.6%)
- **Staging URL:** https://stage.esave.org.uk
