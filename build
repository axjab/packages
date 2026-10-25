
#!/usr/bin/env bash
set -euo pipefail

mkdir -p dist
dpkg-deb --root-owner-group --build pkg/hello dist   # version supplied automatically





# cd "$(dirname "$0")"

# mkdir -p build dist
# rm -rf build/sym build/host-headless

# # Build sym
# bash -n scripts/sym/sym

# mkdir -p build/sym/DEBIAN build/sym/usr/bin
# cp scripts/sym/control build/sym/DEBIAN/control
# install -m 755 scripts/sym/sym build/sym/usr/bin/sym

# dpkg-deb --build --root-owner-group \
#   build/sym dist/

# # Build host-headless
# mkdir -p build/host-headless/DEBIAN
# cp metapackages/host-headless/control \
#   build/host-headless/DEBIAN/control

# dpkg-deb --build --root-owner-group \
#   build/host-headless dist/

# echo "Packages built successfully:"
# ls -lh dist/*.deb

