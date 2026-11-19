# App Idea — Thikana (Working Name)

## One-sentence idea

Thikana is a Bangladesh-focused mobile rental marketplace where people can discover houses, flats, apartments, rooms, seats, sublets, shops, offices, and other spaces for rent, while owners and authorized agents can publish and manage accurate rental listings.

## Problem

Finding a suitable rental property in Bangladesh is fragmented and time-consuming. Rent seekers often search across classifieds, Facebook groups, agents, signs, and word of mouth. Listings can be old, already rented, duplicated, misleading, missing key cost details, or posted using photographs without permission. Contact numbers may be inactive and the person posting may not be the owner or an authorized representative.

Owners also face wasted calls after renting a property, unauthorized use of their photos, and difficulty keeping listing status updated.

Recent reporting in Dhaka Tribune (26 October 2026) documents complaints about outdated advertisements, inactive phone numbers, incorrect addresses, unclear credit/refund arrangements, and photos used without owner permission. The report also cautions that no comprehensive public statistic currently establishes the sector-wide rate of bad listings.

## Proposed solution

Build a rental-only marketplace with:
- Search and discovery by property type, location, rent budget, availability, and property-specific features.
- Structured listing forms for residential and commercial rental spaces.
- Clear monthly rent and disclosed recurring charges.
- Listing status, last-confirmed availability date, and expiry/reconfirmation workflows.
- Explicit, evidence-based verification badges instead of a vague "fully verified" claim.
- Owner/authorized-agent account profiles and listing-management tools.
- Direct contact options and optional viewing requests.
- Reporting, blocking, moderation, and complaint handling.
- A lightweight admin dashboard to review listings, handle reports, verify evidence, and remove scams or stale listings.

The platform should help users discover and contact property advertisers. The first release should not act as a rent/deposit escrow service, sign tenancy agreements, guarantee property title, or broker the tenancy transaction.

## App name

**Thikana** — user-selected working name.

Important: public research found existing Bangladesh property apps and websites already using "Thikana", including Google Play apps covering flats, land, shops, rent and sale. Treat the name as provisional until trademark, app-store, company-name, domain, and social-handle clearance is completed. See `18_NAME_AND_BRAND_CLEARANCE.md`.

## Target users

1. Rent seekers: families, individuals, students/adults, professionals, and people relocating.
2. Commercial tenants: shop owners, small businesses, offices, showrooms, restaurants, and service businesses.
3. Property owners/landlords.
4. Authorized agents and property managers.
5. Internal administrators, moderators, and customer support.

The app should support a user who is both a renter and a property lister under one account, with role-appropriate capabilities.

## Geography

Bangladesh-first. Recommended operational pilot: Dhaka, using selected high-demand neighbourhood clusters rather than launching every district with an empty marketplace. The data model and location catalogue should support nationwide expansion (division, district, upazila/thana, locality/area, and where useful ward/road). The exact launch geography requires owner approval.

## Property types

### Residential rental
- Full house
- Flat/apartment
- Portion of a house
- Private room
- Shared room / bed / seat
- Sublet
- Hostel / mess accommodation
- Family and bachelor-oriented listings where lawful and appropriate

### Commercial rental
- Shop
- Showroom
- Office room / office floor
- Commercial building / space
- Restaurant or retail space
- Warehouse / godown
- Other clearly described business premises

Support category-specific fields; do not show irrelevant residential fields on a shop listing or vice versa.

## Platforms and technology preferences

- Flutter app for Android and iOS.
- Supabase for authentication, PostgreSQL, storage, and Row Level Security.
- Google sign-in and Apple sign-in; add verified mobile number for listing owners/agents.
- Optional FastAPI service only where server-side business logic, scheduled listing expiry, moderation, notifications, or integrations justify it.
- A web-based internal admin/moderation console is required for operation.
- Machine A: source-code creation and lightweight tests.
- Machine B: native builds, emulator, real-device testing, and release preparation.
- iOS release requires macOS and Xcode.

## Core differentiation

Do not compete only on the number of listings. Compete on listing freshness and transparent trust:
- Show when availability was last reconfirmed.
- Expire or hide stale listings automatically.
- Show precisely what has been verified (phone, identity, ownership authority, physical visit, availability), not one ambiguous badge.
- Report false, rented, duplicate, misleading, unauthorized-photo, and scam listings.
- Show rent and recurring cost components transparently.
- Do not charge renters to unlock basic contact details in the MVP.

## Business model

MVP recommendation: free browsing, free basic listing, and free contact. This reduces friction and avoids creating the same trust problem as paid contact-unlock systems.

Potential later revenue:
- Clearly labelled promoted listings.
- Verified business/agent subscriptions.
- Property-management tools.
- Carefully reviewed advertising.

Do not implement paid boosts, contact credits, commissions, rent collection, deposits, escrow, or digital subscriptions in the MVP. Evaluate store billing, Bangladesh payment regulation, refunds, consumer disclosures, and legal obligations before introducing paid features.

## Non-negotiable product principles

- No fake/sample property presented as a real available rental.
- No false "verified" claim.
- No public display of an owner's private phone number unless the owner has opted in and the user deliberately reveals it.
- No exact residential pin/address shown publicly by default; use approximate area until the owner chooses to share details.
- No user is asked to pay rent, advance, or deposit through Thikana in the MVP.
- No collection of NID scans or sensitive identity documents unless a documented necessity, lawful basis, retention rule, security controls, and legal review exist.
- No scraping/copying competitor or Facebook listings without permission and rights to republish.
- No listing can remain active indefinitely without availability confirmation.
- Bengali and English support; BDT (৳); Asia/Dhaka timezone.

## Existing visual direction

The user previously worked with rental/property-app visual references. The current uploaded intake files did not include those images. Add the selected screenshots to `assets/screenshots/` and describe what must be preserved before implementation. Do not invent screenshot-specific requirements.
