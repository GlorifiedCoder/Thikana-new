# Open Questions and Decisions — Thikana

Do not silently treat recommendations as approved. The product architect should research options and request owner decisions on blockers.

| Question / decision | Why it matters | Recommendation | Owner decision | Status |
|---|---|---|---|---|
| Can the public brand remain "Thikana"? | Existing Google Play apps and websites use the same name for property marketplace/management | Keep as internal codename only until trademark, store, domain and company clearance; consider distinctive alternative | TBD | BLOCKER before branding |
| Initial launch geography? | Marketplace liquidity and moderation operations | Dhaka pilot, selected neighbourhoods first | TBD | OPEN |
| Which categories on day one? | Complexity and listing supply | Flats/houses, rooms/sublets, shops/offices; add warehouse after validation | TBD | OPEN |
| Is property sale included? | Changes product architecture and marketing | No; rental-only first release | Recommended | PROPOSED |
| Contact method? | UX, privacy and UGC workload | Call/WhatsApp with owner opt-in plus structured viewing request; defer chat | TBD | OPEN |
| Require account to browse? | Search conversion | No account required to browse; require account for save/post/request | Recommended | PROPOSED |
| Lister verification? | Trust and fraud risk | Phone OTP required; explicit labels for each additional check | Recommended | PROPOSED |
| NID/identity check? | High-risk data processing and storage | Do not collect NID by default; if needed, use counsel-reviewed third-party/manual process and retain minimum evidence | TBD | OPEN |
| Property proof? | Prevent unauthorized photos/listings | Declaration first, risk-based evidence/owner confirmation; do not claim ownership verified without evidence | Recommended | PROPOSED |
| Availability expiry intervals? | Stale listings undermine trust | Reminder day 14; hide/expire after day 30 without confirmation, configurable | TBD | PROPOSED |
| Paid contact-unlock? | Trust, refund and consumer concerns | Do not use | Recommended | PROPOSED |
| Monetization? | Store payments and local payment requirements | Free launch; later transparent promoted listings/business subscription after policy assessment | TBD | OPEN |
| Deposit/advance field? | House Rent Control Act restrictions | Do not recommend or collect. Legal counsel to approve whether/what advertiser-declared disclosure can be displayed | TBD | LEGAL BLOCKER |
| Supabase region? | Bangladesh Personal Data Protection Act cross-border provisions | Compare region, data transfer conditions, subprocessors and contracts before production data | TBD | LEGAL/TECH BLOCKER |
| Maps provider? | Cost and location accuracy | Use structured area catalog first; evaluate Google Maps vs licensed OSM-based provider for map/pin | TBD | OPEN |
| SMS provider? | OTP delivery and cost in Bangladesh | Test multiple compliant providers and cost | TBD | OPEN |
| Admin interface? | Moderation needs | Web admin console is required | Recommended | PROPOSED |
| Public reviews? | Adds UGC, defamation and verification concerns | Defer until a credible verified interaction model exists | Recommended | PROPOSED |

## Assumptions the agent must not make

- That "Thikana" is legally or commercially available as a brand.
- That all listings can be called verified.
- That a phone OTP proves property ownership.
- That an agent is authorized simply because they selected "agent".
- That listing photos are owned by the uploader.
- That a property is available because the listing says "available".
- That an in-app viewing request is a confirmed reservation.
- That the platform can collect advance/security deposits.
- That a database region outside Bangladesh is automatically compliant.
- That competitor listing counts are accurate market size.
- That all users are in Dhaka or all areas use the same English spelling.
- That the platform is legally exempt from obligations because it does not own the properties.

## Decisions requiring owner approval before implementation

1. Naming after clearance.
2. Dhaka pilot and first neighbourhoods.
3. Property category set for MVP.
4. Contact and viewing flow.
5. Verification levels and what evidence to store.
6. Legal approval for upfront-cost disclosure.
7. Hosting/data transfer decision.
8. Business model beyond free initial launch.
