
# packages

Debian packaging sources and APT publication configuration.
Follow instructions below edepnding on case.

## New package

pkg/<pkg-name>/DEBIAN/control

## Build packages

./build

## Publish packages

?

## Testing

Start a disposable Debian 13 container:

```bash
start-os
```

Inside the container:

```bash
apt update
apt install /pkg/hello_0.0.0.deb
dpkg -s hello
```

Exit to destroy the container.

