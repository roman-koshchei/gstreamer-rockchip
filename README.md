# Gstreamer Rockchip plugin

## Dependencies

You first need to build and install both [mpp](https://github.com/roman-koshchei/mpp) and [librga](https://github.com/roman-koshchei/librga) to your system.

Also you need:
```bash
sudo apt install meson pkg-config libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev
```

## Build and installation

Clone and enter repository:
```bash
git clone https://github.com/roman-koshchei/gstreamer-rockchip && cd gstreamer-rockchip
```

Setup meason build:
```bash
meson setup build --prefix=/usr
```

Ninja build:
```bash
ninja -C build
```

Installation:
```bash
sudo ninja -C build install
```

Reload libraries:
```bash
sudo ldconfig
```

## Verify

Run and check if all are present:
```bash
rm ~/.cache/gstreamer-1.0/registry.* && gst-inspect-1.0 rockchipmpp
```
