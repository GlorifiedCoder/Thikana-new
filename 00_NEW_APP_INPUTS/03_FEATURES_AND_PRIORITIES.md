# Features and Priorities — Thikana

Priority meanings: Must = first public MVP; Should = early follow-up; Could = later; Defer = intentionally not in MVP.

| Feature | Description | Who uses it | Priority | Phase | Notes/open questions |
|---|---|---|---|---|---|
| Guest browsing | Browse published listings without account | Rent seeker | Must | MVP | Registration should not block discovery |
| Location hierarchy | Nationwide division/district/upazila-thana/locality filters | All | Must | MVP | Confirm data source and aliases |
| Residential categories | House, flat, room, seat/bed, sublet, hostel/mess | Seekers/listers | Must | MVP | Category-specific fields |
| Commercial categories | Shop, showroom, office, warehouse/godown, commercial space | Seekers/listers | Must | MVP | Prioritize shop/office first |
| Search and filters | Rent, type, location, area/size, rooms, availability, furnishing, amenities | Seeker | Must | MVP | Fast, indexed, server-side |
| Sort | Relevance, newest, rent low-high/high-low, last-confirmed | Seeker | Must | MVP | Do not label sponsored results as organic |
| Listing detail | Photos, location, rent, costs, details, availability, lister, trust evidence | Seeker | Must | MVP | Exact cost fields need legal review |
| Favorites | Save listing | Seeker | Must | MVP | Sign-in needed |
| Lister account | One user may be seeker and owner/agent | Lister | Must | MVP | Role capability, not isolated accounts |
| Google sign-in | Supabase-backed OAuth | All | Must | MVP | Android+iOS |
| Apple sign-in | Supabase-backed sign-in | iOS users | Must | MVP | Required subject to Apple Guideline 4.8 applicability |
| Mobile verification | OTP-verified phone for people posting/contacting at scale | Lister | Must | MVP | SMS provider and cost unknown |
| Create/edit listing | Multi-step category-aware form and drafts | Owner/agent | Must | MVP | Keep completion short |
| Upload property images | Multiple compressed photographs | Lister | Must | MVP | Remove EXIF; enforce limits |
| Authority declaration | Lister declares owner or authorized agent | Lister | Must | MVP | Not proof by itself |
| Listing review | Admin/automated checks before publishing | Admin | Must | MVP | Need operator process |
| Explicit verification badges | Distinguish phone, identity, authority, visit, availability | All | Must | MVP | Exact evidence/meaning visible |
| Availability confirmation | Lister reconfirms availability; stale listings expire | Lister/admin | Must | MVP | Proposed reminder/expiry policy |
| Mark rented/unavailable | Remove from active search immediately | Lister | Must | MVP | Audit event |
| Duplicate detection | Detect suspected duplicate property/photo/phone/location | Admin | Must | MVP | Human review of uncertain matches |
| Report listing | Fake, rented, price, address, scam, unauthorized photo etc. | Seeker | Must | MVP | Must reach admin queue |
| Block lister/account | Prevent further contact/showing unwanted content | Seeker | Must | MVP | App-store UGC safety |
| Admin web console | Moderation, reports, verification, status and audit | Operations | Must | MVP | Internal web access restricted |
| Direct contact | Call/WhatsApp or reveal number with consent/rate limits | Seeker/lister | Must | MVP | Avoid scraping |
| Viewing requests | Structured request for preferred visit time | Seeker/lister | Should | MVP+ | Must not imply reservation |
| In-app messaging | Private conversation | Seeker/lister | Should | Later | Adds moderation, retention, block/report workload |
| Map view | Approximate property pins | Seeker | Should | MVP+ | Provider and cost decision |
| Saved searches/alerts | Notify when matching listings arrive | Seeker | Should | MVP+ | Push consent |
| Listing freshness label | Show date availability was confirmed | Seeker | Must | MVP | Core differentiator |
| Cost transparency | Rent + recurring costs + included/excluded items | Seeker/lister | Must | MVP | Advance/security field requires legal review |
| Bengali and English | Bilingual interface and searchable localities | All | Must | MVP | Bangla default recommended |
| Theme settings | System, Light Blue, Light Gold, Dark | All | Should | MVP | User has requested these four themes |
| Compare listings | Compare rent, area, facilities and location | Seeker | Could | Later | Avoid overloaded UI |
| Agent/business profile | Public profile and listings for verified agents | Agent | Should | Later | Build after owner flow |
| Premium promotion | Clearly-labelled featured/boosted listings | Lister | Defer | Later | Store billing/payment/legal review |
| Advertisement | Third-party ads | All | Defer | Later | Privacy, consent, SDK and UX review |
| Rent payments | Collect rent through platform | Owner/tenant | Defer | Out of scope MVP | Licensed PSP/payment partner, escrow and laws |
| Security deposit/advance collection | Collect holding/deposit payments | Owner/tenant | Defer | Out of scope MVP | Legal risk under House Rent Control Act |
| Digital lease generation/e-sign | Create or sign tenancy documents | Owner/tenant | Defer | Later/possibly out | Local legal counsel and electronic-signature review |
| Tenant/property management | Rent ledger, recurring invoice, maintenance | Owner/tenant | Defer | Later | Separate product scope |
| Public reviews/ratings | Tenant or owner reviews | All | Defer | Later | Verification, defamation and moderation risks |
| AI property matching | Natural-language rental search | Seeker | Could | Later | Only after inventory quality |
| Property sale/land purchase | Buy/sell properties | Buyer/seller | Explicitly out of MVP | Later separate decision | User's current ask is rentals |
