# Release Notes: v0.8.2.0

**Date:** 2026-09-29

## Changes

- **Production licensing**: this is the first package connected to Zenpo's production
  licensing service. Trial registration and license checks run against production.
- **Checkout opens at once**: Buy, Update, Manage billing, Cancel and Renew open a new tab the
  moment you click, show a short "Opening your checkout" page, then take you to the checkout or
  billing page. This works in Safari and in private or InPrivate windows.
- **Renew works**: renewing an expired subscription takes you to the right place for your
  account: the open invoice, a new checkout on your plan, or billing.
- **Clearer registration**: an account with no email address is told why it cannot register,
  and when the licensing service refuses a registration, its own message is shown instead of a
  generic error.
- **Less data on registration**: trial registration no longer sends an IP address or a
  customer name. License calls now include the installed package version.
- **Privacy fix**: the web parts no longer write the site's user list (names and email
  addresses) to the browser's developer console, and each page load makes one fewer call to
  SharePoint.
- **Links**: the license agreement link points at intranet.zenpo.com/license-agreement, and the
  documentation link in each web part's property pane opens
  help.zenpo.com/sharepoint-products/intranet-suite/.
- **Org Chart and Full Calendar**: the expanded view sits above the SharePoint bars instead of
  under them, the org chart centers on open, and scrollbars are thin and match the theme on
  Windows.

---

**Release evidence:** [v0.8.2.0](https://github.com/zenposoftware/zenpo-intranet-suite-sharepoint-docs/tree/main/releases/v0.8.2.0/)
