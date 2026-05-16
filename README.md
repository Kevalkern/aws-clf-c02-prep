# AWS CLF-C02 Prep

Study materials for the AWS Certified Cloud Practitioner exam (`CLF-C02`).

As of `2026-05-16`, the official AWS exam guide lists:

- `50` scored questions
- `15` unscored questions
- passing score: `700 / 1000`
- content domains:
  - `Cloud Concepts` - `24%`
  - `Security and Compliance` - `30%`
  - `Cloud Technology and Services` - `34%`
  - `Billing, Pricing, and Support` - `12%`

Official references:

- AWS exam guide: `https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html`
- In-scope services: `https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html`

## Start Here

If you want the shortest useful path through this repo:

1. Read `docs/high-yield-checklist.md`
2. Read `docs/study-guide.md`
3. Drill `docs/flashcards.md`
4. Take `docs/mock-exam-50.md`
5. Review mistakes with `docs/practice-review-template.md`

## Study Pack

- `docs/study-guide.md` - primary CLF-C02 study guide
- `docs/example-questions.md` - practice questions with explanations
- `docs/mock-exam-50.md` - full 50-question mock exam
- `docs/flashcards.md` - active-recall flashcards
- `docs/glossary.md` - fast review glossary
- `docs/4-week-study-plan.md` - daily study schedule
- `docs/high-yield-checklist.md` - exam-focused checklist
- `docs/service-map.md` - must-know services grouped by category
- `docs/practice-review-template.md` - review sheet for mock exams

## Suggested Flow

1. Read `docs/high-yield-checklist.md` first.
2. Use `docs/study-guide.md` to cover the four exam domains.
3. Use `docs/service-map.md` to drill service recognition.
4. Work through `docs/example-questions.md`.
5. Run `docs/flashcards.md` for active recall.
6. Take `docs/mock-exam-50.md` under timed conditions.
7. After each practice set, fill `docs/practice-review-template.md`.
8. Follow `docs/4-week-study-plan.md` if you want a structured month-long schedule.

## Exam Strategy

- Prioritize service recognition over deep implementation.
- Know when to choose a service, not how to build it.
- Be strong on shared responsibility, IAM, pricing models, support plans, and core services.
- Expect distractors that are real AWS services but not the best fit.
- Use elimination aggressively on multi-response questions.

## High-Probability Topics

- AWS global infrastructure: Regions, Availability Zones, edge locations
- Shared responsibility model
- IAM, MFA, least privilege, root user safety
- S3, EC2, Lambda, RDS, DynamoDB, VPC, CloudFront, Route 53
- CloudWatch vs CloudTrail vs Config
- Organizations, Control Tower, Trusted Advisor, Budgets, Cost Explorer
- Support plans and pricing models
- Well-Architected Framework pillars

## Repo Goal

This repo is optimized for passing `CLF-C02`, not for deep architecture training. The material is intentionally biased toward:

- service selection
- common AWS comparisons
- security and billing fundamentals
- exam-style wording traps

## Notes

- This repo is a study aid, not an official AWS source.
- If AWS updates the blueprint, revise this repo against the official exam guide before exam day.
