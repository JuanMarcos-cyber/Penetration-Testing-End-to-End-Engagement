# 01 – Pre-Engagement & Technical Readiness

## Objective

This phase establishes authorization, scope definition, technical readiness, and safety controls prior to initiating any active penetration testing activities. All conditions described in this document were verified before exploitation began.

---

## Technical Readiness Checklist

### Environment Validation

- DVWA application reachable on port 4280
- Database initialized successfully
- Security level configured to **Low**
- Valid application credentials confirmed

### Tooling Readiness

- Firefox browser available
- Docker service running
- Terminal access confirmed
- curl available for HTTP inspection

---

## Evidence and Reporting Preparation

To ensure consistent documentation and full traceability throughout the engagement, a standardized evidence and reporting structure was defined before exploitation activities commenced.

---

## Reporting Structure

```text
reports/
├── executive-summary.md
├── findings/
├── remediation-plan.md
├── lessons-learned.md
└── screenshots/
```

## Component Purpose

### executive-summary.md

Provides a high-level overview of the engagement for non-technical stakeholders, focusing on business impact, overall risk posture, and key recommendations.

### findings/

Contains detailed vulnerability write-ups, including technical descriptions, exploitation steps, screenshots, and impact analysis.

### remediation-plan.md

Defines a prioritized remediation roadmap with recommended corrective actions and security best practices.

### lessons-learned.md

Documents post-engagement reflections, defensive insights, and improvement opportunities identified during testing.

### screenshots/

Stores visual evidence captured during exploitation, referenced directly from the corresponding findings.

---

## Benefits of This Structure

- Clear separation between executive and technical documentation
- Evidence captured during exploitation rather than retroactively
- Direct traceability from vulnerability discovery to remediation
- Professional reporting format aligned with real-world penetration testing deliverables

---

## Risk Management and Safety Controls

To prevent unintended impact during testing, the following safeguards were defined and enforced throughout the engagement:

- Emergency stop procedures established
- No destructive payloads permitted
- Request rates intentionally kept low
- Testing confined strictly to the DVWA environment
- Instructor designated as escalation contact

---

## Engagement Authorization

All pre-engagement conditions were reviewed and approved prior to initiating testing activities.

### Tester

- Juan Marcos Lázaro Rey

### Environment

- Authorized internal training lab
- Educational and non-production use only

### Authorization Status

- Approved to proceed to Information Gathering and Reconnaissance

---

## Next Phase

### 02 – Information Gathering and Reconnaissance

The next phase focuses on:

- Application mapping
- Endpoint discovery
- Header and technology analysis
- Passive and active reconnaissance
