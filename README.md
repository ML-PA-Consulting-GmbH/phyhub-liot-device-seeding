# phyhub-liot-device-seeding

Minimal snapd seeds per distribution. Each top-level folder is one distribution. 

## Folder contents

**Note:** `template/model.json` and `template/seed-template.yaml` are not required at runtime. They are kept here so the model and seed can be re-uploaded or regenerated whenever needed.

### `template/model.json`
The registration of the model in the L-IoT appstore. It is uploaded to the store with the `m2cp` CLI:

```
m2cp store system model push <file> <description>
```

This only needs to be done **once** per model. 

---

### `constants.go`
Store branding for the snapd build. During the snapd build process this file
replaces `constants/constants.go` so the resulting snapd binary talks to the
correct store. It contains the store's public keys, which snapd uses to verify assertions.

---

### `seed/`
The prebuilt, ready-to-use seed directory. It contains the initial set of snaps
and the assertions / certificates snapd needs to verify them.

snapd installs the seed on its **first start**, before the device attempts to
register with the store. Without a valid seed (and its certificates) the device
cannot bootstrap.

Deploy `seed/` to `/var/lib/snapd/seed`. Because we run snapd on a dedicated
data partition (so it survives OS updates), this is wherever `/var/lib/snapd`
actually lives on the target.

---

### `template/seed-template.yaml`
Input format for our `m2cp` CLI. It declaratively describes the seed contents
(snaps, assertions, channels, etc.) and is used to generate the `seed/`
directory.

---
