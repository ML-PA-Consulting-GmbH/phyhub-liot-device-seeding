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

- Publisher: ML!PA Consulting GmbH, built from the private build kit at `ML-PA-Consulting-GmbH/core24`. Per that repo's `dependencies.json`, the base is Canonical Ltd.'s official, unmodified `core24` snap (snap-id `dwTAh7MZZ01zyriOZErqd1JynQLiOGvM`, version `20260410`, revision 1644 arm64 / 1643 amd64), fetched from the snap store. The build kit's `build.sh` then unpacks it, merges in a small `etc/` overlay (login banner/MOTD text, a `writable` marker — no code), rewrites the version string in `meta/snap.yaml`, disables SSH password authentication (`PasswordAuthentication no` in `etc/ssh/sshd_config`), and repacks it — signed and republished through ML!PA's own snap store (`developer-id: appstore` in the snap-revision assertion). Not Canonical's stock artifact.
- Licence: Multiple (GPL-2.0, GPL-3.0, LGPL, MIT, BSD and others), inherited from the Ubuntu Core 24.04 package set that Canonical's core24 snap ships — confirmed via the pinned upstream version above, not a guess.
- Corresponding source: https://archive.ubuntu.com/ubuntu/ (Ubuntu 24.04 source packages) for the inherited Ubuntu content — Canonical does not publish a separate build-recipe repository for `core24` the way it does for `snapd`. ML!PA's own overlay/build recipe lives in the private `ML-PA-Consulting-GmbH/core24` repo; use the written offer above (**opensource@ml-pa.com**) to obtain it.
- Note: ML!PA-built base snap wrapping Canonical's core24. Contains many packages under differing licences inherited from the Ubuntu base, several of them copyleft — the written offer above applies. ML!PA's own changes are limited to configuration (MOTD, SSH hardening, version string), not a source-level patch to any GPL/LGPL package itself.
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

- Publisher: ML!PA Consulting GmbH, snap-packaged from ML!PA's private build kit at `ML-PA-Consulting-GmbH/m2cp-message-hub` around an **unmodified** LavinMQ (Copyright 2018 84codes AB, https://github.com/cloudamqp/lavinmq). The build kit's `dependencies.json` pins LavinMQ 2.9.3-1 and fetches it as the official `.deb` (arm64/amd64) straight from CloudAMQP's own packagecloud repository, with a checksum recorded — it is not rebuilt from patched source the way this repository's `snapd` and `core24` are.
- Licence: Apache-2.0 (LavinMQ's licence, full text at https://www.apache.org/licenses/LICENSE-2.0). Apache-2.0 is permissive, not copyleft, so the GPL/LGPL written offer above does not apply — but redistribution must retain LavinMQ's copyright notice, include a copy of the Apache-2.0 licence text, and reproduce LavinMQ's NOTICE file content:
  > LavinMQ
  > Copyright 2018 84codes AB.
  >
  > This product includes software developed at
  > 84codes AB (https://www.84codes.com/).
  >
  > LavinMQ is a trademark of 84codes AB
- Corresponding source: LavinMQ 2.9.3, https://github.com/cloudamqp/lavinmq (tag v2.9.3), or the exact package at `https://packagecloud.io/cloudamqp/lavinmq/ubuntu/pool/noble/main/l/lavinmq/lavinmq_2.9.3-1_<arch>.deb`. ML!PA's own snap-packaging layer (systemd units, snap metadata under `src/snap/`) is proprietary and not separately disclosed here.
- Files: 5, approximately 49.9 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/m2cp-message-hub_1.snap`
  - `phyhub-staging-environment/phyboard-pollux-imx8mp-3/seed/snaps/m2cp-message-hub_4.snap`
  - `phyhub-staging-environment/phyboard-segin-imx93-2/seed/snaps/m2cp-message-hub_4.snap`

### snapd

- Publisher: Canonical Ltd. (upstream), built by ML!PA Consulting GmbH from a patched source tree (custom `constants.go`, TPM-related build changes) via the private build kit at `ML-PA-Consulting-GmbH/snapd-snap`. This is not Canonical's unmodified snapd binary.
- Licence: GPL-3.0-only (unchanged by the patching).
- Corresponding source: ML!PA maintains a **public** fork of snapd at https://github.com/ML-PA-Consulting-GmbH/snapd. Its default branch (`master`) tracks upstream Canonical content largely unpatched — the actual modifications live on named branches, e.g. `feat/dynamic_constants` (the swappable-`constants.go` mechanism) and `feat/tpm-improvements` (matching the `build_m2cp-tpm.sh` script found in the build kit), merged forward through release branches such as `release/2.77`. `release/2.77`'s latest commit (2026-07-13) is the closest by date to this binary's snap-revision assertion (revision 3, published 2026-08-28) but the exact commit was **not verified against the binary** — confirm the precise branch/commit before citing it as the definitive corresponding source. Fall back to the written offer above (**opensource@ml-pa.com**) if that pinning can't be nailed down.
- Note: The snap daemon, patched for ML!PA's own store. Copyleft: the corresponding *modified* source must be made available to anyone who receives this binary, per GPL-3.0 §6. The public fork's default branch is not itself sufficient evidence of what was shipped — treat it as a starting point, not a substitute for confirming the exact branch/commit.
- Files: 5, approximately 292.7 MB

  - `phyhub-production-environment/seeds/seed-phyboard-pollux-imx8mp-3/seed/snaps/snapd_3.snap`
  - `phyhub-production-environment/seeds/seed-phyboard-segin-imx93-2/seed/snaps/snapd_3.snap`
  - `phyhub-production-environment/seeds/seed-phygate-tauri-l-imx8mm-2/seed/snaps/snapd_1.snap`
  - `phyhub-staging-environment/phyboard-pollux-imx8mp-3/seed/snaps/snapd_2.snap`
  - `phyhub-staging-environment/phyboard-segin-imx93-2/seed/snaps/snapd_2.snap`

## Trademarks

Ubuntu and Canonical are registered trademarks of Canonical Ltd. This
repository is not affiliated with or endorsed by Canonical Ltd.

