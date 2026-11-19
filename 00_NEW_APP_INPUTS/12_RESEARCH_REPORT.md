# Thikana — Deep Product and Market Research

**Prepared:** 20 November 2026  
**Market focus:** Bangladesh  
**Research method:** Public competitor websites, Google Play listings, official Bangladesh laws/gazettes, and recent local reporting.  
**Scope:** Rental discovery and listing marketplace for homes, flats, rooms, shops and commercial spaces.

## Executive assessment

A Bangladesh rental marketplace is a real, understandable product category, but it is not an empty market. Multiple local products already cover houses, flats, rooms, sublets, hostels, offices and shops. A generic listing app would have weak differentiation.

The most compelling product opportunity is to reduce the cost of bad information:
- listings that are already rented;
- inactive or incorrect phone numbers;
- false/duplicated properties;
- photographs posted without owner permission;
- unclear advertiser identity or authority;
- unclear recurring and upfront costs;
- inadequate complaint and removal processes.

Dhaka Tribune's 26 October 2026 reporting documented these pain points and quoted DNCRP's complaints deputy director saying platform responsibilities include advertiser identity verification, removing outdated listings promptly, and transparent complaint resolution. The same report carefully states there are no comprehensive statistics establishing the proportion of false/outdated listings. Do not invent one.

**Product recommendation:** Thikana should sell confidence through transparent evidence and freshness, not claim "all listings verified" or compete only on inventory volume.

## Market scope and category

Bangladesh-first rental marketplace:
- Residential: house, flat/apartment, room, shared room/seat, sublet, hostel/mess.
- Commercial: shop, showroom, office, commercial floor/space, warehouse/godown.
- Rental-only MVP; property sales, land sales, tenant accounting and rent collection should not dilute the first product.

The product should support nationwide location data but start operations in a dense pilot geography—recommended Dhaka neighbourhood clusters—because a two-sided marketplace needs enough current supply and response capacity in each location.

## Market evidence and limitations

### What can be supported

1. Several rental platforms already list categories spanning residential and commercial rental.
2. Bikroy displayed approximately 3,109 house/apartment rental ads across Bangladesh on 25 October 2026, as reported by Dhaka Tribune. This is a dated observation, not total market size or proof of unique active properties.
3. Google Play public pages show installed apps with 100K+ downloads for some incumbents and lower ranges for others. These figures are platform-reported ranges, can change, and do not establish monthly active users, real listing quality, revenue, or market share.
4. Public local reporting documents complaints about stale listings and misused photos but says sector-wide rates are not known.

### What is not established

- Total Bangladesh rental market size or value.
- Annual number of rental transactions.
- Number of unique active listings across all websites.
- Market share or active users of competitors.
- Verified false-listing rate.
- Rent price index or reliable neighbourhood-level median rent.

Do not write a fabricated TAM/SAM/SOM. Build a small primary research dataset from real tenant/owner interviews and a manually documented listing sample.

## Competitor landscape

See `13_COMPETITOR_MATRIX.md`.

- **Bikroy:** large classifieds marketplace with property rentals; breadth and discovery.
- **Tolet Zone:** rental-oriented app with significant public Play Store install/review range.
- **THE TOLET:** rental discovery and service/credit-based access; public reviews and press reporting highlight contact/listing accuracy concerns.
- **Tolet BD:** category and location filtering across family/bachelor/hostel/sublet/office/shop; direct contact and owner/tenant tools.
- **BDToLet:** property categories, room/seat/sublet/flatmate, maps, contact and rent management features.
- **Dhaka Resident:** early-stage rental marketplace with pre-publication review, viewing requests and approximate public location.
- **Existing Thikana-branded apps/sites:** direct naming overlap in same market.

## Competitive gap

The opportunity is not "we have filters too." It is to operationalize freshness and transparency:
1. Show exactly what was checked.
2. Make availability confirmation date visible.
3. Expire stale inventory automatically.
4. Give owner/agent authority a clear status.
5. Detect suspicious duplicates and copied photos.
6. Explain all recurring charges.
7. Keep basic contact free at MVP.
8. Provide reporting and visible complaint status.
9. Remove rented listings immediately when owner marks them rented.
10. Publish a clear safety process; never imply that Thikana guarantees ownership, legal title or physical conditions unless a defined verification program proves it.

## Recommended trust model

Do not use one ambiguous "Verified" badge.

- **Phone confirmed:** advertiser controlled the phone number using OTP.
- **Identity reviewed:** identity was reviewed through an approved process; this does not prove ownership.
- **Owner authority reviewed:** evidence supports owner's authority or agent authorization for this property.
- **Location visited:** a named field process verified that a property appears at the stated location on a given date; it does not prove title or legal compliance.
- **Availability reconfirmed:** lister confirmed the property is still available on a date.
- **Not independently inspected:** show when no inspection has occurred.

At MVP, start with phone confirmation, authority declaration, manual listing moderation and availability reconfirmation. Do not collect NID by default. Design optional verification only after legal/security review.

## Recommended MVP operating model

- Free browsing and basic listing.
- Guest search.
- Sign-in only when saving/posting/structured enquiry is needed.
- Phone OTP for listers.
- Owner/agent status declaration.
- Manual review at launch (or risk-based manual review after volume is measured).
- Availability reconfirmation workflow with configurable reminder/expiry.
- Reports for wrong/old/fake/duplicate/unauthorized-photo/scam listings.
- Admin team must be staffed before public UGC launch.
- No in-app rent/deposit payments or legal lease generation.
- No paid credit contact gating.

## Recommended differentiators

### 1. Availability freshness
Display "Availability last confirmed [date]". Prompt listers to reconfirm on a recurring schedule. Proposed initial rule: reminder at 14 days; hide/expire after 30 days without confirmation. Validate through pilot metrics.

### 2. Verification transparency
Each badge has a tooltip that explains exactly what was checked. Never convert phone OTP into an "owner verified" label.

### 3. Transparent rental cost
Show base monthly rent and recurring service/utilities/parking charges separately. Legal review is required before displaying advance/security-related amounts.

### 4. Better local search
Structured Bangla/English administrative hierarchy and neighbourhood aliases. Support location and category combinations (e.g., shop in a locality, family flat near a chosen area).

### 5. Lister quality tools
Drafts, listing status, inquiries, availability updates, duplicate warnings, and "mark rented" action.

### 6. Safety
Report listing/user, block, moderation, scam warning, and complaint case tracking.

## Go-to-market recommendation

1. Choose one pilot zone in Dhaka and a few adjacent neighbourhoods only after owner research.
2. Recruit a small, accountable cohort of real landlords/property managers/agents.
3. Manually check initial listings and contact/availability.
4. Give owners a very simple listing and renewal flow.
5. Measure active listings, response rate, stale rate, report rate and renter search-to-contact conversion.
6. Expand by locality/category only when fresh supply exists.

Supply-side acquisition can include owner referrals, property managers and carefully permissioned local agency partnerships. Do not scrape Facebook groups or competitor databases.

## Brand risk: Thikana

This is a major finding:
- A Google Play app named "Thikana" by Jalali Tech Store advertises property buying, selling and renting, including flats and shops.
- Another Play Store app "Thikana ঠিকানা" by kobul.com describes a property marketplace and added rent functionality.
- `thikanakujun.com`, `thikana.bd`, and `thikana.top` show property-related brand use.

This makes the name crowded and confusing in the exact category. It does not prove the developer lacks trademark rights, but a new app should not assume the name is available. Keep as internal codename pending official trademark search in relevant classes, app-store search, company name/domain/social checks, and legal counsel. See `18_NAME_AND_BRAND_CLEARANCE.md`.

## Technical recommendation

- Flutter Android/iOS.
- Supabase Auth/Postgres/Storage with RLS.
- Optional FastAPI backend for privileged operations, scheduled expiry, moderation integration, and notifications; avoid duplicating normal CRUD unnecessarily.
- Admin web console is essential.
- Structured location taxonomy plus optional map provider.
- FCM/APNs for notification.
- Git and CI with Machine A/Machine B workflow.

Do not select production Supabase region until cross-border personal data rules have been reviewed.

## Decisions needed before code

See `09_OPEN_QUESTIONS_AND_DECISIONS.md`. Most important:
1. brand name;
2. pilot location;
3. category scope;
4. contact method;
5. verification process;
6. legal treatment of upfront amounts;
7. Supabase region/data transfer;
8. business model.
