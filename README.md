# Pi-hole Policy Pipeline (DNS Filtering as Code)

## Overview

This project implements a version-controlled DNS policy system using Pi-hole, designed to simulate infrastructure-as-code principles for DNS filtering.

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

## Structure

text lists/   apple-core.txt   microsoft-trusted.txt   cdn-default.txt   bitwarden-trusted.txt 

---

## Design Principles

- Least privilege filtering
- Avoid breaking core services
- Separate policies by function/vendor
- Maintain human-readable rules

---

## CI/CD Direction

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

## Future Improvements

- GitHub Actions integration
- Automated deployment to multiple DNS nodes
- Policy validation testing

---

## Sanitization Notice

No real domain logs, client identifiers, or sensitive DNS data are included.