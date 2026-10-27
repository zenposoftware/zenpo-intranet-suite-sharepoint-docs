# Zenpo Intranet Suite for SharePoint — Documentation & Trust Repository

**Last updated:** 2026-10-27

## Canonical Repository

This is the authoritative public repository for **Zenpo Intranet Suite for SharePoint**
documentation and the evidence used to review it.

Its permanent URL is:

[https://github.com/zenposoftware/zenpo-intranet-suite-sharepoint-docs](https://github.com/zenposoftware/zenpo-intranet-suite-sharepoint-docs)

Microsoft Marketplace submissions, security reviews and enterprise due diligence reference
this URL. It will never be renamed or repurposed.

---

## For Reviewers

If you're reviewing the suite, here's where to start:

| Question | Where to look |
|---|---|
| What data leaves our tenant, and what permissions does the suite need? | [SECURITY.md](SECURITY.md) |
| Can it run in GCC High, DoD, or a tenant that blocks outside calls? | [docs/enterprise-plan.md](docs/enterprise-plan.md) |
| What is in a release, and how do we check the package? | [releases/](releases/) and [SECURITY.md § Release evidence](SECURITY.md#release-evidence) |
| What changed in each release? | [CHANGELOG.md](CHANGELOG.md) |

---

## Purpose of This Repository

This repository is **documentation-only**. It gives customers and reviewers a place to find:

- Product documentation
- Security and data-handling disclosures
- Microsoft Marketplace review artifacts, such as “How to test”
- Release notes and versioned SBOMs
- A stable, auditable public record for enterprise and government reviews

**There is no proprietary source code here.** All product source code stays in private
repositories and controlled build pipelines.

---

## Design Principles

Here's how Zenpo publishes and maintains release and security evidence:

1. **Source code stays private.**

   This repository has no application source code, build scripts, credentials or runtime
   assets.

2. **Release evidence is public on purpose.**

   Release notes, SBOMs, security documentation and other verification artifacts give
   customers and reviewers a lasting record of each release.

3. **Published releases stay as published.**

   Release-specific documentation and artifacts are versioned and preserved. If something
   needs correcting or changing, it goes into a new revision or release. Prior evidence
   isn't silently replaced.

4. **Core documentation is maintained in one place.**

   Marketplace, compliance and submission-specific versions come from that canonical source.
   That reduces the chance of different versions saying different things.

5. **References should hold up over time.**

   Public documentation favors stable paths, explicit versions and static references over
   links that are dynamic or can change underneath a review.

6. **Public evidence describes what was released, verified or supported.**

   Internal documentation covers how those artifacts are produced, tested and maintained.

7. **Automation follows the established structure.**

   Automation can generate, validate or transform artifacts. It still has to follow approved
   conventions; it can't introduce new structures or publication rules on its own.

---

## Repository Structure

```text
zenpo-intranet-suite-sharepoint-docs/
├─ README.md
├─ CHANGELOG.md
├─ SECURITY.md            # Security and data handling
├─ docs/
│  └─ enterprise-plan.md  # Enterprise plan, offline entitlement, government clouds
├─ images/                # Diagrams used by the documentation
└─ releases/              # Release notes, SBOMs, and build metadata (per version)
```

---

## Vendor

**Zenpo Software Innovations, LLC** publishes and maintains the **Zenpo Intranet Suite for
SharePoint**.

Official website: [https://zenpo.com](https://zenpo.com)

Product website: [https://intranet.zenpo.com](https://intranet.zenpo.com)

Help website: [https://help.zenpo.com](https://help.zenpo.com)

---

## Microsoft Marketplace Listing

Zenpo Intranet Suite for SharePoint is distributed through Microsoft Marketplace.

**Permanent Microsoft Marketplace URL:**

[https://marketplace.microsoft.com/en-us/product/WA200012546](https://marketplace.microsoft.com/en-us/product/WA200012546)

The Microsoft Marketplace submission and review materials will link directly to this
repository.

---

## Change History

[CHANGELOG.md](CHANGELOG.md) keeps the complete record of public-facing documentation and
release evidence.
