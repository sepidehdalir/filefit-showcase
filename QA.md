# Pre-submission QA — September 27, 2026

**Not released or submitted.** Pixmere is a provisional consumer name; FileFit remains the internal engineering identity. The exact-fit P icon is user-approved and locked. TestFlight is deferred.

## Verified engineering evidence

- **Minimum supported OS tested:** iOS17.0 on an iPhone SE3 simulator. Twenty unit tests passed, including six local StoreKit scenarios. All six UI scenarios have passing targeted results, including native Photos import/save and Files export/reimport.
- **Native device:** iPhone 17 Pro Max on iOS26.1 passed launch/lifecycle, conversion/share and detail-preview checks across targeted runs. Seven real camera JPEG/HEIC files each produced exactly 600×600 JPEG outputs below 100,000 bytes. A 10,514,729-byte source produced a 99,889-byte output.
- **Photo corpus:** 24 public photographic files, including 16 annotated orientation variants, exercised 120 byte/dimension/format cases using the unchanged production engine. A derived photographic transparent PNG added five cases. All passed. Source camera/location metadata was absent in outputs; basic ImageIO color/dimension fields remain. PNG retained transparent corners; JPEG flattened them to white.
- **Visual review:** nature, interior, HDR, macro and orientation comparisons retained recognizable detail without obvious tinting at the tested limits. This is not a guarantee that every low-byte image preserves readable fine text or faces.
- **Accessibility:** light/dark contrast checks and small-screen largest Dynamic Type conversion/paywall tests passed. Explicit outcome focus and purchase-status announcements are implemented. Spoken VoiceOver remains a human acceptance gate.
- **Commerce:** local StoreKit tests cover unavailable products, purchase/cancel/failure/pending/approval, restore, ownership reload, refund and simulated product-lookup failure while owned. Paywall uses the loaded StoreKit display price. These tests do not validate a live App Store product.
- **Release packaging:** a development-signed Release 1.0.0 (1) archive passed local signature checks and was installed/launched on a physical phone. No debug fixture or local StoreKit configuration is bundled. The locked 1024 px icon, metadata lengths and screenshot formats pass scripted checks.

Some initial UI runs failed because system selectors differed on iOS17, an accessibility service reported an invalid process, or a tap did not navigate. Harness corrections and isolated retests passed; no combined initial run is represented as all-green. Physical-device recordings, signing data and original photo corpus are not published.

The public photo corpus is attributed to [ianare/exif-samples contributors](https://github.com/ianare/exif-samples/tree/5332a9cf0220e9c6c93f88a187daa90808051e10). Source files and derivatives remain outside this repository.

## Still required before shipping

Human checks: spoken VoiceOver, actual provider/denied-permission flows, user-photo/face/document quality, large-camera stress and physical keyboard/rotation acceptance. Account checks: final name reservation, production identifiers/signing, real sandbox purchasing/offline ownership, App Store disclosures, distribution validation and submission approval. No App Store URL, market demand, revenue or production commerce is claimed.

The final CI baseline passed all 20 unit tests and five UI scenarios. A Files-picker harness issue on iOS 18 was corrected by explicitly selecting the saved location and querying its remote Browse control directly. The focused CI retry passed export, an empty relaunch and actual 600×600 reimport. These are separate passing evidence sets, not a rewritten all-green initial run. Production app code was unchanged by the test-navigation corrections.
