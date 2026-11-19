# Thikana — Detailed Screen Catalog and UI Behavior

## Navigation proposal

Bottom navigation:
- Home
- Explore
- Post
- Saved
- Account

Post may be a prominent central action but must be visually and functionally consistent with accessibility patterns.

## Home

Purpose: help users begin a search immediately.
Components:
- City/area selector.
- Search prompt (e.g. "Which area do you want to rent in?").
- Residential and commercial category shortcuts.
- Budget quick ranges.
- Recently added listings.
- Availability recently reconfirmed.
- Popular localities.
- Clear guest browsing path.
Do not show fake inventory or empty-state numbers.

## Explore / results

- List and optional map toggle.
- Filters for property type, locality, budget, availability and core category details.
- Sort by relevance, latest, rent low/high, availability last confirmed.
- Listing cards show photo, category, monthly rent, approximate area, top 2–3 attributes, availability-confirmed date and precise badges.
- Sponsored placements (if introduced later) must be distinctly marked and not misrepresented as organic relevance.

## Filters

Common:
- Location hierarchy.
- Monthly rent min/max.
- Property type.
- Available from.
- Furnished/unfurnished.
- Area size.
- Utilities and parking.

Residential:
- Bedrooms, bathrooms, floor, lift, balcony, family/bachelor suitability only after policy review, sublet/hostel/seat, shared/private.

Commercial:
- Shop/office/showroom/warehouse type.
- Area and floor.
- Frontage/road access if applicable.
- Power, washroom, parking, loading and business-use constraints.

Avoid filters for sensitive personal attributes of prospective tenants.

## Property detail

Sections:
1. Photo gallery.
2. Title and monthly rent.
3. Locality; approximate map by default.
4. Availability status + last reconfirmed date.
5. Verification badges with "what this means".
6. Property attributes.
7. Recurring cost breakdown (service charge, utilities, parking; advance/security only if legal review approves how to display).
8. Availability date and minimum period if applicable.
9. Facilities and house rules.
10. Advertiser card: owner or agent, phone confirmation and other exact check levels.
11. Call / WhatsApp / Request Viewing.
12. Save/share.
13. Report listing.
14. Safety guidance.

## Add listing wizard

Step 1: residential or commercial.
Step 2: category (flat, house, room, seat, sublet, hostel, shop, office, warehouse etc).
Step 3: location hierarchy; exact address stored privately, approximate public area.
Step 4: category-specific property details.
Step 5: rent and ongoing charges; upfront-payment field only after legal approval.
Step 6: availability date/status.
Step 7: photos and image-rights declaration.
Step 8: lister role/authority declaration and phone verification.
Step 9: preview, terms acceptance and submit.
Step 10: status page showing pending review/approved/changes requested/rejected.

Each step should autosave draft and show completion progress. Do not ask every property category to fill irrelevant fields.

## Lister dashboard

- Listing status tabs.
- Enquiry/viewing requests.
- "Confirm availability" action.
- Edit, pause, mark rented, renew, archive.
- Views and contact taps later (avoid misleading counts).
- Rejection reasons and resubmission.

## Trust and safety UI

- "Phone confirmed" does not equal "property ownership verified".
- "Owner authorization reviewed" only after evidence reviewed.
- "Availability confirmed on [date]" does not guarantee future availability.
- Always provide report controls.
- Make blocked users/listings disappear from user's experience.
- Provide a clear safety centre: visit first, verify identity and authority, read/sign appropriate agreement, do not transfer money based only on messages or photos.

## Theme and localization

- System
- Light Blue
- Light Gold
- Dark

Design tokens must keep contrast, states and focus visible in all themes. Bangla/English switch must not break layout.
