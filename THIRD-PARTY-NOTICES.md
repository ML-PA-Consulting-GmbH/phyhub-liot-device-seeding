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
- Licence: Wraps Canonical's Ubuntu Core 24.04 base snap, which contains packages under GPL-2.0, GPL-3.0, LGPL, MIT, BSD and others. The exact contents of this specific build were not independently re-verified for this notice (no `.snap` unpacking tool was available) — confirm nothing else was added or changed by the wrapping before publishing.
- Corresponding source: https://archive.ubuntu.com/ubuntu/ (Ubuntu 24.04 source packages) for the inherited Ubuntu content. For ML!PA's own wrapper/build recipe, contact **opensource@ml-pa.com**.
- Note: ML!PA-built base snap wrapping Ubuntu Core 24.04. Contains many packages under differing licences inherited from the Ubuntu base, several of them copyleft — the written offer above applies.
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

- Publisher: ML!PA Consulting GmbH. Built on LavinMQ (Copyright 2018 84codes AB, https://github.com/cloudamqp/lavinmq).
- Licence: Apache-2.0 (LavinMQ's licence, full text at https://www.apache.org/licenses/LICENSE-2.0). Apache-2.0 is permissive, not copyleft, so the GPL/LGPL written offer above does not apply — but redistribution must retain LavinMQ's copyright notice, include a copy of the Apache-2.0 licence text, and reproduce LavinMQ's NOTICE file content:
  > LavinMQ
  > Copyright 2018 84codes AB.
  >
  > This product includes software developed at
  > 84codes AB (https://www.84codes.com/).
  >
  > LavinMQ is a trademark of 84codes AB
- Corresponding source: https://github.com/cloudamqp/lavinmq (LavinMQ upstream) for the LavinMQ portion. ML!PA's own changes/additions on top are not separately disclosed here — confirm with ML!PA whether this build modifies LavinMQ beyond configuration.
- Files: 5, approximately 49.9 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-staging-environment/phyboard-pollux-imx8mp-3/seed/snaps/m2cp-message-hub_4.snap`
  - `phyhub-staging-environment/phyboard-segin-imx93-2/seed/snaps/m2cp-message-hub_4.snap`

### snapd

- Publisher: Canonical Ltd. (upstream), built by ML!PA Consulting GmbH from its own build kit at `ML-PA-Consulting-GmbH/snapd-snap` — a snapd source tree patched with a custom `constants.go` (store URLs, snap IDs, account keys) and at least one ML!PA-specific build script, then compiled via that repo's Docker-based build. This is not Canonical's unmodified snapd binary.
- Licence: GPL-3.0-only (unchanged by the patching).
- Corresponding source: `ML-PA-Consulting-GmbH/snapd-snap` holds the actual patched source and build scripts for the binary distributed here, but that repository is **private** — linking to unmodified upstream (https://github.com/canonical/snapd) alone would not satisfy GPL-3.0's corresponding-source obligation for a modified build. Use the written offer above (**opensource@ml-pa.com**) to obtain the actual corresponding source; do not rely on the upstream link by itself.
- Note: The snap daemon, patched for ML!PA's own store. Copyleft: the corresponding *modified* source must be made available to anyone who receives this binary, per GPL-3.0 §6 — the written offer is the compliance mechanism here since the build repo is private.
- Files: 5, approximately 292.7 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/snapd_3.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/snapd_3.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/snapd_1.snap`
  - `phyhub-staging-environment/phyboard-pollux-imx8mp-3/seed/snaps/snapd_2.snap`
  - `phyhub-staging-environment/phyboard-segin-imx93-2/seed/snaps/snapd_2.snap`

## Trademarks

Ubuntu and Canonical are registered trademarks of Canonical Ltd. This
repository is not affiliated with or endorsed by Canonical Ltd.

