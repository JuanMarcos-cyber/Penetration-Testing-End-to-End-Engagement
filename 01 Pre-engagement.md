# 01 – Pre-Engagement
====================

## Purpose

The purpose of this phase is to formally define the scope, authorization,
constraints, and preparation required before initiating any penetration
testing activities.

A well-executed pre-engagement phase ensures that testing is **authorized,
controlled, ethical, and reproducible**, and prevents scope creep or accidental
impact on unintended systems.

---

## Engagement Overview

- **Organization:** Internal Training Lab  
- **Assessment Type:** Web Application Penetration Test  
- **Target Application:** DVWA (Damn Vulnerable Web Application)  
- **Target URL:** http://localhost:4280  
- **Environment:** Localhost / Docker-based Linux container  
- **Tester:** Juan Marcos Lázaro Rey  
- **Engagement Date:** December 11th, 2025  
- **Engagement Duration:** 1 hour (active testing window)

This assessment was conducted exclusively for **educational and training
purposes** in a controlled lab environment.

---

## Scope Definition

### In-Scope Assets

The following assets were explicitly authorized for testing:

- DVWA web application running on `127.0.0.1:4280`
- Application-layer vulnerabilities only
- Web interfaces and application logic
- Authentication and session management mechanisms

---

### Out-of-Scope Assets

The following systems and activities were explicitly excluded from testing:

- Host operating system
- Docker host and container escape attempts
- Network infrastructure
- Physical security
- Social engineering
- Denial-of-service (DoS) attacks
- Privilege escalation beyond application scope

Testing outside this scope was **strictly prohibited**.

---

## Rules of Engagement (RoE)

### Authorization

- Testing was pre-authorized by the lab environment owner.
- Legal framework: **Educational use only**
- No real or sensitive data was involved.
- All actions were confined to intentionally vulnerable systems.

---

### Permitted Activities

- Web application vulnerability scanning
- Manual penetration testing
- SQL injection testing
- Cross-site scripting (XSS) proof-of-concepts
- Authentication and session management testing
- File upload and file inclusion testing

---

### Prohibited Activities

- Host system exploitation
- Docker container escape attempts
- Network-level attacks
- High-volume automated scanning
- Data destruction or modification
- Service disruption

Any deviation required **explicit instructor approval**.

---

## Testing Methodology

The engagement followed an industry-aligned methodology, including:

- OWASP Testing Guide v4.0
- Manual validation of identified vulnerabilities
- Controlled exploitation with proof-of-concept only
- Evidence-based documentation

Testing was intentionally **manual-first** to reflect realistic attacker
behavior rather than automated exploitation.

---

## Communication and Escalation

- **Primary Contact:** Lab Instructor  
- **Reporting Schedule:** Upon completion of testing  
- **Critical Findings:** Immediate notification and testing halt  
- **Unexpected Behavior:** Stop testing and consult instructor  

### Emergency Stop Procedure

```bash
docker compose down
```

![Docker environment initialized using docker compose up](screenshots/Screenshot%20Docker%20compose%20up.png)
