# Release Notes: v1.0.1.0

**Date:** October 18, 2026

## What's fixed

- **Settings pane on dark site themes.** On a dark site theme, the settings pane of every
  Zenpo web part showed white text and dark controls on a white pane. Labels, dropdowns,
  toggles, sliders, list and column pickers, color swatches and the License section are
  readable again on every site theme, across all web parts.
- **Zenpo Mini Calendar.** The "Inherit from Theme" option follows the site theme again
  instead of showing a grey grid with dark text.
- **Zenpo Stats Counter.** The State colors help text now says which stats use state colors
  and how to type the values.

## Why the settings pane broke

In August 2026 Microsoft changed SharePoint's page editing tools to a neutral color scheme
(Microsoft 365 Roadmap 566698, Message Center MC1426716). Web part toolbars and the property
pane stopped following the site theme; page content still does. Our settings controls kept
drawing in the site theme, so on a dark site they showed white text and dark controls on the
new white pane. We ran our QA pass in the same weeks the change was rolling out, before it
reached our tenants, which is why it was not caught then. This release moves every Zenpo
settings control onto the pane's own theme.

Microsoft's roadmap entry: https://www.microsoft.com/microsoft-365/roadmap?id=566698

Nothing new was added in this release.

---

**Release files:** [v1.0.1.0](https://github.com/zenposoftware/zenpo-intranet-suite-sharepoint-docs/tree/main/releases/v1.0.1.0/)
