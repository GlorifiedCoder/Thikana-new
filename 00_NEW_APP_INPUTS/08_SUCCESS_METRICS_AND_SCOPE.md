# Success Metrics, Scope and Constraints — Thikana

## Main outcome

A renter can find a genuinely available, relevant rental space and reach the correct owner/authorized agent with less wasted time. A lister can publish, keep updated, and manage legitimate rental advertisements without repeated unnecessary calls.

## Success metrics

| Metric | Measures | Initial target | Notes |
|---|---|---|---|
| Freshness confirmation rate | Published listings with recent owner-confirmed availability | Set pilot baseline; target ≥80% within chosen confirmation window | Define time window with pilot |
| Stale listing rate | Listings found unavailable/incorrect after being shown as published | Reduce continuously; establish baseline | Core quality metric |
| Contact success rate | Contact attempts that reach active, correct advertiser | Establish baseline; aim ≥80% after pilot | Survey/contact outcome |
| Owner response rate | Enquiries answered within agreed period | Establish baseline | Measure only if platform enquiry flow exists |
| Search-to-contact conversion | Relevant searches that lead to contact | Establish baseline by category/location | Do not optimize by hiding contact |
| Report resolution time | Time from report to moderation action | Severe safety reports same business day; routine target set operationally | Requires staffing |
| Duplicate/unauthorized listing removal | Reports and admin detections resolved | Track counts and recurrence | Distinguish reports from confirmed cases |
| Listing completion rate | Started listing forms reaching submission | Establish baseline | Reduce form friction |
| Search latency | Server-side result response time | p95 under 1 second for indexed standard searches, subject to infrastructure | Define test dataset |
| Crash-free sessions | Mobile stability | ≥99.5% before broad release target | Release quality target |
| User retention | Renter/lister returning | Track 7-day/30-day | Do not rely only on downloads |
| Supply density | Active, current listings per pilot locality/category | Minimum viable inventory defined before launch | Avoid launching empty areas |

Targets are hypotheses, not claims about current market performance.

## First release scope — MUST

- Android and iOS Flutter apps.
- Bangla/English, BDT.
- Guest browse/search.
- Location and property-type search.
- Residential house/flat/room/seat/sublet/hostel categories.
- Commercial shop and office categories; warehouse if validated.
- Category-specific property details.
- Transparent monthly rent and recurring cost display.
- Listing detail and photo gallery.
- Favorites.
- Google and Apple sign-in, plus verified lister mobile.
- Owner/agent listing creation, drafts, edit, pause, renew, mark rented.
- Review/moderation workflow and admin console.
- Explicit verification levels.
- Availability confirmation/expiry.
- Report listing/user and block user.
- Contact options (call/WhatsApp) with privacy protection.
- Account deletion and privacy controls.
- App store compliance and security baseline.

## Should / follow-up

- Viewing requests.
- Map results.
- Saved searches and push alerts.
- In-app messaging after operational moderation readiness.
- Agent business profile.
- Compare listings.
- Better duplicate photo detection.
- Listing performance metrics for owner.

## Could / later

- Paid listing boost, subscriptions and business packages.
- Public renter/owner reviews after a verified-transaction/visit basis exists.
- AI natural-language search after sufficient inventory.
- Landlord tenant management and rent book as separate module.
- Lease document tools after legal review.

## Explicitly out of MVP scope

- Buying/selling homes, flats, plots, land.
- In-app rent/deposit collection.
- Escrow/holding payments.
- Paid credit to unlock contact.
- Legal advice or guaranteed legal agreements.
- Full property management/accounting.
- Broad anonymous public chat.
- AI-generated fake listing descriptions/photos.
- Nationwide high-touch verification without a staffing plan.

## Launch strategy

Recommended: start with a tight Dhaka pilot and seed quality supply in a few selected neighbourhoods. Keep nationwide location taxonomy ready, but do not market nationwide availability until the app has sufficient active listings and moderation coverage in each location.
