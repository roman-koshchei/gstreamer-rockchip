# Gstreamer Rockchip plugin

## Dependencies

You first need to build and install both [mpp](https://github.com/roman-koshchei/mpp) and [librga](https://github.com/roman-koshchei/librga) to your system.

Also you need `meson`:
```bash
sudo apt install meson
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
