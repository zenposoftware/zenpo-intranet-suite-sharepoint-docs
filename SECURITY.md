# Security and Data Handling

**Product:** Zenpo Intranet Suite for SharePoint
**Applies to:** v1.0.1.0, the current release
**Last reviewed:** 2026-10-27

This page is for security, network and procurement reviewers. It says what the web parts
do in your tenant, what leaves it, and what Zenpo keeps.

---

## Summary

- The suite is 18 SharePoint Framework (SPFx) web parts. They run in the browser, on
  SharePoint Online modern pages.
- Every SharePoint request runs as the signed-in user, under that person's own permissions.
  Nothing elevates access.
- The package requests no API permissions: no Microsoft Graph, no admin consent, no
  app-only access.
- Your content stays in your SharePoint. Zenpo has no copy of your lists, libraries or pages.
- Zenpo does not track what people do: no clicks, no searches, no record of who viewed which
  page.
- The web parts call Zenpo for two things only: license calls, and the buy page when an editor
  clicks a subscription button. Neither includes your content.
- On the Enterprise plan with offline entitlement, the web parts make no calls to Zenpo at
  all. See [Enterprise Plan](docs/enterprise-plan.md).

---

## What the suite does not need

- **No Zenpo account or login.** People sign in to Microsoft 365 as usual. Nobody creates a
  Zenpo account to use the web parts.
- **No Zenpo server for your content.** No Zenpo backend reads, stores or serves your
  content.
- **No custom database.** Your content lives in your SharePoint lists, libraries and pages.
- **No API but SharePoint's.** Content comes only from your SharePoint, through SharePoint's
  own REST API.

The one Zenpo service the web parts need to run is license checking, described below. On the
Enterprise plan with offline entitlement, the web parts need nothing but your SharePoint.

---

## What is in the package

- 18 web parts. No SharePoint Framework extensions: no application customizers, field
  customizers or command sets.
- Scripts, styles and images ship inside the `.sppkg` file and are served from your own
  SharePoint. No script or style loads from Zenpo or from a third-party CDN.
- The package supports tenant-wide deployment from the app catalog.
- Every release publishes a software bill of materials and build checksums. See
  [Release evidence](#release-evidence).

---

## How the web parts use SharePoint

**Reading.** Web parts read lists, libraries and pages through SharePoint REST as the
signed-in user. SharePoint applies that person's permissions to every read, so each person
gets back only the items they are allowed to see. The images and links a web part shows are
the ones in your own lists and pages.

Org Chart and People Directory read a SharePoint list or a CSV file you control. They do
not read Microsoft Graph or Microsoft Entra ID.

**Writing.** Web parts write to SharePoint only when an author chooses a setup action, and
only under that author's own permissions:

- An optional starter list, with sample rows, that an author chooses to create. The sample
  rows are ordinary list items the author can edit or delete.
- Three page templates that an author installs with Page Templates, and a small setup file in
  the site's Site Assets library. Page Templates never changes, replaces or deletes an
  existing page.
- Images an author uploads to the site's Site Assets library.

Viewers never write to SharePoint.

---

## Your governance applies

Everything the web parts show lives in your SharePoint, so the controls you already set there
apply to it:

- Your data-handling policies decide what may go into a list or library. The web parts show
  what is there and add nothing to it.
- List and library content keeps whatever versioning, retention, audit logging, sensitivity
  labels and eDiscovery your tenant has set, the same as any list or library.
- Banner, Simple Blurbs, Intranet Footer and Page Heading store their content in the page
  itself. It is saved, versioned and published with the page.
- Your SharePoint admin deploys the package from your app catalog and can remove it at any
  time. Removing it leaves your lists, libraries and pages in place.

---

## What leaves your tenant

![What leaves your tenant with an online license check and with offline entitlement](images/data-flow.svg)

This section applies to the free trial, the Pilot, Essential, Standard and Scale plans, and
the Enterprise plan with online licensing.

| Call | When it happens | What it includes |
|---|---|---|
| License check | A web part loads, unless this browser got a license reply for your registered domain in the last 24 hours | SharePoint domain, product identifier, which Zenpo web part made the call, installed package version. Not the page address, and not who is viewing |
| Registration | Once per tenant, when someone accepts the license terms in a web part's settings pane | SharePoint domain, product identifier, the email address of the person accepting, the number of users in the site collection, which web part, package version, a fixed source label |
| Trial extension | An editor extends the trial from the settings pane | SharePoint domain, product identifier, which web part, a fixed source label |
| Subscription | An editor clicks a buy, update, manage billing, cancel or renew button in the settings pane | Sent to buy.zenpo.com: the editor's email address, the SharePoint domain, the address of the page, and the subscription ID if there is one. The buy page opens in a new tab |

As with any web request, the receiving service sees the network address the request comes
from.

**What Zenpo keeps.** A license record for your domain, a log of the license calls it
receives, and, if you buy online, your subscription record.

**What never leaves your tenant:**

- List items, documents, files and page content.
- Names or email addresses of your users. The user count is counted in the browser; only the
  number is sent. The only email addresses sent are the person who accepts the license terms
  and an editor who opens a subscription page.
- Clicks, searches, and who viewed which page.

### If the licensing service cannot be reached

On these plans the web parts need to reach the Zenpo licensing service. If a firewall blocks
it, the web part shows **Unable to reach licensing server**, unless this browser got a
license reply for your registered domain in the last 24 hours. This is a designed state, not
a silent failure. See
[License Messages Explained](https://help.zenpo.com/sharepoint-products/intranet-suite/licensing/license-messages/).

Tenants that cannot allow any outside call use the Enterprise plan with offline entitlement.

---

## What is stored in the browser

- **License reply.** The last license reply, saved for 24 hours in the browser's local
  storage, and a marker that your domain is registered.
- **List data.** To load faster, several list-driven web parts keep a copy of the items they
  show in the browser's local storage. Each copy is reused for a limited time before the web
  part reads the list again; in some web parts the page author sets that time. The copy stays
  on that device and is never sent to Zenpo.
- **Display state.** Small markers such as which accordion sections are open or whether a
  banner video is paused.

---

## Release evidence

Each release has a folder under [releases/](releases/):

| File | What it is |
|---|---|
| `release-notes.md` | What changed in the release |
| `sbom.cdx.json` | Software bill of materials for the package (CycloneDX) |
| `checksums.txt` | SHA-256 hashes the build pipeline recorded when it built the package |
| `build-metadata.json` | Version, build number, pipeline run, source commit and build date |

To check a package file, compute its SHA-256 hash and compare it with the `.sppkg` line in
that version's `checksums.txt`:

```text
macOS or Linux:   shasum -a 256 "Zenpo Intranet Suite for SharePoint.sppkg"
Windows:          Get-FileHash -Algorithm SHA256 "Zenpo Intranet Suite for SharePoint.sppkg"
```

Published release evidence is never changed. A correction ships as a new release.

---

## Reporting a security issue

Email [support@zenpo.com](mailto:support@zenpo.com).

---

## Related pages

- [Enterprise Plan](docs/enterprise-plan.md)
- [Permissions and Data Access](https://help.zenpo.com/sharepoint-products/intranet-suite/permissions/)
- [Requirements and Supported Environments](https://help.zenpo.com/sharepoint-products/intranet-suite/requirements/)
- [License Agreement](https://intranet.zenpo.com/license-agreement)
