# FileFit privacy policy
Effective draft: September 26, 2026. Applicable to version 1.0.0. This is a published pre-release draft; final developer-identity and distribution review remain release gates.

FileFit processes images on your device. The app does not operate an image-upload service, require an account, include advertising SDKs, or transmit analytics events. We do not collect your photos, filenames, presets or location.

When you use Photos, Apple's system picker supplies only the images you choose. Save to Photos requests add-only permission to create a new copy. Files access is limited to items you choose in the system picker. Originals are not modified.

New outputs are rendered as sRGB still images and encoded without the source metadata dictionaries. Source EXIF, GPS and IPTC metadata is not copied. Color-profile and basic encoder information may be written. HEIC auxiliary information and Live Photo motion are not preserved. JPEG replaces transparent areas with white; PNG retains transparency. Metadata removal does not remove information visibly present in the image itself.

Images and prepared files are held in memory and the application's temporary directory during use. Temporary exports are removed when you prepare another batch or on the next fresh app launch; system temporary-file management may also remove them. If a preset file is corrupt, saving a new preset keeps a local recovery copy until the app is deleted. Saved constraint presets are stored in Application Support with file protection and may be included in your system device backup. Delete presets within the app; deleting the app removes its local data, subject to Apple's backup behavior. Exports you save elsewhere remain under your control.

Apple processes purchases and provides verified purchase entitlements. FileFit does not receive payment-card details. Apple may provide aggregate App Store analytics and diagnostic information according to your device and account settings. There is no third-party analytics or tracking SDK in the app.

When you share or export a file, the destination you select receives that file and applies its own practices. Sharing destinations or Photos may re-encode images, so the exported copy's verified byte count need not describe a later transformed copy.

For support, use the published support page linked from the App Store listing. Do not submit sensitive photos or documents in public support requests. This policy must be reviewed with the final distribution build and developer identity before launch.
