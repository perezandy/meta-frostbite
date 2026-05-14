meta-frostbite
================================

My own lightweight OpenEmbedded/Yocto Layer.

What is Frostbite?
-------------------------

Frostbite is what I call my beaglebone with a screen connected. I wanted finer control of what goes into the image as well as to familiarize myself with the yocto system. My planned features are a github contributions showcase that lets you change the user and colors, as well as a generic UI for more apps.

Can I just use linux or android and be fine? Yes. But I won't.

Hardware
-------------------------

This layer is configured for:

- **BeagleBone Black** (AM335x ARM Cortex-A8)
- **NewHaven 7-inch IPS LCD cape** with capacitive touchscreen
  - Product page: <https://newhavendisplay.com/7-inch-ips-lcd-beaglebone-cape-with-capacitive-touchscreen/>
- Optional: (TODO add the 3D Print here)

Building
-------------------------

Cloning bitbake itself is deprecated, I had to follow this guide:
[https://docs.yoctoproject.org/dev-manual/poky-manual-setup.html]
I chronicled my steps here.

1. Setup a workspace by cloning the core OpenEmbedded/Yocto Layers:

```bash
mkdir -p frostbite/layers && cd "$_"
git clone -b yocto-5.3.3 https://git.openembedded.org/bitbake
git clone -b yocto-5.3.3 https://git.openembedded.org/openembedded-core
git clone -b yocto-5.3.3 https://git.yoctoproject.org/meta-yocto
git clone https://github.com/perezandy/meta-frostbite.git
```

1. Initialize and build

```bash
cd ../
ln -s layers/meta-frostbite/env_setup.sh .
source env_setup.sh # NOTE: This will put you in build/
 
# Make sure conf/bblayers.conf includes meta-frostbite
frostbite/
├── build
│   ├── bitbake-cookerdaemon.log
│   ├── cache
│   │   ├── hashserv.db
│   │   ├── hashserv.db-shm
│   │   └── hashserv.db-wal
│   ├── conf
│   │   ├── bblayers.conf   # <------- HERE
│   │   ├── conf-notes.txt
│   │   ├── conf-summary.txt
│   │   ├── local.conf
│   │   └── templateconf.cfg


# Edit should look like so:
BBLAYERS ?= " \
  /home/.../frostbite/layers/openembedded-core/meta \
  /home/.../frostbite/layers/openembedded-core/../meta-yocto/meta-poky \
  /home/.../frostbite/layers/openembedded-core/../meta-yocto/meta-yocto-bsp/ \
  /home/.../frostbite/layers/openembedded-core/../meta-frostbite/common-bsp/ \
  "

# Now build:
bitbake frostbite-image
```

The built image will be in `tmp/deploy/images/beaglebone/`.

What's Inside
-------------------------

The `frostbite-image` recipe includes:

- Linux kernel with NewHaven LCD cape drivers enabled
- Framebuffer utilities for direct display access
- Touch input support (via evdev/libinput)
- Busybox for essential POSIX utilities
- SSH server for headless management
- Minimal init system (sysvinit)

Maintainer
-------------------------

Andy Perez <perezandy2001@gmail.com>

License
-------------------------

MIT License - see individual recipes for specifics.
