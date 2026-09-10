# Website release notes

Prepared from the OweTally source on 10 September 2026. The app is described as preparing for release; add a verified store link once it is live.

## URLs after deployment

- App: https://moenish.github.io/OweTally/
- Privacy policy: https://moenish.github.io/OweTally/privacy/
- Terms: https://moenish.github.io/OweTally/terms/
- Support and deletion: https://moenish.github.io/OweTally/support/

## Before the app release

- Add the privacy policy URL in Play Console and a working link or policy text inside the app. The current app Settings/About does not expose it.
- Review support retention wording and provider details against actual handling of moenish.dev@gmail.com. These pages are a draft based on source code, not a jurisdiction-specific legal review.
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
