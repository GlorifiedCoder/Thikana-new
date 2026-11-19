# Thikana — Bangladesh Legal, Rental and Privacy Research

**Research snapshot:** 20 November 2026  
**Important:** This is product/engineering research, not legal advice. Engage a Bangladesh lawyer before public launch and before accepting money, processing identity documents, generating tenancy contracts, or choosing a foreign production database region.

## 1. Personal Data Protection Act, 2026

The official Laws of Bangladesh site lists the **Personal Data Protection Act, 2026 (Act No. 63 of 2026), dated 10 April 2026**. It repeals the prior 2025 Personal Data Protection Ordinance and 2026 amendment ordinance.

Research-relevant provisions in the official text include:
- Section 5: lawful basis for processing; consent must be free, specific, clear, informed and revocable where consent is used.
- Sections 10–12: data subject rights and access/correction (review exact applicable rules).
- Section 16: restrictions on disclosing personal data for purposes other than the collection purpose without consent, subject to the Act.
- Section 17: technical and organizational safeguards; confidentiality, integrity, availability, encryption/pseudonymisation, risk review and regular testing are mentioned.
- Section 18: retention should not exceed the applicable period/purpose except as provided.
- Section 19: recordkeeping obligations appear in the text.
- Section 22: data protection planning.
- Section 29: transfer of classified personal data outside Bangladesh is subject to specified conditions, including consent/contract and conditions about suitable technology/locations; sensitive large-scale transfers have additional notification provisions.
- Section 1 says most provisions are deemed effective from 6 November 2025, while sections 23 and 31–35 have a delayed commencement mechanism tied to a later government gazette notification after the specified period.

### Product implications

1. Build a data inventory before choosing hosting and SDKs.
2. Explain purpose, duration, transfer, and withdrawal where consent is used.
3. Collect only necessary information.
4. Provide access/correction/deletion workflows appropriate to law.
5. Create retention schedules for accounts, listings, reports, messages, logs and verification records.
6. Use encryption, RLS, access logging, backups and tested incident recovery.
7. Review every processor, SDK, auth provider, maps provider, SMS provider, email provider, analytics provider and cloud region.
8. Do not assume Supabase Singapore or another foreign region is automatically permissible. The exact transfer conditions, approved destinations, implementing rules, contractual safeguards and applicability should be reviewed by local counsel before production personal data is stored.
9. Do not collect NID, biometrics, identity documents, or exact user GPS by default.
10. Treat mobile number, location and online identifiers as personal data.

## 2. House Rent Control Act, 1991

The official text's definition of "house" includes a building or part of a building intended to be rented for residential or non-residential or both purposes.

Section 10 (as published in the official Bengali text) restricts:
- demanding/receiving premium, salami, security deposit or similar money over rent for letting/renewal/extension;
- demanding/receiving more than one month's rent as advance without prior approval of the Controller.

Section 11 contains a statutory exception for a particular long-term development lease scenario. Section 13 concerns providing a signed receipt when rent is paid. Section 14 concerns refunds of certain amounts prohibited by the Act.

### Product implications

- Do not build a "recommended deposit" calculator.
- Do not imply that an advance/security amount is lawful because an advertiser entered it.
- Do not collect or route rent, advance, salami or deposit in MVP.
- Obtain a Bangladesh lawyer's written view on whether and how listing fields may display advertiser-stated upfront amounts and how section 10 applies to each residential/commercial category.
- If an upfront amount is shown after legal approval, label it as advertiser-provided, show the legal disclaimer without suggesting the platform validates legality, and provide report support.
- Do not provide legal advice or generate lease terms in the MVP.

## 3. Transfer of Property Act, 1882

Section 107 states that a lease of immovable property from year to year, for a term exceeding one year, or reserving yearly rent can be made only by a registered instrument; other leases may be made by registered instrument or oral agreement accompanied by delivery of possession, subject to law and exceptions.

Product implications:
- A viewing request is not a lease/booking.
- The app should not say that clicking "contact" or "request viewing" forms a tenancy.
- Defer lease generation and e-sign until counsel reviews applicable laws, stamping, registration and signature validity.
- Display an educational reminder that users should review terms and execute the legally appropriate agreement.

## 4. Consumer and digital commerce

- Bangladesh Government Press lists the Digital Commerce Operation Guidelines, 2021 in the 4 July 2021 Extraordinary Gazette (Ministry of Commerce).
- Dhaka Tribune reported on 26 October 2026 that the Ministry published a draft amendment to the Consumer Rights Protection Act, 2009 on 30 September 2026, including digital commerce proposals. Reporting says it was put out for 30-day public comments. The draft must not be described as enacted law without checking the latest official gazette.
- The same reporting describes DNCRP concerns around advertiser identity, stale listings and complaint resolution. It does not establish a definitive legal classification of every rental listing intermediary.
- Verify current DBID/business registration and platform obligations with Bangladesh counsel before monetization or launch.
- Public support/contact details, complaint intake, moderation evidence and clear terms should be in product regardless.

## 5. Platform responsibility and disclaimers

Thikana may be a listing intermediary, but should not assume it has zero responsibility just because users own the properties. The platform should:
- remove reported fraudulent or stale listings;
- identify listers and distinguish owners from agents;
- explain the exact scope of checks;
- preserve complaint/audit records;
- give transparent terms and contact support;
- avoid claiming to guarantee title/condition/availability unless independently verified.

Disclaimer language should be reviewed by legal counsel; it does not replace good operational practice.

## 6. Store policy interaction

The app contains UGC (property descriptions, photos, owner/agent profiles, enquiries). Implement filters, reporting, blocking, moderation and support before public launch. Implement account deletion in app and the external deletion route required by relevant store policies where applicable. Complete privacy/data-safety declarations based on actual code and all third-party SDKs, not assumptions.

## 7. Required legal review checklist

- Thikana company/business registration and Digital Commerce/DBID applicability.
- User terms, listing rules, intermediary status and takedown process.
- House Rent Control Act treatment of advance/deposit and commercial listings.
- Property advertising/owner authorization evidence requirements.
- Privacy policy and Personal Data Protection Act 2026 obligations.
- Cross-border data transfers and Supabase region/provider contracts.
- Retention and breach response.
- Consumer complaint and refund obligations if paid products are introduced.
- Payment gateway licensing/escrow rules if platform ever processes real-world payments.
- Trademark clearance and IP rights for logo/name/photos/maps.
