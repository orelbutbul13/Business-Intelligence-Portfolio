# Insurance Quote Funnel BI Analysis

Business Intelligence project analyzing a 15,000-row anonymized commercial insurance quote funnel to identify where funnel volume is actually being lost, which losses are fixable, and which surface-level completion and rejection metrics are misleading once the correct denominator is applied.

---

## Project Documentation

- [View Full Report and Analysis](https://docs.google.com/document/d/1stFMDTX9L2pk34scuOuEXp5oqLBMd8OQFN9OlhF5-2A/edit)

---

## Business Objective

Insurance MGA and broker leadership require structured visibility into where a digital quoting funnel is losing volume, and which parts of that loss are attributable to underwriting appetite, data/pipeline gaps, or funnel UX.

This project transforms a raw funnel export into actionable business intelligence supporting:

- Denominator-aware conversion and rejection rate reporting
- Silent-failure identification (funnel-complete rows with no priced or rejected outcome)
- Acquisition channel quality comparison (conversion rate vs. underwriting fit)
- Structured extraction and validation of a semi-structured underwriting rejection log
- Premium concentration and pricing-driver analysis by industry category and business size
- Repeat-applicant and data-quality segmentation

The objective was to convert a raw 15,000-row funnel export into 90 structured, denominator-explicit business answers, each paired with a named, owned recommendation.

---

## Dataset Overview

The analysis is based on an anonymized commercial insurance quote-funnel export, including:

- Funnel stage, completion status, and incomplete-stage detail
- Acquisition source and device type
- Industry classification and business-size (annual revenue) band
- 9 premium components and total premium
- A semi-structured underwriting rejection log
- A verified business-location identifier (used as a pricing-eligibility gate)

The rejection log required custom regex extraction across 8 reason-type keys before it could be analyzed as structured data.

---

## Analytical Focus Areas

- True funnel completion rate vs. raw stage-reached completion rate
- Underwriting rejection rate by decision-population and by all-applications denominator
- Acquisition channel conversion and rejection-rate comparison
- Premium concentration by industry category and correlation with business-size band
- Category-level rejection-rate reliability (sample-size-aware)
- Repeat-applicant resolution behavior
- Data-entry normalization gaps in free-text segmentation fields

---

## Tools and Techniques

- SQL-style aggregation (SUMIFS/COUNTIFS-equivalent logic)
- Google Sheets formula-driven analysis, including REGEXEXTRACT-based structured log parsing
- Cross-field data-quality validation and reconciliation
- Denominator auditing and KPI design
- Funnel and cohort-style segmentation analysis

---

## Key Findings

- True funnel completion is 30.3%, not the 66.6% a raw stage-reached flag suggests; the gap is a "ghost complete" bucket worth an estimated $13.9M in recoverable premium.
- Rejection rate is 54.2% of quotes that reached a real final outcome (rejected or priced), but only 16.4% of all applications, since most never reach a decision at all.
- One acquisition channel converts at ~70.9% (nearly double the ~38% average of other channels) while also carrying the lowest rejection rate, a rare channel that wins on both axes.
- A missing verified business-location identifier is a hard pricing gate: applicants still complete the funnel 94.9% of the time but are priced 0% of the time without it.
- A single over-broad eligibility rule (not a genuine risk rule) accounts for an estimated $2.65M in recoverable rejected premium.
- Repeat applicants (250 businesses, 2-4 applications each) reach a real outcome 100% of the time, a validated warm-lead segment hiding in what looks like duplicate traffic.
- Revenue concentration is a category story, not an account story: it takes 66.1% of all priced quotes to reach 80% of total premium, so the real diversification risk sits in category mix, not a handful of large accounts.
- 72.6% of priced quotes carry a $0 flood premium, and content premium outweighs building premium roughly 116 to 1, pointing to a flood-coverage cross-sell gap and a renter-dominant customer base.
- Completion rate is flat across device type (desktop 30.5%, mobile 30.1%, tablet 30.1%), ruling out a device/UX theory, while applications flagged as duplicate submissions resolve at only 15.6%, roughly half the rate of any other segment.

---
