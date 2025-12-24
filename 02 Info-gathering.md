## Discovered Services

The following network services were identified on the target host:

- **22/tcp** — SSH
- **3389/tcp** — RDP / xRDP
- **4280/tcp** — DVWA web application

Port **4280** is bound exclusively to `127.0.0.1`, confirming that DVWA is not
externally accessible.

---

## Docker Network Enumeration

### Docker Bridge Network

The DVWA environment uses a dedicated Docker bridge network:

- **Bridge name:** `br-8925aeef9fd1`
- **Bridge IP range:** `172.18.0.1/16`

### Container IP Allocation

- **DVWA container:** `172.18.0.3`
- **MariaDB container:** `172.18.0.2`

The database container is **not exposed externally** and is only reachable
from within the Docker bridge network.

This architecture enforces isolation between the database and the host system.

---

## Service Fingerprinting

### Web Service Identification

```bash
nmap -sV -p 4280 localhost
```

## Identified Technology Stack

- **Web Server:** Apache 2.4.65 (Debian)
- **Backend Language:** PHP 8.5.0

The service stack is disclosed via banner grabbing and HTTP response headers.

---

## DNS Enumeration

DNS-based reconnaissance was performed against a simulated internal domain.

- **Domain tested:** `dvwa.local`
- **Result:** `NXDOMAIN`

DVWA does not rely on DNS resolution and is accessed directly via `localhost`,
which is typical for Docker-based laboratory environments.

---

## Directory & File Enumeration

### Automated Directory Discovery

```bash
dirb http://localhost:4280
```

### Discovered Directories

- `/config/` — 403 Forbidden
- `/database/` — 403 Forbidden
- `/docs/` — 403 Forbidden
- `/external/` — 403 Forbidden
- `/tests/` — 403 Forbidden

### Discovered Files

- `php.ini`
- `phpinfo.php`
- `robots.txt`
- `index.php`
- `favicon.ico`

Although access is restricted, the presence of configuration-related files
represents a significant information disclosure risk in real-world environments.

---

### Extension-Based Enumeration

```bash
dirb http://localhost:4280 -X .php,.txt,.bak,.old
```

### Key Application Files

- `setup.php`
- `login.php`
- `security.php`
- `instructions.php`
- `about.php`
- `security.txt`

No backup or legacy files were discovered.

---

## OSINT Reconnaissance

Although the target is not publicly exposed, OSINT-style techniques were applied
to simulate real-world reconnaissance activities.

### HTML Content Analysis

No email addresses, usernames, developer comments, or metadata were found
within the HTML source of the landing page.

---

### HTTP Header OSINT

```bash
curl -I http://localhost:4280
```

### Observed Disclosures

- Apache version
- PHP version
- Debian-based operating system
- Authentication entry point (`login.php`)
- Session cookies (`PHPSESSID`, `security`)

These headers provide valuable fingerprinting data for attackers.

---

## Reconnaissance Summary

Key findings from this phase include:

- DVWA is isolated to localhost via Docker port binding
- The database is not externally exposed
- The application stack is clearly disclosed (Apache, PHP, Debian)
- Directory and file enumeration reveals sensitive paths
- No user or organizational OSINT is exposed
- Network topology is simple but clearly segmented

The gathered information provides a complete view of the attack surface
without performing any exploitation.

---

## Transition to Next Phase

➡️ **03 – Threat Modeling**

The next phase focuses on:

- Trust boundary identification
- Attack path mapping
- Impact-driven prioritization


