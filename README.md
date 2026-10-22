# External QA Defect Report: Bank Career Portal

Independent exploratory QA review of the public registration page of a Turkish
participation bank's career portal. The review found privacy-notice and
localization defects in the production environment. I documented them in a
structured defect report, submitted it through the bank's official customer
channel, and retested the page two weeks later.

> The bank's name, URL and logo are redacted because some of the reported
> defects were still open at the time of the last retest.

## Scope

| | |
|---|---|
| Environment | Production, public career portal (no login required) |
| Page | New user registration |
| Platform | Desktop, Windows 11, Brave 1.97 |
| Languages | Turkish (TR), English (EN) |
| Approach | Exploratory testing as a regular applicant; no logs, network traces or backend access |

## Findings

| ID | Component | Turkish (TR) | English (EN) |
|---|---|---|---|
| EXT-001 | Privacy Notice dialog | Displayed only "test" | Empty |
| EXT-001 | Explicit Consent dialog | Displayed only "deneme" | Empty |
| EXT-001 | Consent checkbox labels | - | Remained in Turkish while other labels were in English |

**Suggested severity / priority:** Major (S2) / High (P1). Applicants could not
review privacy information before giving their declarations in a public
production registration flow.

## Report

The full report ([report.pdf](report.pdf)) contains:

- Environment and reproduction steps
- Expected vs. actual results
- Impact assessment and suggested severity / priority
- Screenshot evidence (Appendix A)

## Timeline

| Date | Event |
|---|---|
| 8 Oct 2026 | Defects observed and documented |
| 9 Oct 2026 | Report submitted through the bank's official customer channel; acknowledged |
| 22 Oct 2026 | Retest: TR dialogs display full content; EN dialogs still empty; EN consent labels still in Turkish |

## Skills demonstrated

Exploratory testing · Localization testing · Defect reporting ·
Severity and priority assessment · Retesting · Responsible disclosure
