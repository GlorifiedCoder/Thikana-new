# User Flows — Thikana

## 1. First-time renter (guest)

1. Open app.
2. See a brief welcome/search screen; no mandatory login.
3. Select or search a city/area (or continue to all Bangladesh).
4. Choose a category: flat, house, room/sublet, hostel/seat, shop, office, etc.
5. Enter budget and optional property requirements.
6. View results; sort/filter and switch to approximate map if available.
7. Open listing detail and inspect monthly rent, recurring charges, photos, availability confirmation date, verification badges, lister profile, and safety information.
8. Save requires sign-in; contact action follows owner's consent and platform rate limits.
9. Contact lister by available call/WhatsApp/enquiry option.
10. Visit property and independently verify owner authority, actual condition and terms before any payment or agreement.

## 2. Returning renter

1. Restore preferred language, theme, last selected city/area and recent search filters.
2. Open saved listings and saved searches.
3. View new matching listings and only those with current availability status.
4. Compare listing dates and verification detail.
5. Contact lister or submit a viewing request.
6. Report inaccurate listing if necessary.

## 3. Owner creates a listing

1. Tap Post a Property.
2. Sign in with Google/Apple or supported account method.
3. Verify mobile number through OTP.
4. Choose "I am the owner" or "I am an authorized agent/property manager".
5. Choose residential/commercial type and subcategory.
6. Enter title, description, location, approximate public map point and optional exact address (private by default).
7. Enter category-specific attributes: size, rooms, bathrooms, floor, furnishing, access, amenities, facilities, business-use suitability.
8. Enter monthly rent and recurring charges with explicit inclusion/exclusion.
9. Advance/deposit/upfront amounts must follow a legally reviewed form/policy; do not default or suggest a particular amount.
10. Add original/authorized photos; system compresses images and strips EXIF metadata.
11. Confirm the property is genuinely available and the lister has authority to advertise it.
12. Preview and submit.
13. Listing enters pending review. The owner can see review status and any required correction.
14. After approval, listing appears in public search.
15. Owner receives enquiries and can edit, pause, confirm availability, or mark rented/unavailable.

## 4. Authorized agent creates a listing

1. Sign in and verify mobile.
2. Select agent/property manager role.
3. Declare authorization to represent the owner.
4. Submit required evidence if requested by risk level.
5. Create listing and specify owner contact/authority appropriately.
6. Platform review checks for duplicate or unauthorized property/photos.
7. Listing is published with accurate "posted by agent" role and the exact verification level achieved.

## 5. Listing refresh and expiry

1. System reminds lister to confirm availability on a defined schedule.
2. Lister selects Available, Temporarily unavailable, Rented, or Needs edit.
3. If available, record `last_availability_confirmed_at` and extend the listing's freshness window.
4. If no response by expiry, automatically mark the listing expired/hidden.
5. Seeker sees a clear "last confirmed" date and does not confuse a stale ad with current availability.
6. Owner can renew after reconfirmation; if content changed materially, send back for review.

## 6. Contact and viewing

1. Seeker selects Call, WhatsApp, or Request Viewing (depending on owner settings).
2. Reveal action displays a privacy/safety reminder and is rate-limited.
3. Viewing request shows selected date/time and makes clear it is a request, not a booking or reservation.
4. Owner accepts, declines, or proposes another time.
5. Both parties receive notification.
6. Do not accept payments or deposits through the request flow.

## 7. Report and moderation

1. User selects Report Listing or Report User.
2. Choose reason: already rented, fake/duplicate, wrong price, wrong area/address, unauthorized photos, misleading details, scam/payment request, harassment, discriminatory/illegal content, other.
3. Add optional explanation/evidence.
4. Report is assigned a case ID and enters admin queue.
5. Moderator reviews listing and related history; may hide, suspend, request edits, reject, or restore it.
6. Reporter receives status update when appropriate.
7. Actions, reasons and moderator identity are audit logged.

## 8. Admin/operator

1. Admin authenticates with a separately protected role.
2. Open queues for new listings, suspicious listings, reports and verification requests.
3. Review photos, duplicates, owner/agent declarations, availability and content policy.
4. Approve, reject, hide, suspend, or request changes with reason.
5. Review user appeal/support cases.
6. Resolve account deletion requests and data rights requests.
7. Inspect audit trail and system health.
8. Never use a client-controlled user metadata field as proof of admin role.

## 9. Account deletion

1. User opens Settings → Privacy → Delete Account.
2. Explain consequences: profile, saved listings/searches, contact details, messages/enquiries where applicable, and owned listings.
3. Ask for confirmation and re-authentication if needed.
4. Handle active listings: hide/unpublish immediately; preserve only records required by applicable law or legitimate dispute obligations.
5. Delete/anonymize remaining personal data according to approved retention policy.
6. Revoke provider sessions/tokens as required.
7. Provide completion/status message and an external web deletion request route for store compliance where required.

## 10. Error, cancellation, recovery

- Network unavailable: preserve draft and retry upload.
- Photo upload fails: retry individual file; do not lose form.
- OTP invalid/expired/rate-limited: explain and offer resend after cooldown.
- OAuth cancelled: return safely without creating duplicate account.
- Listing rejected: display reason and edit/resubmit path.
- Listing expires: allow reconfirm or archive.
- Viewing cancelled: notify both sides.
- Report submission fails: preserve report draft and retry.
- Unauthorized account action: deny and log; never trust supplied owner ID.
