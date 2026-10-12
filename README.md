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
