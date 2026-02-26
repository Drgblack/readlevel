# ReadLevel – Product Roadmap & Strategic Concepts

## Purpose of this document

This document captures the strategic intent, product principles, and validated
feature concepts for ReadLevel.

It is **not** a task list or sprint backlog.
It exists to:
- preserve product thinking that should not be lost
- prevent reactive feature creep
- guide sequencing decisions
- provide clarity to future contributors (including future me)

ReadLevel is intentionally minimal. Anything added must earn its place.

---

## Core Product Principles (Non-Negotiable)

These principles override all feature ideas.

### 1. Guidance, not judgement  
ReadLevel provides decision support, not verdicts.
It explains *why* a text may be difficult and *what that means* — it does not shame,
score competitively, or imply failure.

### 2. Neutrality is the product  
ReadLevel does not rewrite content by default, upsell aggressively, or profit from
telling users their work is “wrong”. Trust and restraint are the differentiators.

### 3. Privacy first, always  
- Text is analysed client-side where possible
- No text content is stored
- Any analytics are aggregate, anonymised, and explicit
Trust is earned once and lost permanently.

### 4. Free core, paid workflows  
The free tool must remain genuinely useful.
Paid features extend ReadLevel into *professional workflows* that copy-paste
cannot support.

### 5. Individuals → Institutions  
ReadLevel earns trust with individuals first.
Institutional revenue comes later through audits, certification, and compliance
artefacts — not by locking core functionality.

---

## Product Scope (What ReadLevel Is)

ReadLevel is:
- A neutral readability analysis tool
- CEFR-aware and education-literate
- Calm, fast, and distraction-free
- Suitable for teachers, ESL educators, editors, accessibility reviewers, and
  public-sector content teams

ReadLevel is **not**:
- A writing assistant by default
- A content generator
- A gamified scoring system
- An ad-driven SEO farm

---

## Near-Term Infrastructure (Build First)

These are foundations that unlock multiple future products without committing
to them prematurely.

### Authentication
- Simple email/password accounts
- Required for subscriptions, saved insights, and institutional features
- No OAuth complexity initially

### Persistent Assessments
- Store assessment snapshots (not raw text)
- Enable immutable, dated records
- Foundation for audits, exports, and verification pages

### Public Assessment Pages
- Read-only snapshot pages at `/assessments/[id]`
- Show scope, date, methodology, and results
- No editing or regeneration
- Future verification anchor

### Exportable Assessment Summaries
- Neutral PDF titled “ReadLevel Readability Assessment Summary”
- Useful immediately for schools and organisations
- Basis for future certification artefacts

### Feature Flags
- `hasProAccess`
- `isFormalAssessment`
- Enables controlled rollout without refactoring

---

## Validated Feature Candidates (Individuals)

These ideas are promising but not yet commitments.

### Audience Match Score  
**Status:** Candidate (high confidence)

Instead of only returning a reading level, ReadLevel compares the text against a
declared audience and provides a plain-language verdict.

Example:
> “This text is C1. For B1 ESL learners, it may be too difficult for independent
> reading but suitable with teacher scaffolding.”

Why it fits:
- Decision support, not rewriting
- Extremely useful to teachers
- Makes the free tool feel intentionally incomplete

Monetisation:
- Free: level only
- Paid: audience match verdict + saved profiles

---

### Rewrite Assistant (Side-by-Side)  
**Status:** Candidate (medium confidence)

Generate a simplified version at a target level and display it alongside the
original — never replacing it, never automatic.

Why it fits:
- Visual, shareable, and word-of-mouth friendly
- Respects professional agency
- Clear paid upgrade

Risks:
- Must not drift into generic AI rewriting
- Requires careful tone and framing

---

## Institutional & B2B Concepts (Phase 2)

These features have higher revenue potential but require validation and sales effort.

### Content Audit Tool  
**Status:** Phase 2

Bulk analysis of URLs or document sets with a distribution view.

Target customers:
- Publishers
- Government communications teams
- EdTech platforms
- Accessibility consultants

Revenue:
- One-time or recurring audits
- API integrations for platforms

---

### Readability Certification  
**Status:** Phase 2 (Strategic)

Issue dated certificates and embeddable badges verifying that content meets a
defined readability standard.

Key idea:
ReadLevel becomes a *standard people cite*, not just a tool they use.

Why it fits:
- Neutrality = credibility
- Accessibility regulation tailwinds (EU / UK)
- Institutional budgets, not individual spend

Critical constraint:
Certification must be conservative, transparent, and defensible.
No automated pass/fail without human-interpretable criteria.

---

## Data & Analytics Philosophy

ReadLevel may collect:
- Aggregate usage patterns
- Result distributions
- Self-declared roles (e.g. teacher, editor)

ReadLevel will never:
- Store user text
- Sell data
- Profile individuals covertly

Analytics must benefit users directly via Insights pages, not just the product.

---

## Explicitly Deferred Ideas

These ideas are intentionally parked.

- Inline grammar correction
- Tone scoring
- Gamification / leaderboards
- Social sharing of scores
- AI “fix this text” buttons without context

Deferral is a decision, not neglect.

---

## Final Note

ReadLevel’s biggest risk is not technical difficulty.
It is *becoming noisy, cluttered, or extractive*.

Every feature must answer one question:
> Does this make ReadLevel more trustworthy?

If the answer is unclear, the feature waits.