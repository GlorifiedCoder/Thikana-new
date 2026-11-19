# Platform and Constraints — Thikana

## Target platforms

- [x] Flutter Android
- [x] Flutter iOS
- [ ] Public web marketplace for MVP (consider later)
- [x] Internal web admin/moderation console
- [x] Backend/API

## Technology preferences

Recommended baseline:
- Flutter + Dart mobile app (Android and iOS).
- Riverpod for application state (or another justified maintained solution).
- GoRouter for navigation.
- Supabase Auth, PostgreSQL, Storage, RLS.
- Supabase migrations in Git.
- FastAPI as a small, optional service for jobs and privileged server operations where Supabase alone is not a good fit.
- FCM/APNs for push notifications.
- Responsive web admin console, preferably reusing the team's chosen Flutter/web stack if practical.
- GitHub Actions for CI and build artifacts.

Keep architecture modular but do not create microservices for an MVP.

## Machine A / Machine B

Machine A:
- Windows, 4 GB RAM, around 10 GB free storage.
- ZCode already installed.
- Install/use Git, Flutter SDK and Python.
- Do not require Android Studio, Android SDK, NDK, Docker, emulator or local PostgreSQL.
- Write all possible frontend/backend/database/admin code and run static analysis/lightweight tests.
- Use hosted Supabase, but do not deploy production personal data until data residency and legal review are complete.
- Avoid local Android build commands and large caches.

Machine B:
- Install Flutter version pinned by the project, Android Studio or command-line Android SDK, compatible JDK, platform/build tools and only required NDK/CMake.
- Use OpenCode with DeepSeek V4.1 Flash for independent read-only audit first, then approved fixes.
- Build and test on Android emulator and physical Android devices.
- Install Supabase CLI/Docker only if local Supabase or local service containers are justified.
- For iOS actual build/sign/test: macOS with Xcode, iOS Simulator and real iPhone.

## Offline / connectivity

Online-first. Property browsing, image upload, authentication and messaging/enquiries require network.

Provide:
- Cached recent search results/listing details for graceful browsing where appropriate.
- Draft persistence during weak connectivity.
- Resumable/retryable photo uploads.
- Clear stale-data labels; never imply cached availability is current.
- No offline creation/publishing success claim before server confirmation.

## Localization and accessibility

- Bangla and English.
- Bangla should be the default recommendation for the Bangladesh pilot; user can switch to English.
- Unicode-safe Bengali search, sort and display; test common Android Bengali fonts.
- BDT (৳) formatting.
- Asia/Dhaka timezone.
- Area in square feet; consider Bangladeshi local units only if validated with users.
- Accessible contrast, text scaling, screen-reader labels, keyboard navigation for admin, clear touch targets.

## Location and maps

- Use a curated, versioned Bangladesh location hierarchy for filters, not only map-provider free text.
- Support English/Bengali names, alternate spellings and transliteration aliases.
- Store precise coordinates privately only where necessary; public map pins should be approximate by default.
- No background location.
- Request device location only when user chooses "near me".
- Owner should be able to select the approximate property pin.
- Evaluate Google Maps SDK and alternative map providers. Check current Bangladesh-specific pricing, billing, attribution, caching, API-key restrictions and provider terms before selecting.
- Never use unauthorized scraping of map services.

## Privacy and legal constraints

Bangladesh Personal Data Protection Act, 2026 (Act 63 of 2026) is now listed on the official Laws of Bangladesh site. Its provisions include lawful processing/consent, data subject rights, confidentiality, security, retention and cross-border transfer. Because Supabase region and third-party provider locations may be outside Bangladesh, cross-border data transfer must be assessed before production personal data is stored. See `17_BANGLADESH_LEGAL_AND_PRIVACY_RESEARCH.md`.

House Rent Control Act, 1991 includes restrictions around premium/salami/security or similar payments and advance rent. Do not build deposit collection, rent collection or legal contract flows without Bangladesh legal review.

## Budget assumptions

Unknown. Keep costs low in development:
- Free/basic listings in MVP.
- Free browsing and contact.
- Minimize map API calls and image storage.
- Avoid expensive identity verification vendors at MVP.
- Avoid AI inference until the core marketplace data and listing quality justify it.
- Provide cost estimates for Supabase, storage, SMS, maps, notifications and hosting before production rollout.

## Reliability/performance expectations

- Fast first screen on mid-range Android phones.
- Efficient compressed images and thumbnails.
- Server-side filtering/pagination; never download all listings to client.
- Indexed queries for location, rent, category, status and availability.
- Rate limits for OTP, contact reveal, reports and listing creation.
- Crash/error monitoring with privacy-reviewed SDKs.
