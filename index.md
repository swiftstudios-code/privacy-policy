# Privacy Policy for Expired

**Effective date: 12 September 2026**

Expired ("the App") helps you track subscriptions, memberships and documents, and reminds
you before they renew or expire.

The App is published by **Deon O'Brien, Dubai, United Arab Emirates** (trading as Swift
Studios), referred to below as "we" or "I". For privacy purposes I am the data controller
for the limited processing described here.

This policy describes exactly what the App handles, what leaves your device, and what we
never collect.

## Summary

- **No account is required.** There is no sign-up. We never ask for your name, email
  address or password.
- **Your item data stays on your device**, and — if you enable iCloud — syncs privately
  between your own devices through your Apple Account. We cannot see it.
- **We operate no analytics, crash-reporting or advertising SDKs**, and we show no
  advertising.
- We hold three small server-side records about you: a random identifier, a daily
  **count** of AI requests, and whether your Pro subscription is active. Details below.
- **We never sell, rent or trade your information.**

## 1. Information stored on your device

Everything you enter — item names, costs, billing cycles, renewal and expiry dates,
categories, notes, website addresses, and any account email, username or password you
choose to record against an item — is stored locally on your device in the App's private
database.

**Reminders are scheduled and delivered locally by your device.** We operate no
push-notification server, and no reminder passes through us.

## 2. iCloud sync

If iCloud is enabled on your device, the App's database also syncs through **Apple's
CloudKit** into your own private iCloud container, so your items appear on your other
devices. That container belongs to your Apple Account and is governed by
[Apple's Privacy Policy](https://www.apple.com/legal/privacy/). **We have no access to it**
and no ability to read, export or recover its contents.

A small number of preferences (your reminder time and reminder lead time) sync between your
devices through Apple's iCloud key-value store. These are settings, not item data.

You can disable this at any time in your device's iCloud settings, after which your data
remains on the single device.

## 3. Anonymous identifier

**When it is created.** The first time the App launches, it signs in anonymously to our
backend (Supabase) and is issued a **random identifier (a UUID)**. This happens at launch,
before and regardless of whether you use any paid or AI feature, because the same
identifier is used to check your subscription status.

**What it is.** The identifier is generated randomly. It is **not derived from and not
intentionally linked to** your name, email address, Apple Account, device identifier or any
advertising identifier. We cannot use it to work out who you are. Under UK and EU data
protection law it is nonetheless likely to count as **pseudonymous personal data**, and we
treat it as such.

**What it is used for.** Associating a request with a subscription licence, and enforcing
per-user daily limits on AI requests.

**Retention and deletion.** It persists until you delete the App and its data. You can ask
us to delete the identifier and its associated records using the contact details below.

## 4. Server-side records we hold

Our backend runs on **Supabase**. Against your anonymous identifier we store only:

| Record | Contents |
|---|---|
| Anonymous user | The random identifier and its creation timestamp |
| AI usage counter | The date, a count of requests made that day, and an estimated token total |
| Entitlement mirror | Whether Pro is active, and its expiry date |

**We do not store the screenshots you submit, the text extracted from them, or any of your
item data.** The usage record is a counter, not a log of content.

## 5. Information that leaves your device

### AI Screenshot Import (optional)

If you choose to import a screenshot so the App can create items from it, the image is sent
over an encrypted connection to our processing service (a Supabase Edge Function we
operate), which forwards it to one third-party AI provider to extract the text it contains.

**Neither our processing service nor the App stores your screenshot or the text extracted
from it.** The image is held in memory only for the duration of the API call and is not
written to any database or file. What our service records is a counter — see section 4.

The providers currently in use, and what each does with the request:

**Google (Gemini API, paid tier)** —
[privacy policy](https://policies.google.com/privacy) ·
[API terms](https://ai.google.dev/gemini-api/terms)
Google does not use prompts or generated outputs from the paid API tier to train or
fine-tune its models. Requests are retained for up to **55 days** solely for abuse and
safety monitoring, then purged.

**DeepSeek (Open Platform API)** —
[privacy policy](https://cdn.deepseek.com/policies/en-US/deepseek-privacy-policy.html) ·
[terms](https://cdn.deepseek.com/policies/en-US/deepseek-open-platform-terms-of-service.html)
DeepSeek's Open Platform terms are broader. DeepSeek logs API requests and associated
metadata, and its terms and privacy policy reserve rights to use inputs and outputs for
platform development, research and model improvement. **We cannot tell you that data sent
to DeepSeek is never retained or never used for model development, and we do not claim
that.** DeepSeek is based in China, so a request routed to it is processed there.

Because a screenshot may be processed outside the UAE, the UK and the EEA, and because the
DeepSeek terms above are broader than Google's, **please do not import screenshots
containing information you would not want a third party to retain.** If you never use this
feature, no image ever leaves your device.

### Service icon lookup (optional)

When you add an item with a website address, the App may request that site's icon so the item
shows a recognisable logo. The request is sent to public icon services — currently
[Google's favicon service](https://policies.google.com/privacy),
[icon.horse](https://icon.horse/privacy) and
[DuckDuckGo's icon service](https://duckduckgo.com/privacy) — and contains **only the
website domain you entered**. It does not contain the item's name, cost, dates, notes or any
credentials you stored.

### Purchases

Expired Pro is sold through Apple's In-App Purchase. Payment is handled entirely by Apple —
**we never see or receive your payment details.** We use
[RevenueCat](https://www.revenuecat.com/privacy/) to verify subscription status; RevenueCat
receives the anonymous identifier above and the purchase receipt Apple issues, and returns
whether Pro is active. RevenueCat's SDK also collects standard device and app metadata
(such as app version, device model and operating system version) in order to validate
purchases. Subscription changes, cancellations and refunds are handled by Apple.

### Network metadata

Any internet request necessarily reveals technical information to whoever receives it. Our
processing service, the AI providers, the icon services, RevenueCat and Apple will each
receive things such as your **IP address, the time of the request, and network/user-agent
information**. We do not store, analyse or use this metadata for any purpose, and we do not
combine it with anything else; but we cannot claim the request contains nothing beyond the
content described above. Each recipient handles it under its own policy.

## 6. What we never collect

- Your name, email address, phone number or postal address
- The account emails, usernames or passwords you store against items. **These never leave
your device except into your own private iCloud container, and are never transmitted to
us or to any AI provider.**
- Analytics, usage statistics, crash reports or performance telemetry
- Advertising or tracking identifiers
- Your location
- Your contacts, photo library, calendar or health data

## 7. How we use information

We use the limited information described above only to provide the feature you requested,
to enforce fair-use limits, and to verify access to paid features. We do not profile you,
and we do not use your information for advertising or marketing.

## 8. Retention

We do not retain your item data, because we never receive it. We do not retain the
screenshots you submit or the text extracted from them. AI usage counters are kept only as
long as needed to enforce daily limits and understand aggregate load. Entitlement records
are kept for as long as necessary to honour your purchase. You may request deletion of the
records in section 4 at any time.

Retention **by the AI providers** is governed by their own terms, summarised in section 5:
up to 55 days for abuse monitoring at Google, and per DeepSeek's Open Platform terms for
DeepSeek.

## 9. Your choices and your rights

Because your item data is held on your device and in your own iCloud container, you control
it directly:

- **Delete any item** at any time within the App.
- **Delete everything** by deleting the App and, if you used iCloud sync, removing Expired's
data from iCloud in your device settings.
- **Stop all outbound requests** by not using AI Screenshot Import and not entering website
addresses.
- **Withdraw consent** for the optional features simply by not using them; no setting needs
changing and nothing is retained.

If you are in the United Kingdom, the European Union or another region granting
data-protection rights — access, correction, erasure, portability, restriction or objection —
you may exercise them by contacting us below, and we will respond within the period the
applicable law requires. For almost all of your data we hold no copy, so deleting it within
the App is both faster and more complete than a request to us.

## 10. Security

We use reasonable technical and organisational safeguards to protect the limited information
we hold, including encrypted transport and access controls on our backend. However, **no
method of electronic storage or transmission is completely secure**, and we cannot guarantee
absolute security.

## 11. Children

Expired is not directed to children under 13, and we do not knowingly collect personal
information from children.

## 12. Changes to this policy

If this policy changes materially, we will post the updated version at this URL with a new
effective date before the change takes effect.

## 13. Contact

Questions about this policy, or a data-protection request:
**swiftstudio.dob@gmail.com**
