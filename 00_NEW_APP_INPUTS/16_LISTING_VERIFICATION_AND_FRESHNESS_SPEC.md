# Thikana — Listing Verification and Freshness Specification

## Principle

"Verified" must never be a generic unqualified label. Display the exact check, the date, the method, and what it does not prove.

## Suggested levels

| Badge | Evidence | What it means | What it does NOT mean |
|---|---|---|---|
| Phone confirmed | OTP completed for lister's mobile number | Lister controls that number at verification time | Not identity, ownership or availability proof |
| Identity reviewed | Approved manual/third-party identity process | Identity credential was reviewed | Not proof of property title |
| Owner authorization reviewed | Acceptable owner/agent authority evidence reviewed | Evidence links lister to authority to advertise the property | Not legal title search or guarantee |
| Location visited | Defined field agent visit and dated checklist/photo evidence | A representative visited the stated vicinity/property on date | Not title, structural safety, or ongoing availability |
| Availability reconfirmed | Owner/lister positively confirms availability in app | Availability confirmed by lister on the displayed date | Not a guarantee after that date |
| Listing information updated | Material details refreshed and reviewed | Listing details updated on date | Not independent inspection |

Never display "100% verified", "guaranteed property", or "safe owner" without legally meaningful evidence and an approved scope.

## MVP verification

- Require mobile OTP for listing owners/agents.
- Collect owner vs agent declaration.
- Run listing content/photo checks and manual review for new/suspicious accounts.
- Do not collect NID by default.
- Avoid storing identity or ownership documents until a documented legal basis, secure access, retention period, processor contract, breach process and deletion workflow exist.
- If verification documents are introduced, store them in private restricted storage, not public property image buckets; log every access; redact unnecessary numbers; delete per retention policy.

## Freshness workflow (recommended hypothesis)

- At publish, require explicit availability confirmation.
- Day 14: reminder to reconfirm.
- Day 24: second reminder.
- Day 30 after last positive confirmation: hide/expire from public search if not reconfirmed.
- Owner can mark rented/unavailable immediately; remove from search.
- Every reconfirmation creates immutable timestamped event.
- Rejected/expired listings can be renewed; material edits may trigger moderation.
- Intervals should be configurable and validated with pilot owners.

## Duplicate detection

Signals:
- Same owner phone.
- Near-identical title and description.
- Similar or identical image hashes.
- Same/nearby coordinates and same property features.
- Multiple active records for same building/unit.
Signals trigger a review queue, not automatic accusations or permanent blocking.

## Report reasons

- Already rented / unavailable.
- Fake property / wrong address.
- Wrong rent or hidden charge.
- Inactive or unrelated phone.
- Unauthorized or copied photos.
- Duplicate listing.
- False owner/agent representation.
- Scam, advance/deposit demand or suspicious payment request.
- Discriminatory/illegal content.
- Harassment, threat or abuse.
- Other.

## Moderation service levels

Before launch, assign real staff/owner responsible for:
- reviewing new listings;
- urgent scam/fraud/safety reports;
- normal listing reports;
- identity/authority review;
- appeals;
- account deletion and privacy requests.

Suggested operations: urgent threats/scams triaged quickly; routine listings reviewed on a published service target. Do not promise response times the team cannot meet.
