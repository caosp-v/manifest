# CAOSP AOSP 15 ( Vanilla Ice Cream )

 Getting Started
---------------
To get started with the CAOSP sources, you'll need to get
familiar with [Git and Repo](https://source.android.com/setup/build/downloading).

 To initialize your local repository, use command:

```bash
repo init -u https://github.com/caosp-v/manifest.git -b 15 --git-lfs
```
If you wanna save some time and space

```bash
repo init --depth=1 -u https://github.com/caosp-v/manifest.git -b 15 --git-lfs
```

Then sync up:

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

Building the System
-------------------
 Initialize the ROM environment with the envsetup.sh script.

```bash
. build/envsetup.sh
```

Lunch your device after cloning all device sources if needed.

```bash
lunch aosp_devicecodename-ap3a-buildtype
```

Start compilation

```bash
make bacon -j$(nproc --all)
```
