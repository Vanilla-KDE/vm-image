# Vanilla OS Kipferl VM Image

Containerfile for building a Vanilla OS KDE + VM image.

This image is based on top of [`vanillakde/kde`](https://github.com/Vanilla-KDE/desktop-image/pkgs/container/kde) and offers the default Vanilla OS Desktop experience with KDE and VM tools pre-installed.

## Build

```bash
vib build recipe.yml
podman image build -t vanillakde/kde-vm .
```

## Verify Image Build Provenance Attestation

All the image builds/pushes are attested for build provenance and integrity using the [attest-build-provenance](https://github.com/actions/attest-build-provenance) action. The attestations can be verified [here](https://github.com/Vanilla-KDE/vm-image/attestations) or by having the latest version of [GitHub CLI](https://github.com/cli/cli/releases/latest) installed in your system. Then, execute the following command:

```sh
gh attestation verify oci://ghcr.io/vanilla-kde/kde-vm:latest --owner Vanilla-KDE
```
