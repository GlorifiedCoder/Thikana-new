# Business Rules and Data Notes — Thikana

## Roles and permissions

| Role | View | Create/edit/delete | Restrictions |
|---|---|---|---|
| Guest | Public published listings | No account content | No private contact data by default |
| Renter/seeker | Public listings, own saved items/enquiries | Favorites, saved searches, reports, viewing enquiries | Cannot edit listings or access other users' private data |
| Owner/lister | Public listings and own dashboard | Own property listings, availability, photos, status | Cannot claim verification not granted; cannot edit another user's listing |
| Authorized agent/property manager | Same as lister with declared agency role | Listings they are authorized to represent | Must not imply ownership; authorization evidence may be requested |
| Moderator | Assigned listing/report cases | Moderation actions | No access to unrelated sensitive user data |
| Verification operator | Verification evidence and checks | Set precise verification outcome | Limited access; evidence retention rules apply |
| Admin | Operational tools and reporting | Assign cases, manage categories, suspend users | Privileged actions must be audited |
| Super-admin | System administration | Role/configuration management | Very limited account count; MFA; no routine daily use |

One account can act as both seeker and lister; role is a permission capability, not a separate user identity.

## Listing lifecycle

Allowed statuses:
- draft
- pending_review
- changes_requested
- published
- paused_by_owner
- temporarily_unavailable
- rented
- expired
- rejected
- suspended
- removed
- archived

Only `published` listings appear in public search. `rented`, `expired`, `rejected`, `suspended`, `removed`, and `archived` are not publicly shown in normal search.

## Core business rules

1. Every listing must have a category, title, rent, location hierarchy, availability state, lister identity, and minimum mandatory category fields.
2. Rent is expressed in BDT (৳), with an explicit basis (normally per month for MVP).
3. Separate recurring cost lines: service charge, utilities, parking, maintenance, other. State whether each is included, fixed or variable.
4. Do not imply that a rent or advance amount is legal merely because the form accepts it.
5. Bangladesh House Rent Control Act, 1991 section 10 contains restrictions on premium/salami/security or similar amounts and advance rent beyond one month's rent without prior Controller approval, subject to statutory exceptions. Before implementing a public advance/deposit field or payment-related flow, obtain Bangladesh legal review. The app must not recommend an amount or facilitate unlawful collection.
6. The listing lister must declare owner or authorized representative. The declaration is not equivalent to independent proof.
7. Verification badges describe evidence, not a broad guarantee.
8. Material changes (rent, property type, photographs, location, owner/authority) require moderation re-review.
9. Availability updates produce a timestamped event. Lister cannot backdate a confirmation.
10. Proposed freshness policy: send a confirmation reminder on day 14; expire/hide if not reconfirmed by day 30 after last confirmed date. These intervals are product proposals, not market facts; validate with pilot users.
11. Expired listings must not appear in search by default.
12. The owner can mark rented/unavailable immediately. This action removes the listing from public search without waiting for moderation.
13. Suspected duplicate listing should enter review; do not automatically delete based only on similar photos.
14. Photo uploader confirms rights/authorization. Do not scrape other platforms.
15. No rent collection, deposit, escrow, lease execution, or legal brokerage in the MVP.
16. Do not publish full residential address or exact pin by default; disclose approximate area. Exact location/contact disclosure requires owner setting and user action.
17. No paid contact-unlock in MVP. Basic search and contact should be free.
18. Paid promotion, subscription, or ads require later review of store billing, payment-provider, refund and data disclosure rules.

## Category-specific fields

### Flat/apartment
- bedrooms, bathrooms, balconies, floor, total floors, area (sq ft), furnishing, lift, parking, gas type/supply, water, generator, security, family/bachelor suitability if legally reviewed, available-from date.

### House / portion
- whole house or portion, floors/levels, bedrooms, bathrooms, yard/roof/parking, area, furnishing, utility and access details.

### Room / shared room / bed / hostel
- private/shared, beds available/total, room capacity, attached/shared bathroom, meal facilities, gender/safety/house rules only where lawful and carefully reviewed, internet, utilities, curfew if any, available date. Avoid unnecessary sensitive personal data about potential tenants.

### Sublet / flatmate
- portion/room/bed, current occupancy context, permission/authority to sublet declaration, rent, bills included, shared facilities, house rules, available date. Subletting authority must be clearly declared and may require proof.

### Shop / showroom
- frontage, floor/level, floor area, road exposure, foot traffic (lister claim), utility capacity, washroom, loading/access, permitted business use, fit-out condition, parking, lease term.

### Office / commercial space
- area, floor, private/shared, meeting room, power backup, internet/fiber availability (lister claim), lift, parking, washroom, fit-out, access hours.

### Warehouse / godown
- floor area, clear height, loading access, vehicle access, power, safety/fire facilities (claims must not be represented as certified without evidence), loading dock.

## Data collection and privacy table

| Data | Why | Required? | Sensitivity | Access | Retention/deletion |
|---|---|---|---|---|---|
| Auth user ID | Account identity | System | Personal | User/system | Follow account lifecycle |
| Name/display name | Profile and contact context | Minimum display name | Personal | User; public only if chosen | User-editable |
| Email | OAuth/account recovery | Provider-dependent | Personal | User/system | Delete/anonymize per policy |
| Mobile number | Lister verification and contact | Required for lister; optional for casual browsing | Personal | Private; reveal only with consent | OTP status stored; keep per legal need |
| Property listing content | Rental discovery | Required | Public/business data plus potential location risks | Public when published | Archive/delete by policy |
| Approximate property location | Search by area | Required area | Can expose privacy | Public approximate locality | Keep while listing active |
| Exact address/pin | Owner management/contact | Optional | Sensitive location | Restricted | Never public by default |
| Property photos | Listing | Required minimum | May expose residents/interior/private data | Public listing | Strip EXIF; remove on deletion/expiry subject to evidence retention |
| Identity/ownership proof | Optional verification | Not MVP default | High sensitivity | Restricted verification operators only | Minimize, redact, short retention; legal review |
| Search history | Improve UX | Optional | Personal/behavioral | User/system | User controls and retention limit |
| Favorites/saved searches | User convenience | Optional | Personal preference | Owner | Delete with account |
| Enquiry/viewing request | Connect seeker and lister | Optional | Personal | Participants and support under policy | Retention policy |
| Reports/moderation cases | Safety and compliance | When submitted | Potentially sensitive | Moderation team | Documented legal/operational retention |
| Device token | Push notifications | Optional | Online identifier | Notification service | Delete on logout/token expiry |
| Location permission/device GPS | Nearby search | Optional | Sensitive location | On-device, server only if explicitly needed | Prefer selected area; don't collect background location |
| Analytics/crash data | Reliability | Optional/minimized | Device/usage data | App operations/SDK provider | Disclose accurately; retention limit |

## Integrations

| Provider/service | Purpose | Required? | Notes |
|---|---|---|---|
| Supabase Auth | Google/Apple and account sessions | Yes | Region/data-transfer review before production personal data |
| Supabase PostgreSQL | Listings, profiles, moderation | Yes | RLS on exposed tables |
| Supabase Storage | Listing photographs | Yes | Public listing image bucket; private verification bucket only if later approved |
| Maps provider | Map display/geocoding | Optional | Evaluate Google Maps vs MapLibre/OSM provider costs, terms and local coverage |
| SMS/OTP provider | Verify lister phone | Yes for listers | Compare Bangladesh deliverability, cost and regulatory terms |
| FCM/APNs | Notifications | Should | Permission optional and purpose explained |
| FastAPI | Sensitive backend jobs/admin integrations | Conditional | Do not duplicate Supabase CRUD without need |
| Email provider | Alerts/support/verification | Conditional | SPF/DKIM/DMARC and unsubscribe as applicable |
| Analytics/crash provider | Product reliability | Optional | SDK/data disclosure audit |

## Suggested logical data entities

- `profiles`
- `user_role_grants` (server-controlled)
- `locations` (hierarchical, localized labels and aliases)
- `property_listings`
- `listing_photos`
- `listing_amenities`
- `listing_availability_events`
- `listing_verification_checks`
- `listing_authorization_evidence` (only if later approved; private)
- `favorites`
- `saved_searches`
- `enquiries`
- `viewing_requests`
- `listing_reports`
- `user_blocks`
- `moderation_cases`
- `moderation_actions`
- `notifications`
- `notification_preferences`
- `account_deletion_requests`
- `privacy_consent_records`
- `admin_audit_events`

Do not build the final schema until ZCode has converted category rules, status transitions, access rules, retention, and RLS requirements into an ERD and reviewed migrations.
