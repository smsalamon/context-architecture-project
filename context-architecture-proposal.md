# SSA Context Architecture: Summary

## 1. Concept categories

1. **Program overview**: what a benefit or program is and who it is for.
2. **Eligibility**: who qualifies (credits, disability definition, spouse/survivor/child criteria, continuing eligibility).
3. **Procedure**: step-by-step "how to do X".
4. **Required documents**: per-scenario document lists (mainly card pages, plus application evidence).
5. **Benefit amount rules**: reduction/increase percentages, FRA by birth year, delayed credits, family maximum, spouse share, GPO/WEP, premium tiers.
6. **Decision guidance**: trade-offs for timing and choices (when to claim, working while receiving, Medicare now vs. later).
7. **Medicare interplay**: how Social Security and Medicare affect each other (enrolment timing, Part B, SEPs, IRMAA, Medicare cards).
8. **Fraud and phishing protection**: recognising and reporting phishing, security freezes, extra account security.
9. **Tools and calculators**: what a tool does, who can use it, required inputs.

Dropped as boilerplate: navigation menus, "Related Information"/"Publications" lists, "Still have questions?"/contact blocks, session-timeout notices, web UI prompts, repeated card-page rule block.

## 2. Facets

| Facet | Values | Applies to |
|---|---|---|
| Program | retirement, disability, survivors, SSI, Medicare, card, general | all files |
| Age group | adult, child | card pages and age-dependent content; optional elsewhere |
| Citizenship/birth status | U.S.-born, foreign-born citizen, noncitizen | card pages and status-dependent content; optional elsewhere |
| Relationship | worker, spouse, divorced spouse, survivor, child, parent | family and survivor content; optional elsewhere |
| Procedure type | apply, update card/record details, replace card, request document, set up access, appeal, report change in status | Procedure only |
| Eligibility stage | qualifying, approved, continuing | Eligibility only |

## 3. Finalized folder structure after the split

```
Slice/
├── 01-program-overview/
│   └── ssi-program.md
├── 02-eligibility/
│   ├── social-security-credits.md
│   └── continuing-disability.md
├── 03-procedure/
│   ├── apply-ssi.md
│   ├── request-benefit-verification-letter.md
│   └── sign-in-identity-verification.md
├── 04-required-documents/
│   └── original-card-us-born-adult.md
├── 05-benefit-amount-rules/
│   ├── early-retirement-reduction.md
│   ├── delayed-retirement-credits.md
│   └── government-pension-offset.md
├── 06-decision-guidance/
│   └── when-to-start-retirement.md
├── 07-medicare-interplay/
│   └── medicare-only-and-part-b-enrollment.md
├── 08-fraud-protection/
│   └── detecting-phishing-emails.md
└── 09-tools-and-calculators/
    ├── retirement-estimator.md
    └── gpo-calculator.md
```

## 4. Sample frontmatter (one file per concept type)

**Program overview** (`overview-ssi-program.md`)
```yaml
---
title: SSI program overview
concept_type: Program overview
program: SSI
---
```

**Eligibility** (`eligibility-social-security-credits.md`)
```yaml
---
title: Social Security credits and benefit eligibility
concept_type: Eligibility
eligibility_stage: qualifying
program: retirement, disability, survivors
relationship: worker, survivor
---
```

**Procedure** (`procedure-apply-ssi.md`)
```yaml
---
title: How to apply for SSI
concept_type: Procedure
procedure_type: apply
program: SSI
age_group: adult, child
---
```

**Required documents** (`documents-original-card-us-born-adult.md`)
```yaml
---
title: Documents for an original card, U.S.-born adult
concept_type: Required documents
program: card
age_group: adult
citizenship_status: U.S.-born
---
```

**Benefit amount rules** (`benefit-rules-early-retirement-reduction.md`)
```yaml
---
title: Full retirement age and early retirement reduction
concept_type: Benefit amount rules
program: retirement
relationship: worker
---
```

**Decision guidance** (`decision-guidance-when-to-start-retirement.md`)
```yaml
---
title: When to start retirement benefits
concept_type: Decision guidance
program: retirement
relationship: worker, spouse
---
```

**Medicare interplay** (`medicare-only-and-part-b-enrollment.md`)
```yaml
---
title: Applying for Medicare only and Part B enrollment
concept_type: Medicare interplay
program: Medicare, retirement
relationship: worker
---
```

**Fraud and phishing protection** (`fraud-detecting-phishing-emails.md`)
```yaml
---
title: Detecting phishing emails pretending to be Social Security
concept_type: Fraud and phishing protection
program: general
---
```

**Tools and calculators** (`tools-retirement-estimator.md`)
```yaml
---
title: Retirement Estimator
concept_type: Tools and calculators
program: retirement
relationship: worker
---
```
