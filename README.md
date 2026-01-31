# Zenpo Intranet Suite for SharePoint — Documentation & Trust Repository

## Canonical Repository

This repository is the **authoritative public documentation and trust surface** for:

**Zenpo Intranet Suite for SharePoint**

Permanent canonical URL (never renamed or repurposed):

[https://github.com/zenposoftware/zenpo-intranet-suite-sharepoint-docs](https://github.com/zenposoftware/zenpo-intranet-suite-sharepoint-docs)

This URL is referenced by AppSource submissions, security reviews, and enterprise due-diligence processes.

---

## Purpose of This Repository

This repository is **documentation-only**.

It exists to provide:

* Product documentation
* Security and data-handling disclosures
* AppSource review artifacts (for example, “How to test”)
* Release notes and versioned SBOMs
* A stable, auditable public record for enterprise and government reviewers

**No proprietary source code is stored here.**
All product source code lives in private repositories and controlled build pipelines.

---

## Design Principles

These principles apply to **all humans, scripts, and automation** interacting with this repository.

1. **Code stays private**
   This repository never contains application source code, build scripts, or runtime assets.

2. **Evidence is public**
   Release notes, SBOMs, and security posture documentation are published intentionally.

3. **Immutability per release**
   Documentation and artifacts are versioned and never modified after release.

4. **Canonical vs. rendered documentation**
   Canonical documentation is authored once. Submission-specific variants (for example, AppSource uploads) are derived from it.

5. **Boring beats clever**
   No dynamic links, no mutable references, no marketing language.

6. **Public is declarative, private is operational**
   Public files describe what exists. Private documentation describes how it is produced.

7. **Automation must follow structure, not invent it**
   Automation may scaffold or transform files, but must never introduce new conventions without explicit approval.

---

## Repository Structure

```text
zenpo-intranet-suite-sharepoint-docs/
├─ README.md
├─ CHANGELOG.md
├─ SECURITY.md
├─ SUPPORT.md
├─ LICENSE
│
├─ docs/                  # Canonical documentation (relative links)
├─ appsource/             # AppSource submission artifacts (absolute, version-pinned links)
├─ releases/              # Release notes, SBOMs, and build metadata (per version)
├─ images/                # Versioned images referenced by documentation
└─ tools/                 # Automation helpers (no code execution)
```

---

## Vendor

**Zenpo Software Innovations, LLC**
Official website: [https://zenpo.com](https://zenpo.com)

Zenpo is the publisher and maintainer of the **Zenpo Intranet Suite for SharePoint**.

---

## Microsoft AppSource Listing

The Zenpo Intranet Suite for SharePoint is distributed via Microsoft AppSource.

**AppSource listing:**
*To be published.*

This repository will be referenced directly from the AppSource submission and review materials.

---

## Changelog

All notable changes to the Zenpo Intranet Suite for SharePoint documentation are recorded here by product release.

This changelog reflects **documentation and trust artifacts**, not internal development activity.

---

### Unreleased

* Initial documentation scaffold

---

### v1.0.0

* Initial public release documentation
* Security and data-handling disclosures
* AppSource review artifacts
* SBOM publication
