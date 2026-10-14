# Indiemaps public device previews

Only test PMTiles and manifests are published here. Build code, raw inputs and full audit records remain in the private build repository.

## Southend trial, 12 October 2026

Main manifest (1,544 pins):
https://github.com/kvaak-kvaak/indiemaps-alt-preview/releases/download/southend-2026-10-12-v1/manifest.json

Optional parking manifest (154 pins):
https://github.com/kvaak-kvaak/indiemaps-alt-preview/releases/download/southend-2026-10-12-v1/parking-manifest.json

Both use Vela's `regions` manifest and `places` tile layer. Parking is separate and should default off. Do not use the parking manifest as a replacement for the main source.

This tests map transport and basic cards. Independent search and rich-card integrations remain separate. Do not combine this source with another POI overlay over Southend when assessing duplicates.

See attribution.txt and checksums.json in the release. Tile build was performed in GitHub Actions, with a decode check for all IDs/properties and coordinate quantization under 9 cm.

## Streaming test URLs (CORS-enabled raw hosting)

Main: https://raw.githubusercontent.com/kvaak-kvaak/indiemaps-alt-preview/southend-web-2026-10-12-v1/southend/manifest.json

Optional parking: https://raw.githubusercontent.com/kvaak-kvaak/indiemaps-alt-preview/southend-web-2026-10-12-v1/southend/parking-manifest.json

These small preview files are pinned to an immutable test tag. This is test delivery, not a final large-scale hosting decision.

## Category recovery preview, 13 October 2026

Main manifest: https://raw.githubusercontent.com/kvaak-kvaak/indiemaps-alt-preview/southend-web-2026-10-13-v2/southend/manifest.json

1,622 main-map pins (+78), 154 optional parking pins unchanged. All 2,946 existing reviewed records preserved. Six potential duplicates withheld. Built and decoded in Actions run 38318516993. Previous immutable preview URLs remain available.

## Southend + Helsinki with card details, 13 October 2026

Manifest: https://raw.githubusercontent.com/kvaak-kvaak/indiemaps-alt-preview/cities-web-2026-10-13-v1/manifest.json

Southend: 1,622 map pins; 333 enriched records. Helsinki: 11,075 map pins; 499 enriched records. Each region has a separate version-bound SQLite details download described by `details`. Existing Vela clients ignore this optional field; rich cards require the updated Android reader. Parking remains separate and off by default.

## Corrected Helsinki preview, 14 October 2026

Manifest: https://raw.githubusercontent.com/kvaak-kvaak/indiemaps-alt-preview/cities-web-2026-10-14-v2/manifest.json

Helsinki: 11,102 map pins, 238 optional parking pins, 691 enriched records, 253 places with dated official hours. Southend assets unchanged. Built and decoded in Actions run 38590350115. Matching conflicts remain held. Updated Android client renders dated hours; visual phone testing remains outstanding. Earlier immutable preview tags remain available for rollback.
