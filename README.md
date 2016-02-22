## CoreOS ARM64 Repositories

To build CoreOS for ARM64 with my development repositoties follow the CoreOS SDK instructions here https://coreos.com/docs/sdk-distributors/sdk/modifying-coreos, but use my manifest when initializing your local repositories:

    repo init -u https://github.com/glevand/coreos--manifest.git
    repo sync
    ./chromite/bin/cros_sdk --create --nousepkg

To build for ARM64 pass ```--board=arm64-usr``` to the CoreOS SDK utilities:

    ~/trunk/src/scripts/build_packages --board=arm64-usr --nousepkg
    ~/trunk/src/scripts/build_image --board=arm64-usr dev

The above commands should build the final CoreOS 'dev' disk image in ```~/trunk/src/build/images/arm64-usr/```.

See the README at https://github.com/glevand/hikey-coreos for info on running CoreOS on ARM64.
