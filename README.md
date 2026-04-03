# based-os &nbsp; [![bluebuild build badge](https://github.com/jle64/based-os/actions/workflows/build.yml/badge.svg)](https://github.com/jle64/based-os/actions/workflows/build.yml)

Personnal custom image. Based. Made with [BlueBuild docs](https://blue-build.org/how-to/setup/).

## Rebasing

On bootc systems:
```bash
bootc switch ghcr.io/jle64/based-os
```

On rpm-ostree systems:
```bash
rpm-ostree rebase ostree-unverified-registry:ghcr.io/jle64/based-os:latest
systemctl reboot
rpm-ostree rebase ostree-image-signed:docker://ghcr.io/jle64/based-os:latest
systemctl reboot
```

## Building an ISO

```bash
bluebuild generate-iso --iso-name based-os.iso image ghcr.io/jle64/based-os
```

## Signature verification

```bash
cosign verify --key cosign.pub ghcr.io/jle64/based-os
```
