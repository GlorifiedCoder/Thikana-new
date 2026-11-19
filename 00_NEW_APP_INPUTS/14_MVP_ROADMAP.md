# Thikana — Recommended MVP Scope and Development Roadmap

## Phase 0 — Owner decisions and validation (before coding)

Deliverables:
- Resolve provisional brand risk.
- Approve rental-only scope.
- Approve pilot market.
- Choose the first property categories.
- Interview a small set of renters, owners and agents.
- Define exact verification badges and evidence.
- Obtain legal review of advance/deposit presentation and data hosting.
- Create a first-party sample listing catalogue; do not use copied listings.
Exit gate: requirements and key assumptions approved.

## Phase 1 — Product, architecture and foundation

Build:
- Flutter Android/iOS project.
- Feature-first modular structure.
- Design system and user's four themes (System, Light Blue, Light Gold, Dark).
- Localization foundation (Bangla/English).
- Navigation and guest experience.
- Supabase Auth integration plan.
- Database ERD, RLS matrix, migrations and storage design.
- Admin authentication/authorization architecture.
- CI and test structure.
- Privacy data inventory and retention design.
Machine A: most code, static checks, model/unit tests.
Machine B: native builds and provider callback testing.
Exit gate: app boots, guest navigation works, migration and security design reviewed.

## Phase 2 — Property catalogue and search

Build:
- Location taxonomy.
- Category taxonomy.
- Listing schema and category-specific validation.
- Search, server-side filters, sort and pagination.
- Detail page and image gallery.
- Saved listing/favorites.
- Approximate map/location architecture.
- Bangla/English location aliases.
Exit gate: users can discover test listings and filters return correct results.

## Phase 3 — Lister posting and listing management

Build:
- Owner/authorized-agent account capabilities.
- Google and Apple authentication.
- Lister mobile OTP.
- Listing wizard and drafts.
- Photo uploads and metadata removal.
- Preview and submit.
- My listings: edit, pause, renew, mark rented.
- Contact and structured enquiry.
Exit gate: owner can submit, manage and close a listing; unauthorized users cannot change it.

## Phase 4 — Trust, freshness and moderation (must precede public UGC launch)

Build:
- Admin web console.
- Listing review queue.
- Report listing/user.
- User block/hide.
- Explicit verification status and audit.
- Duplicate/suspicious listing review.
- Availability confirmation reminders and expiry.
- Scam warning and help centre.
- Support and complaint workflow.
Exit gate: operators can review, respond, remove and restore listings safely; no public launch with unstaffed reports.

## Phase 5 — Notifications and quality improvements

Build:
- Push notifications with optional consent.
- Viewing request accept/decline (if chosen).
- Saved searches and alerts.
- Analytics and crash monitoring after SDK privacy review.
- Performance/image optimization.
- Accessibility and localization polish.
Exit gate: end-to-end journeys and performance targets met.

## Phase 6 — Machine A completion gate

Must complete where possible:
- Dart formatting and analyzer.
- Flutter unit/widget tests.
- Backend tests.
- SQL migration static validation and local/hosted test database checks where safe.
- RLS tests for users, listers, moderators and admins.
- API contract tests.
- Dependency/license/security scans.
- Privacy inventory and SDK inventory.
- App store policy assessment.
- Documentation and README.
- Generate test report with PASS/FAIL/BLOCKED/NOT RUN.
- Record exact Git commit and remaining Machine B tasks.
Do not call the product bug-free; record evidence.

## Phase 7 — Machine B independent review and native build

- OpenCode + DeepSeek V4.1 Flash read-only audit first.
- Review architecture, security, SQL, RLS, OAuth, API, UI and test gaps.
- Approve fixes and keep commits.
- Install Flutter/JDK/Android SDK/build tools/NDK/CMake only as required.
- Build debug/release APK/AAB.
- Run emulator and physical-device tests.
- Verify package identifiers, deep links, Google login, Android permission flows and file uploads.
- Review storage, network, low-memory and slow-network behavior.
- Use macOS/Xcode for iOS build, sign-in, permissions and device testing.
Exit gate: Android and iOS test matrices have actual run evidence; critical/high defects fixed.

## Phase 8 — Legal, store and operational release gate

- Confirm Thikana brand/legal clearance and final app identifiers.
- Legal review of Bangladesh property/rent and personal-data issues.
- Confirm hosting region and international data transfer.
- Publish Privacy Policy, Terms, listing rules, safety policy and contact/support pages.
- Implement account deletion and external deletion website.
- Complete Google Play Data Safety and Apple App Privacy accurately.
- Complete app content/age rating, location/photo permissions and reviewer instructions.
- Create screenshots, icons, metadata and demo accounts.
- Confirm target SDK/Xcode requirements on submission date.
- Signing keys/secrets securely stored.
- Run production smoke tests and rollback plan.
Exit gate: no unresolved release-critical privacy/security/legal/functional issues.

## Phase 9 — Controlled pilot and expansion

- Start with chosen pilot localities.
- Monitor freshness, reports, response rate and listing density.
- Manually audit first cohort of listings.
- Adjust reminder/expiry rules.
- Expand geography/categories when enough active listings and moderation capacity exist.

## Never defer until "testing" only

These must be designed during earlier phases:
- Database ownership and RLS.
- Account deletion/data retention.
- Privacy consent and data inventory.
- UGC reporting/blocking/moderation.
- Lister authority and verification semantics.
- Exact vs approximate location design.
- Listing expiry and stale-state logic.
- Payment/deposit restrictions.
- Data transfer/hosting region decision.
