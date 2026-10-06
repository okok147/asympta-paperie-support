# Asympta Paperie — App Store Review Checklist

Last official-document review: **2026-10-06**

This is a release gate for the App Store version that includes a **Lifetime** unlock.

## Public URLs

- Support: https://okok147.github.io/asympta-paperie-support/
- Privacy Policy: https://okok147.github.io/asympta-paperie-support/privacy/
- Source repository: https://github.com/okok147/asympta-paperie-support

## P0 — must be true before submission

- [x] GitHub Pages is published and both public URLs return HTTP 200 without login. Verified 2026-10-06.
- [x] Support page contains public support contact information (hello@everformlab.com).
- [x] Privacy Policy describes the current production candidate behavior.
- [x] The app contains an easily accessible Privacy Policy link in the Page menu.
- [x] The app contains a Support link in the Page menu.
- [ ] Paid Apps Agreement is active in App Store Connect.
- [ ] Required tax information is complete.
- [ ] Required banking information is complete.
- [x] Lifetime IAP exists as **Non-Consumable**.
- [x] Lifetime IAP has en-US + zh-Hant localizations and a final base price.
- [ ] Lifetime IAP has an App Review screenshot and Review Notes.
- [ ] The first Non-Consumable IAP is added to the **same App Review submission as the new app version**.
- [x] Reviewer can reach Lifetime from Notebooks → New notebook after two free notebooks exist.
- [x] StoreKit returns and displays the localized price; no storefront price is hard-coded.
- [ ] Decide deliberately whether Lifetime should use Family Sharing **before enabling it**. Apple says Family Sharing for an IAP cannot be turned off after it is enabled.
- [ ] Successful purchase unlocks Lifetime immediately.
- [ ] Cancelled, failed, and pending purchases do not falsely unlock Lifetime.
- [x] A visible **Restore Purchases** action exists on the Lifetime sheet and refreshes StoreKit entitlement state.
- [x] Free users can create and use 2 notebooks without purchasing.
- [ ] App Store screenshots/description make paid-only features clear.
- [ ] Correct release build is selected.
- [ ] App Privacy answers match the shipping code and this Privacy Policy.
- [x] Privacy manifest is bundled; current source audit found app-owned UserDefaults as the required-reason API and declares CA92.1.
- [ ] Third-party SDK privacy-manifest/signature requirements pass.
- [ ] Fresh-install, offline, iCloud-unavailable, and StoreKit-unavailable paths do not crash.
- [ ] Physical iPhone test passes.
- [ ] Physical iPad + Apple Pencil test passes.
- [ ] Notebook create/open/rename/delete and persistence pass.
- [ ] Background/foreground and termination/relaunch persistence pass.
- [ ] iCloud synchronization and conflict/recovery behavior pass.
- [ ] Lifetime purchase and restore pass in StoreKit/Sandbox testing.

## App Store Connect fields

### App version

Support URL:
`https://okok147.github.io/asympta-paperie-support/`

### App Privacy

Privacy Policy URL:
`https://okok147.github.io/asympta-paperie-support/privacy/`

### IAP type

`Non-Consumable`

Suggested customer-facing name:
`Paperie Lifetime`

Suggested short description:
`One-time unlock for unlimited notebooks.`

## Suggested App Review Notes

See `REVIEW_NOTES_TEMPLATE.md`.

## Apple references

- App Review Guidelines: https://developer.apple.com/app-store/review/guidelines/
- Submit an In-App Purchase: https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/submit-an-in-app-purchase
- IAP review information: https://developer.apple.com/help/app-store-connect/manage-in-app-purchases/view-and-edit-in-app-purchase-information
- App privacy: https://developer.apple.com/help/app-store-connect/manage-app-information/manage-app-privacy
- App version information / Support URL: https://developer.apple.com/help/app-store-connect/reference/app-information/platform-version-information
- Paid Apps Agreement: https://developer.apple.com/help/app-store-connect/manage-agreements/sign-and-update-agreements
- Required-reason APIs: https://developer.apple.com/documentation/bundleresources/describing-use-of-required-reason-api
- Third-party SDK requirements: https://developer.apple.com/support/third-party-SDK-requirements/
- Family Sharing for IAP: https://developer.apple.com/help/app-store-connect/configure-in-app-purchase-settings/turn-on-family-sharing-for-in-app-purchases
- App privacy details: https://developer.apple.com/app-store/app-privacy-details/
