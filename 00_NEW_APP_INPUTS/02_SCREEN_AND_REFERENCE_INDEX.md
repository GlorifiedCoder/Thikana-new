# Screen and Reference Index — Thikana

## Visual references

No screenshot image files were included in this intake upload. Add the user's approved property-app screenshots and any inspiration images to `assets/screenshots/` or `assets/design_references/` before implementation.

For every reference, document:
- What must be preserved (layout, hierarchy, visual density, components, navigation, icons).
- What may be improved.
- Which interactions are not visible in the static image.
- Whether the reference is original user work or third-party inspiration.

## Product visual direction

Recommended direction:
- Clean, premium, trustworthy property marketplace.
- Listing photographs are the primary visual asset.
- Strong readable rent price and location hierarchy.
- Spacious cards and uncluttered filtering.
- Neutral surfaces with one recognizable brand accent.
- Avoid dense classifieds layouts, excessive badges, loud gradients, misleading urgency, and too many promotional banners.
- Trust information should be legible and specific, not decorative.
- Use Bengali typography with proper Unicode rendering and legible English.
- Support user's previously requested themes: System, Light Blue, Light Gold, and Dark. Theme choice must not reduce contrast or accessibility.

## Recommended main navigation

Proposed bottom navigation:
1. Home — discovery, search, categories, recently added/confirmed listings.
2. Explore — search results and map/list views.
3. Post — create a rental listing (visible to eligible listers).
4. Saved — favourites and saved searches.
5. Account — profile, role switch, my listings, alerts, settings, help, privacy.

The final navigation structure must be validated against the complete screen design.

## Core screen inventory

| Screen | Main purpose | Important interactions | Priority |
|---|---|---|---|
| Splash / app initialization | Restore auth and settings | Session check, theme and locale restore | Must |
| Onboarding / location preference | Help users start searching | Choose city/area or skip | Should |
| Home | Entry point for rental discovery | Search, location, property categories, new/confirmed listings | Must |
| Location picker | Select area precisely | Division → district → upazila/thana → area; search aliases | Must |
| Search results | Browse matching properties | Sort, filters, list/map switch, pagination | Must |
| Filter sheet | Narrow search | Rent range, type, availability, rooms, size, amenities | Must |
| Map results | Understand approximate distribution | Pan, zoom, select pin, return to list | Should |
| Property details | Evaluate a property | Photo gallery, costs, amenities, availability, trust evidence, report, save | Must |
| Photo gallery | Inspect listing images | Zoom, swipe, report inappropriate image | Should |
| Lister profile | Understand who posted | Role, phone verified status, active listings, report/block | Must |
| Contact options | Contact advertiser | Reveal/call/WhatsApp where enabled, viewing enquiry | Must |
| Viewing request | Request a visit | Preferred time, message template, confirmation | Should |
| Sign-in / account creation | Authenticate | Google, Apple, email/phone as selected | Must |
| Account linking | Manage providers | Link/unlink safely; avoid accidental duplicate accounts | Should |
| Create listing wizard | Submit a rental property | Category-specific steps, save draft, upload photos | Must |
| Listing preview | Confirm ad before submission | Edit, confirm authority, submit for review | Must |
| My listings | Manage posted properties | Edit, pause, mark rented, renew, delete | Must |
| Listing status detail | Explain moderation/status | Rejection reason, required changes, availability updates | Must |
| Saved properties | Return to favourites | Remove, compare, share | Must |
| Saved searches / alerts | Revisit search criteria | Create/edit/delete alert | Should |
| Notifications | Show enquiries and listing updates | Mark read, deep-link | Should |
| Report listing/user | Report misuse | Select reason, add evidence, submit | Must |
| Blocked accounts | Control unwanted contact/content | Block/unblock | Must |
| Help & safety centre | Safety education and support | Contact support, safety tips, complaint tracking | Must |
| Account & privacy settings | Manage preferences and data | Language, theme, notifications, privacy, export/delete | Must |
| Delete account | Account deletion | Explain effects, re-authenticate, request deletion | Must |
| Admin sign-in | Internal access | Secure role-based access | Must |
| Admin moderation queue | Review new/reported listings | Approve, reject, suspend, remove, record reasons | Must |
| Admin listing detail | Inspect evidence | Compare duplicates, photos, contact and history | Must |
| Admin user verification | Review proof and role | Approve/reject exact verification level | Must |
| Admin report queue | Resolve user reports | Triage, contact reporter, action, audit | Must |
| Admin audit log | Track sensitive actions | Search and inspect actions | Must |

## Interactions requiring special design

- Guest users should be able to browse listings; do not force login before showing inventory.
- Saving, posting, or sending a structured enquiry may require authentication.
- Posting should require verified mobile number.
- Use system photo picker; request camera only when user chooses to take a photo.
- Use approximate map area publicly; exact address visibility is controlled by lister and user action.
- Contact reveal must be protected against automated scraping and abuse.
- Editing rent, photos, address, property type, or ownership/authority details should send the listing back through moderation.
- Updating only availability should create a dated confirmation event and preserve audit history.
- Every listing must display its availability status and last confirmed date.
- No fake "booking confirmed" state: viewing request is only an enquiry until owner accepts.
- Show an explicit safety warning before any direct payment discussion; Thikana does not collect rent/deposits in the MVP.
