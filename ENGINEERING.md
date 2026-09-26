# Engineering decisions

## Verify the artifact, not the intent

A compression setting is not a byte count. The engine encodes a candidate, decodes that candidate, confirms its actual format and dimensions, and compares its exact Data count to the requested maximum. Only a verified result may be exported. A “pass” is deliberately limited to these constraints and never promises acceptance by a website.

## Distinguish maximum dimensions from exact dimensions

Aspect-preserving fit may reduce dimensions to satisfy bytes. Exact crop and pad must keep their canvas size; if encoding cannot satisfy the remaining byte constraint at the quality floor, the operation fails with useful alternatives. PNG is lossless, so it cannot be treated as a JPEG-quality slider.

## Do not assume encoder monotonicity

JPEG candidates are searched in descending discrete quality steps, down to a documented floor. The algorithm prioritizes detail at the chosen dimensions before reducing flexible dimensions. This produces a practical bounded strategy without claiming a globally optimal perceptual result. Text readability remains a human preview decision.

## Bound memory and cancellation

Source bytes, megapixels, decoded long edge, output pixels and batch count are bounded. Decode orientation is applied by ImageIO thumbnail transformation. Each queue item finishes independently; cancellation and backgrounding stop subsequent work. The original is never an output destination.

## Paid access is a verified transaction state

A preferences flag is not purchase evidence. Lifetime access is derived from StoreKit's verified current entitlements; transaction updates handle approval and revocation. Product-fetch failure does not create a purchase or erase a separately verified entitlement. Local StoreKit tests and production sandbox tests are different evidence classes.

## Commercial and engineering honesty

No backend is needed for the core task. Typed analytics default to no-op, so there is no invented central activation funnel. Store positioning and proposed pricing are hypotheses. Accessibility, simulator testing, physical-device behavior, purchase-account setup and App Store release are tracked independently.
