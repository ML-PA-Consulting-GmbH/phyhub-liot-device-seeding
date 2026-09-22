# Third-party notices

This repository redistributes third-party binary payloads (`.snap` files)
in addition to its own source code. This file records what they are, under
what terms they are redistributed, and how to obtain their source.

Total bundled payload: approximately 685.2 MB across 23 file(s).

## Written offer for source code

For any binary in this repository distributed under the GNU General Public
License or GNU Lesser General Public License, ML!PA Consulting GmbH will provide the
complete corresponding machine-readable source code on request, for a period
of three years from the date of distribution, at no charge beyond the cost of
physically performing the distribution.

Requests: **opensource@ml-pa.com**

Where an upstream source location is listed below, that location provides
equivalent access to the corresponding source and may be used instead.

## Bundled components

### core24

- Publisher: ML!PA Consulting GmbH. This is ML!PA's own build, signed and published through ML!PA's own snap store (`developer-id: appstore` in the snap-revision assertion) — it is not Canonical's stock `core24` artifact, even though it wraps Ubuntu Core 24.04.
- Licence: Believed to still contain Ubuntu Core 24.04-derived packages under GPL-2.0, GPL-3.0, LGPL, MIT, BSD and others, since it is built as a wrapper around that base. Contents were not independently re-verified for this notice (no `.snap` unpacking tool was available) — confirm before publishing.
- Corresponding source: https://archive.ubuntu.com/ubuntu/ (Ubuntu 24.04 source packages) for the inherited Ubuntu content. For ML!PA's own wrapper/build recipe, contact **opensource@ml-pa.com**.
- Note: ML!PA-built base snap wrapping Ubuntu Core 24.04. Likely still contains many packages under differing licences, several of them copyleft, inherited from the Ubuntu base — treat the written offer above as applicable unless ML!PA confirms otherwise.
- Files: 5, approximately 292.2 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/core24_1.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/core24_1.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/core24_1.snap`
  - `phyhub-staging-environment/phyboard-pollux-imx8mp-3/seed/snaps/core24_2.snap`
  - `phyhub-staging-environment/phyboard-segin-imx93-2/seed/snaps/core24_2.snap`

### liot-ota-rauc

- Publisher: ML!PA Consulting GmbH (own build, not third-party)
- Licence: Proprietary - ML!PA Consulting GmbH. Not licensed under the GPL or LGPL, so the written offer above does not apply to this component.
- Corresponding source: not applicable (proprietary, in-house build)
- Files: 3, approximately 16.9 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/liot-ota-rauc_3.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/liot-ota-rauc_3.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/liot-ota-rauc_3.snap`

### m2cp-gateway

- Publisher: ML!PA Consulting GmbH (own build, not third-party)
- Licence: Proprietary - ML!PA Consulting GmbH. Not licensed under the GPL or LGPL, so the written offer above does not apply to this component.
- Corresponding source: not applicable (proprietary, in-house build)
- Files: 5, approximately 33.3 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/m2cp-gateway_1.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/m2cp-gateway_1.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/m2cp-gateway_1.snap`
  - `phyhub-staging-environment/phyboard-pollux-imx8mp-3/seed/snaps/m2cp-gateway_2.snap`
  - `phyhub-staging-environment/phyboard-segin-imx93-2/seed/snaps/m2cp-gateway_2.snap`

### m2cp-message-hub

- Publisher: ML!PA Consulting GmbH (own build, not third-party)
- Licence: Proprietary - ML!PA Consulting GmbH. Not licensed under the GPL or LGPL, so the written offer above does not apply to this component.
- Corresponding source: not applicable (proprietary, in-house build)
- Files: 5, approximately 49.9 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-staging-environment/phyboard-pollux-imx8mp-3/seed/snaps/m2cp-message-hub_4.snap`
  - `phyhub-staging-environment/phyboard-segin-imx93-2/seed/snaps/m2cp-message-hub_4.snap`

### snapd

- Publisher: Canonical Ltd.
- Licence: GPL-3.0-only
- Corresponding source: https://github.com/canonical/snapd
- Note: The snap daemon. Copyleft: the corresponding source must be made available to anyone who receives this binary.
- Files: 5, approximately 292.7 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/snapd_3.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/snapd_3.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/snapd_1.snap`
  - `phyhub-staging-environment/phyboard-pollux-imx8mp-3/seed/snaps/snapd_2.snap`
  - `phyhub-staging-environment/phyboard-segin-imx93-2/seed/snaps/snapd_2.snap`

## Trademarks

Ubuntu and Canonical are registered trademarks of Canonical Ltd. This
repository is not affiliated with or endorsed by Canonical Ltd.

