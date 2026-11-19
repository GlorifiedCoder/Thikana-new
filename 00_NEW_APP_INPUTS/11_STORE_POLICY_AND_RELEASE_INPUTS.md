# Store, Privacy and Release Inputs — Thikana

Research snapshot: 20 November 2026. This is an applicability assessment input, not legal advice.

## Distribution

- Target platforms: Flutter Android and iOS.
- Target stores: Google Play and Apple App Store.
- Launch region: Bangladesh initially; international availability not planned for MVP.
- Developer account type: UNKNOWN.
- Release date: UNKNOWN.
- Public website/support site: REQUIRED before submission; domain/name clearance pending.

## Audience and content

- Adult-oriented rental marketplace.
- Guest browsing of public property ads.
- User-submitted listing text, photos, prices, location details and lister profiles.
- Listers can be owners or agents.
- Reviews and public messaging are deferred from MVP.
- No child-directed functionality.

## Accounts and sign-in

- Account creation: Yes, for posting, saving and structured enquiries.
- Browsing should not require login.
- Google login: Yes.
- Apple login: Yes on iOS; configure Android flow only if supported and justified.
- Verified phone number required for listers.
- Account deletion: In-app plus external web deletion request route.
- Admin/moderator reviewer access: Create role-restricted demo account and sample listings; never provide production data.

## Data and permissions

Potential data:
- Name/display name, email, phone, profile, submitted rental listing, photos, approximate property location, saved searches, favourites, enquiries, reports, device push token, logs/analytics.
- Avoid collecting NID, biometric data, background location, contacts, microphone, or precise device location unless a future justified feature needs it.
- Photo picker preferred over broad gallery access.
- Camera only when user chooses camera capture.
- Location only when user chooses "near me"; no background location.
- Analytics/crash SDKs require inventory and privacy review.
- Supabase and provider region/subprocessor locations require Bangladesh cross-border data-transfer legal review.

## UGC safety

- Listing text/photos are user-generated content.
- In-app reporting for listing and lister.
- Block user/account and hide their listings for the reporting user.
- Listing filters and prohibited content checks.
- Moderation queue, appeals/support and documented response process.
- Published contact/support information.
- Rights declaration for listing photos.
- No in-app public chat in MVP. If chat is added later, add message reporting, abuse controls, retention and blocking before release.

## Monetization

- MVP: free browse, free basic listing, free contact.
- No rent, deposit, escrow, lease payment or credit-to-unlock contact.
- Later paid promotion/subscription is undecided and requires Apple/Google billing review, Bangladesh payment-provider and consumer-law review, refund disclosures and merchant compliance.
- Ads deferred.

## Legal research to recheck

- Personal Data Protection Act, 2026 (Act 63 of 2026): lawful processing/consent, data subject rights, confidentiality, technical/organizational safeguards, retention, records and overseas transfer. Confirm rules/notifications and commencement of deferred provisions before release.
- House Rent Control Act, 1991: section 10 restrictions regarding premium/salami/security or similar amounts and more than one month's advance without Controller approval, with statutory exception(s); section 13 rent receipts; obtain legal review on how it applies to listed property categories and how listing forms present such charges.
- Transfer of Property Act, 1882 section 107: registration rule for leases from year to year, term exceeding one year, or reserving yearly rent. Do not generate legal lease documents without counsel.
- Digital Commerce Operation Guidelines, 2021: official gazette exists. Review applicability to classified rental listing, paid promotions, contact fees and any payment service.
- Consumer Rights Protection Act amendment draft reported on 30 September 2026; verify whether enacted before launch. Do not represent the draft as enacted law.
- DPDT trademark and name clearance; exact "Thikana" property apps already exist.

## Release artifacts

Must prepare:
- Privacy Policy (public URL and in-app access).
- Terms of Use and listing rules.
- Safety guidance / scam warning.
- Listing moderation and prohibited-content policy.
- Account deletion page and workflow.
- Support/contact page.
- Data inventory and retention schedule.
- Google Play Data Safety answers based on actual SDK and backend behavior.
- Apple App Privacy answers based on app and third-party SDK practices.
- Content rating, target audience, location/photo permission descriptions.
- Store descriptions, screenshots, app icon and feature graphics.
- Reviewer instructions and demo account.
- Android signing and iOS signing credentials stored securely.
- SDK/license/privacy manifest audit.
- Store minimum target SDK/Xcode requirements checked immediately before upload.
