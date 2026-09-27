# QA milestone — September 26, 2026

This is pre-release engineering evidence. No App Store submission or production purchase is claimed.

- **19 unit tests passed** on iOS 26.2 simulator, including the image engine, storage, workspace and five local StoreKit scenarios.
- The deterministic image suite includes **48 generated cases**, all eight orientations, alpha, HEIC, exact/max dimensions, impossible byte targets and a separate 24 MP input.
- **Five small-screen UI tests passed**, covering the free flow, native sharing, lifecycle, targeted accessibility, Photos import and saving, and Files export.
- Separate large-screen conversion/share, full-size preview, and Dark Mode at the largest accessibility text size passed.
- A native Files export was checked byte-for-byte against the verified output: 63,894 bytes, 600 × 600 JPEG.
- A physical iPhone passed 14 core tests and the conversion/share UI flow. The full physical UI run was interrupted and requires repetition; it is not marked fully verified.
- A development-signed iPhone-only Release archive built and passed local signature verification. It has not been validated for App Store distribution.

These results come from separate runs. Earlier checks caught and resolved a Photos callback concurrency crash, missing result-screen feedback, contrast/clipping issues and an asynchronous StoreKit test assertion. The final unit rerun and simulator UI runs passed after those corrections.

Remaining release gates include real sandbox/TestFlight commerce, older-OS compatibility, a real-camera/document legibility corpus, complete VoiceOver navigation, denied-permission checks, external Files providers and uninterrupted physical-device testing. The contrast audit covers stable first/result screens; native scroll-edge material limits automated contrast interpretation on scrolled content.

Synthetic fixtures are reproducible engineering tests, not user validation, portal certification or proof of market demand.

## Naming correction — 2026-09-26

Consumer naming has been reopened. FileFit is the engineering codename. Previous branded screenshots are withdrawn from this showcase, and the earlier signed archive is historical evidence only. New release artwork and a fresh archive are required after naming is resolved. The neutral development bundle builds and all five local StoreKit tests pass after the development product ID change. No production purchase migration or release is claimed.

The post-correction conversion/result/share UI test also passed. Current README images are unchanged attachments from that simulator test, visually inspected; they show the engineering codename and synthetic test artwork.

## Provisional Pixmere identity — September 27, 2026

The user selected Pixmere provisionally while retaining FileFit engineering/repository names. Five initial directions were followed by four focused refinements to remove paper/PDF associations. The recommended exact-fit P was reviewed at 1024, 60 and 40 px. The working UI and paywall use the same mark with emerald, ivory and sage. These are qualitative design judgments, not measured conversion results. No name clearance or reservation is claimed.

All 19 unit tests passed after branding. All six simulator UI scenarios have passing evidence across separate runs, including the real localized StoreKit test price, conversion/share, preview, Photos import/save, Files export and targeted accessibility/lifecycle checks. The Photos permission test race was fixed; an infrastructure accessibility error passed on isolated retry. This is not a claim that every intermediate run was green. A fresh development-signed archive built and passed local signature verification; the first Pixmere archive installed and launched on the connected phone. The updated physical test run remains blocked by device lock. App Store Connect login is unavailable, so account configuration, real sandbox purchases, distribution validation and name reservation remain open.

Two additional small-screen UI checks passed on iPhone SE (3rd generation), iOS 26.2, Dark Mode with the largest accessibility text size. The first screen and paywall were visually inspected. This is targeted accessibility evidence, not a complete spoken VoiceOver audit.

The final retained Pixmere archive, including the paywall layout refinement, was also installed successfully on the connected iPhone on September 27. Physical test execution remains a separate outstanding gate.

## Exact-fit refinement — September 27, 2026

D replaces the earlier paper-fold P as the provisional working recommendation. The four focused simulator UI checks passed together after the asset update: accessibility/lifecycle, localized paywall, conversion/share and detail preview. Real captures and App Store compositions were regenerated and visually inspected. The installed simulator Home Screen confirms the new icon under the iOS mask. The prior development archive contains the older fold and is not evidence for this asset revision. No final icon approval or App Store release is claimed.

The preceding source revision also passed [GitHub CI](https://github.com/sepidehdalir/filefit-ios/actions/runs/36303996013); this is distinct from the local asset-refinement validation.

The exact-fit revision also passed two targeted small-screen Dark Mode checks at the largest accessibility text size; the first screen and paywall were visually inspected.
