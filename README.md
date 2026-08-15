# Pi-hole Policy Pipeline (DNS Filtering as Code)

> **Portfolio Progression Project**
>
> This repository documents an earlier stage of my DNS policy automation work, focused on version-controlled filtering rules and the design of a safe deployment pipeline.
>
> The concepts developed here later informed the broader DNS and infrastructure automation work documented in my current public portfolio:
> [Enterprise-Style Homelab Infrastructure](https://github.com/Shaw4552/homelab-public)

## Overview

This project documents the design of a version-controlled DNS policy system using Pi-hole, applying infrastructure-as-code principles to DNS filtering.

---

## Objectives

- Manage DNS allow/block lists via Git
- Track changes and maintain audit history
- Enable safe, repeatable updates
- Separate policy logic from runtime systems

---

## Approach

DNS policies are stored as:

- Allowlists
- Blocklists
- Group-specific rules

All updates are:

- Version controlled
- Documented
- Reviewed before deployment

---

## Planned Policy Structure

```text
lists/
├── apple-core.txt
├── microsoft-trusted.txt
├── cdn-default.txt
└── bitwarden-trusted.txt
---

## Design Principles

- Least privilege filtering
- Avoid breaking core services
- Separate policies by function/vendor
- Maintain human-readable rules

---

## CI/CD Direction at This Stage

Future pipeline will:

- Validate lists before deployment
- Push updates to Pi-hole instances
- Maintain consistency across nodes

---

## Lessons Learned

- Overblocking causes more issues than underblocking
- Vendor-specific allowlists are critical
- DNS filtering requires iterative tuning

---

## Improvements Identified at This Stage

- GitHub Actions integration
- Automated deployment to multiple DNS nodes
- Policy validation testing

---

## Sanitization Notice

No real domain logs, client identifiers, or sensitive DNS data are included.