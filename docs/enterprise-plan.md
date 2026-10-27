# Enterprise Plan

**Product:** Zenpo Intranet Suite for SharePoint
**Last reviewed:** 2026-10-27

Some site collections are large. Some tenants can't allow a web part to call an outside
service at all. The Enterprise plan covers both. You buy it by quote, and you get the same
18 web parts and the same features as every other plan.

---

## Who it is for

- Site collections with 2,000 or more users.
- GCC High and DoD tenants, or any tenant whose policy blocks browser calls to an outside
  service.
- Organizations that buy by quote, invoice, purchase order, reseller or contract vehicle.

---

## Two ways to license

The licensing choice comes down to whether the web parts can contact Zenpo. Here's what
changes between the two options:

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

With offline entitlement, the web parts need nothing outside your SharePoint. No Zenpo
service, no Microsoft Graph, no third-party CDN. They make no calls to services outside your
SharePoint, and the content they show comes from your own lists and pages. That's what
allows the suite to run in GCC High and DoD tenants, where outside calls are blocked.

For your reviewers, that means:

- There are no calls to Zenpo. Nothing to allowlist and no license data to review.
- There's no registration step, and no email address is sent anywhere.
- There's no telemetry. Zenpo doesn't know when a page loads or which web part is on it.
- SharePoint permissions work the same way they do on every plan. Each request runs as the
  signed-in user. Nothing elevates access.

---

## Same product in every cloud

None of the web parts use Microsoft Graph, so there's no feature to remove for government
clouds. A web part that works in commercial SharePoint works the same way in GCC, GCC High
and DoD.

---

## How to buy

Enterprise is quoted rather than bought online. You can buy through an invoice, a purchase
order, a reseller or a contract vehicle.

To request a quote, use [zenpo.com/contact-us](https://zenpo.com/contact-us/) or email
[support@zenpo.com](mailto:support@zenpo.com).

---

## Related pages

- [Security and Data Handling](../SECURITY.md)
- [Pricing](https://intranet.zenpo.com/pricing)
- [License Agreement](https://intranet.zenpo.com/license-agreement)
