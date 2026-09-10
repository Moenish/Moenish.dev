# Website release notes

Prepared from the OweTally source on 10 September 2026. Only the two store availability cards contain pre-release copy. Add verified store links once published.

## URLs after deployment

- App: https://moenish.dev/OweTally/
- Privacy policy: https://moenish.dev/OweTally/privacy/
- Terms: https://moenish.dev/OweTally/terms/
- Support and deletion: https://moenish.dev/OweTally/support/

## Before the app release

- Add the privacy policy URL in Play Console and a working link or policy text inside the app. The current app Settings/About does not expose it.
- Review support retention wording and provider details against actual handling of moenish.dev@gmail.com. The policies reflect the inspected implementation; country-specific provider disclosures still require the publisher’s country and individual/business status.
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
- Review is not a legal certification: publisher country, business/trader status, monetization, actual support retention, and any required service address must be confirmed. Do not invent or publish a home address from unrelated sources.
- Do not mistake the general app About privacy summary for a complete policy: the app still needs a working policy link or full text before release.
