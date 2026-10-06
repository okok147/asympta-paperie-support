# App Review Notes Template — Asympta Paperie

Current production-candidate notes. Re-verify the exact submitted build before submission.

---

Asympta Paperie is a handwriting notebook for iPhone and iPad.

No account or sign-in is required to use the core app.

## Lifetime In-App Purchase

Product: **Paperie Lifetime**
Type: **Non-Consumable**

The free experience includes 2 notebooks. Lifetime is a one-time purchase that unlocks unlimited notebooks. It is not a subscription and does not auto-renew.

To review the purchase:

1. Launch Paperie.
2. Open **Notebooks / 我的筆記本**.
3. If only one notebook exists, choose **New notebook / 新增筆記本** and create the second free notebook.
4. Choose **New notebook / 新增筆記本** again. The **Paperie Lifetime** sheet appears before notebook 3 is created.
5. Select **Unlock Lifetime / 解鎖終身版**. The purchase sheet is presented by StoreKit.
6. After a successful verified transaction, unlimited notebooks are available immediately.

To restore a previous purchase:

1. Follow the same path to the **Paperie Lifetime** sheet.
2. Select **Restore Purchases / 恢復購買**.
3. Paperie calls AppStore.sync(), refreshes the current entitlement, and updates the UI.

No external payment mechanism is used for this digital unlock.

## iCloud

Paperie is local-first. Notebook data is saved to local SQLite before any cloud work. When the user's iCloud account is available, Paperie uses the private CloudKit database to synchronize the notebook library snapshot, including pages, PencilKit drawings, typed text, stamps, stickers, cover appearance, and paper settings. The Page menu shows a quiet sync state and a **Sync now / 立即同步** retry action.

The app remains usable when iCloud is unavailable. Divergent edits use a three-way merge; conflicting remote pages are preserved as recovered pages instead of silently replacing local handwriting.

## Permissions

- **Photos:** Paperie uses Apple's system PhotosPicker only when the user explicitly chooses an image for personal stationery. It does not request broad photo-library access.
- **iCloud:** CloudKit uses the user's Apple iCloud account for private database synchronization. No Paperie account or sign-in is required.
- No advertising, tracking, microphone, camera, location, contacts, or health permission is used by the current build.

## Review contact

Support: hello@everformlab.com
Support URL: https://okok147.github.io/asympta-paperie-support/
Privacy Policy: https://okok147.github.io/asympta-paperie-support/privacy/

---

Before submission, verify these paths once more on the exact submitted TestFlight/App Store build. No private reviewer credentials are required.
