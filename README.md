
# packages

Debian packaging sources and APT publication configuration.






















---

- `metapackages/host-headless/control`: initial headless dependency bundle.
- `scripts/sym/`: reserved for the complete original sym script and its packaging metadata. Not packaged yet: the supplied source is incomplete.
- `repositories/apt/`: reserved for signed APT repository configuration and publishing automation.
- `dist/`: generated .deb artifacts, not the canonical source.

## Build

```sh
mkdir -p build/host-headless/DEBIAN
cp metapackages/host-headless/control build/host-headless/DEBIAN/control
chmod 755 build/host-headless/DEBIAN # on normal filesystems
dpkg-deb --build --root-owner-group build/host-headless dist/host-headless_0.1.0_all.deb
```

This package only declares dependencies. It does not install or configure APT repositories, firewall rules, or services. Configure external repositories and package preferences separately before installation. In particular, pin `gum` to Charm's APT repository.

The maintainer field is a placeholder and should be replaced before publication.
