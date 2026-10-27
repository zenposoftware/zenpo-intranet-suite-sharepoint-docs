# Enterprise Plan

**Product:** Zenpo Intranet Suite for SharePoint
**Last reviewed:** 2026-10-27

The Enterprise plan is for large site collections and for tenants that cannot allow a web
part to call an outside service. It is quoted, not bought online. It has the same 18 web
parts and the same features as every other plan.

---

## Who it is for

- Site collections with 2,000 or more users.
- GCC High and DoD tenants, and any tenant whose policy blocks calls from the browser to an
  outside service.
- Organizations that buy by quote, invoice, purchase order, reseller or contract vehicle.

---

## Two ways to license

![What leaves your tenant with an online license check and with offline entitlement](../images/data-flow.svg)

| | Online license check | Offline entitlement |
|---|---|---|
| How the license is confirmed | The web parts call the Zenpo licensing service, as described in [SECURITY.md](../SECURITY.md#what-leaves-your-tenant) | Zenpo builds a package for your organization with your entitlement inside it. The web parts confirm it without contacting Zenpo |
| Calls from the web parts to Zenpo | The calls listed in [SECURITY.md](../SECURITY.md#what-leaves-your-tenant) | None |
| Telemetry | Zenpo keeps a log of license calls | None. Zenpo receives nothing from your tenant |
| Registration in a web part | Once per tenant | None |
| Firewall rules to add | The Zenpo licensing service | None |
| SharePoint environments | Commercial and GCC | Commercial, GCC, GCC High and DoD |

---

## Offline entitlement

With offline entitlement, the web parts depend on nothing outside your SharePoint: no Zenpo
service, no Microsoft Graph, no third-party CDN. The web parts call no service outside your
SharePoint, and what they show comes from your own lists and pages. That is what lets the
suite run in GCC High and DoD tenants, where outside calls are blocked.

What your reviewers will see:

- No calls to Zenpo, so there is nothing to allowlist and no license data to review.
- No registration step, and no email address sent anywhere.
- No telemetry. Zenpo does not know when a page loads or which web part is on it.
- The same SharePoint permission model as every plan: every request runs as the signed-in
  user, and nothing elevates access.

---

## Same product in every cloud

No web part uses Microsoft Graph, so no feature is removed for government clouds. A web
part that works in commercial SharePoint works the same way in GCC, GCC High and DoD.

---

## How to buy

The Enterprise plan is available by quotation and purchase order. It can be bought through
an invoice, a purchase order, a reseller, or a contract vehicle.

To request a quote, use [zenpo.com/contact-us](https://zenpo.com/contact-us/) or email
[support@zenpo.com](mailto:support@zenpo.com).

---

## Related pages

- [Security and Data Handling](../SECURITY.md)
- [Pricing](https://intranet.zenpo.com/pricing)
- [License Agreement](https://intranet.zenpo.com/license-agreement)
