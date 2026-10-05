# Asympta Paperie — App Review Checklist

Last updated: 2026-10-06

This checklist tracks the public-facing facts Apple Review should see. It must match the shipping app exactly.

## Product

- App: **Asympta Paperie**
- Bundle ID: `com.everformlab.AsymptaPaperie`
- App Store app ID: `6818553101`
- Version: `1.0`
- Default language: Traditional Chinese
- English: selectable in app
- Support URL: https://okok147.github.io/asympta-paperie-support/
- Privacy Policy URL: https://okok147.github.io/asympta-paperie-support/privacy/

## Lifetime purchase

- Product ID: `com.everformlab.AsymptaPaperie.lifetime`
- Type: non-consumable
- Free allowance: **2 notebooks**
- Lifetime unlock: unlimited notebooks
- Creating notebook 3+ opens the Lifetime sheet.
- Price shown in app must come from StoreKit.
- **Restore Purchases** is visible on the Lifetime sheet.
- Existing notebooks remain fully usable if StoreKit is unavailable.
- Existing notebooks are never locked because entitlement cannot be refreshed.

### Reviewer path

1. Launch Asympta Paperie.
2. Open **Notebooks / 筆記本**.
3. Create a second notebook.
4. Open **New notebook / 新增筆記本** again.
5. The **Paperie Lifetime / Paperie 終身版** sheet appears.
6. The sheet contains the App Store localized price and **Restore Purchases / 恢復購買**.

## iCloud

- Local SQLite persistence is canonical for live writing.
- iCloud work happens only after local persistence.
- Paperie uses the user's private CloudKit database.
- No Paperie account is required.
- Offline writing remains available.
- The page-actions area contains human-readable sync state and **Sync now / 立即同步**.
- Conflict handling preserves divergent handwriting instead of silently replacing a page.
- Notebook deletion can synchronize across the user's devices.

## Writing and search

- Apple Pencil strokes remain original PencilKit strokes.
- Fingers navigate by default.
- Finger ink requires explicit **Write / 書寫** mode.
- Pinch zoom changes only the view transform; stored stroke/sticker coordinates do not change.
- Typed text stays searchable even when rendered with the handwritten look.
- On supported system versions, Apple Pencil handwriting search is indexed in the background.
- Search updates while typing; a separate Search confirmation button is not required.

## Data and privacy

The public Privacy Policy must accurately state:

- local-first notebook storage;
- private CloudKit synchronization;
- StoreKit entitlement processing;
- user-selected photo handling;
- support email handling;
- no advertising SDKs or third-party behavioral tracking in the current release;
- retention/deletion behavior;
- conflict-recovery behavior.

If the shipping app changes any of these facts, update the public policy before submission.

## App Store Connect release preparation

- [ ] Final build is `VALID` in App Store Connect.
- [ ] Final build is available to the Internal TestFlight group.
- [ ] Support URL is set on the 1.0 version localization.
- [ ] Privacy Policy URL is set on App Info.
- [ ] App Privacy / nutrition answers match the policy.
- [ ] Encryption declaration matches the binary.
- [ ] Lifetime IAP has English and Traditional Chinese localization.
- [ ] Lifetime IAP has pricing/availability.
- [ ] Lifetime IAP has an App Review screenshot from the actual app.
- [ ] Lifetime IAP is included with the app's review submission when required.
- [ ] Review notes explain Lifetime, Restore Purchases, iCloud, search, and notebook management.
- [ ] Review contact email/phone in App Store Connect are current.
- [ ] Screenshots and app description describe only features in the submitted build.
- [ ] CloudKit production schema is deployed before App Store review.

## Suggested review notes

Asympta Paperie is a local-first digital notebook for iPhone and iPad.

The free experience supports two notebooks. To locate the non-consumable Lifetime IAP, open **Notebooks**, create a second notebook, then choose **New notebook** again. The **Paperie Lifetime** sheet displays the StoreKit-provided local price and includes **Restore Purchases**. Lifetime unlocks unlimited notebooks.

Apple Pencil handwriting remains native PencilKit data. Typed text is searchable, and supported OS versions index Pencil handwriting in the background. Search results appear as the user types.

iCloud synchronization uses the user's private CloudKit database and runs only after local persistence. Offline writing remains available. Sync state and a manual **Sync now** action are available from Page actions.

Notebook rename, cover appearance, default paper, and delete actions are available by long-pressing a notebook in the notebook library. The final remaining notebook cannot be deleted.

No login is required.

## Do not submit if

- Support or Privacy URLs are unreachable.
- Public wording disagrees with the build.
- Lifetime cannot be loaded by the review build.
- Restore Purchases is missing or hidden.
- CloudKit production schema is not deployed.
- A release-gate test is failing.
