# Website release notes

Prepared from the OweTally source on 10 September 2026. Only the two store availability cards contain pre-release copy. Add verified store links once published.

## URLs after deployment

- App: https://moenish.dev/OweTally/
- Privacy policy: https://moenish.dev/OweTally/privacy/
- Terms: https://moenish.dev/OweTally/terms/
- Support and deletion: https://moenish.dev/OweTally/support/

## Before the app release

- Add https://moenish.dev/OweTally/privacy/ in Play Console. The updated app source has Settings → About → Privacy policy, which opens this URL in an external browser; rebuild the app to include it.
- Review support retention wording and provider details against actual handling of moenish.dev@gmail.com. The policies reflect the inspected implementation; the publisher is an individual based in Romania, using the personal developer account previously confirmed. OweTally is completely free, with no ads, subscriptions, or in-app purchases.
- Complete Play Console Data safety for the final release binary and all included SDKs. Local-only processing is not the same as transmitting data off-device; evaluate user-directed sharing and backups under the form's definitions.
- No OweTally account-creation feature was found. The support page explains local deletion rather than claiming to offer server-side account deletion.
- Check target audience, app-access instructions, content rating, and any applicable financial-features declaration in Play Console separately.
- Review the final merged Android manifest and device backup behavior. The source does not opt out of OS backups, so the policy explicitly allows for them.
- Privacy and terms must be updated if ads, analytics, cloud services, accounts, contact import, or other data handling are added.

## Evidence checked

pubspec.yaml; Android main manifest and MainActivity; iOS Info.plist; database tables; settings and backup repository; receipt picker; sharing UI. The README has outdated roadmap items (including CSV/contact import); site copy follows implemented features instead.

## Sources

- https://support.google.com/googleplay/android-developer/answer/10144311
- https://support.google.com/googleplay/android-developer/answer/10787469
- https://developer.android.com/identity/data/autobackup
- https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement

## Local preview

Run `python -m http.server 8080` from this repository and open http://localhost:8080/. Root-relative links require an HTTP server.

## Review on 10 September 2026

- Public HTTPS checks: root, app, privacy, terms, support, and CSS returned 200. The GitHub Pages root redirects to moenish.dev. No Set-Cookie header appeared in those responses.
- Existing Android release manifest (built 9 September 2026): no INTERNET, contacts, location, camera, broad storage, or advertising-ID permissions. Recheck the final rebuilt release; this is evidence for the inspected build only.
- No app accounts, backend, analytics, advertising, or crash-reporting SDK integration found in inspected source and direct dependencies. Sharing, external viewers, unencrypted exports, and OS backups remain disclosed.
- Added a separate website/contact privacy notice, linked throughout, with controller identity, purposes, legal basis, voluntary provision, provider transfers, retention criteria, and rights.
- No placeholder contact details or policy boilerplate tokens remain in rendered pages; only store availability remains unfinished.
- Review is not a legal certification: Romania and completely free distribution are confirmed; personal publishing follows the account context. Actual support retention and any applicable commercial-provider disclosures still need to match practice. Do not invent or publish a home address from unrelated sources.
- The app now links to the full online policy through a dedicated Settings entry, with a selectable URL if browser launch fails. The labels are localized in English, Hungarian, and Romanian. This uses url_launcher; recheck the rebuilt final manifest and release binary.

## Romanian publisher details

- Country: Romania. Publisher: Moenish, publishing personally as Moenish.
- Completely free app; no ads, subscriptions, or in-app purchases.
- Privacy notices identify ANSPDCP and preserve the right to approach another competent authority.
- Romanian Law 365/2002 Articles 1 and 5 govern covered information-society services and provider disclosures, including a domicile/registered address. Free pricing alone does not establish whether an activity is outside the law: indirect economic benefit can matter. No commercial status or address exemption is asserted on the website. Reassess if this becomes a business or commercially promotional activity; do not publish a personal address without confirming applicability.
- Official sources: https://legislatie.just.ro/Public/DetaliiDocument/153252 and https://dataprotection.ro/?lang=ro&page=Plangeri_meniu
