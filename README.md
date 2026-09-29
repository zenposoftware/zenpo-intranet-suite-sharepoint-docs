# Zenpo Intranet Suite for SharePoint — Documentation & Trust Repository

## Canonical Repository

This repository is the **authoritative public documentation and trust surface** for:

**Zenpo Intranet Suite for SharePoint**

Permanent canonical URL (never renamed or repurposed):

[https://github.com/zenposoftware/zenpo-intranet-suite-sharepoint-docs](https://github.com/zenposoftware/zenpo-intranet-suite-sharepoint-docs)

This URL is referenced by Microsoft Marketplace submissions, security reviews, and enterprise due-diligence processes.

---

## Purpose of This Repository

This repository is **documentation-only**.

It exists to provide:

* Product documentation
* Security and data-handling disclosures
* Microsoft Marketplace review artifacts (for example, “How to test”)
* Release notes and versioned SBOMs
* A stable, auditable public record for enterprise and government reviewers

**No proprietary source code is stored here.**
All product source code lives in private repositories and controlled build pipelines.

---

## Design Principles

These principles govern how Zenpo publishes and maintains release and security evidence.

1. **Source code remains private**  
   This repository contains no application source code, build scripts, credentials, or runtime assets.

2. **Release evidence is intentionally public**  
   Release notes, SBOMs, security documentation, and other verification artifacts are published to provide customers and reviewers with durable evidence of each release.

3. **Published releases are immutable**  
   Release-specific documentation and artifacts are versioned and preserved as published. Corrections or changes are issued through a new revision or release rather than silently replacing prior evidence.

4. **Documentation has one canonical source**  
   Core documentation is maintained once. Marketplace, compliance, or submission-specific versions are derived from that canonical source to reduce inconsistency.

5. **References should remain durable and predictable**  
   Public documentation favors stable paths, explicit versions, and static references over dynamic or mutable links.

6. **Public evidence is declarative; internal processes remain operational**  
   Public materials describe what was released, verified, or supported. Internal documentation defines how those artifacts are produced, tested, and maintained.

7. **Automation preserves established structure**  
   Automation may generate, validate, or transform artifacts, but it must follow approved conventions rather than introducing new structures or publication rules independently.

---

## Repository Structure

```text
zenpo-intranet-suite-sharepoint-docs/
├─ README.md
├─ CHANGELOG.md
└─ releases/              # Release notes, SBOMs, and build metadata (per version)
```

---

## Vendor

**Zenpo Software Innovations, LLC**
Official website: [https://zenpo.com](https://zenpo.com)

Product website: [https://intranet.zenpo.com](https://intranet.zenpo.com)

Help website: [https://help.zenpo.com](https://help.zenpo.com)

Zenpo is the publisher and maintainer of the **Zenpo Intranet Suite for SharePoint**.

---

## Microsoft Marketplace Listing

The Zenpo Intranet Suite for SharePoint is distributed via Microsoft Marketplace.

**Microsoft Marketplace listing:**
*To be published.*

This repository will be referenced directly from the Microsoft Marketplace submission and review materials.

---

## Change History

A complete record of public-facing documentation and release evidence
is maintained in the changelog.

See: [CHANGELOG.md](CHANGELOG.md)
