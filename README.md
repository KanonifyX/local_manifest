# README
## Build Environment Setup

Setup the build environment following the usual ROM guide.

Setup your local sources:
e.g lineage 22.1

```
repo init -u git://github.com/LineageOS/android.git -b lineage-22.1

```

```
git clone https://github.com/KanonifyX/local_manifests.git -b 15 .repo/local_manifests
```

Then to sync up:
```
repo sync --force-sync --no-tags --no-clone-bundle --optimized-fetch --prune -c -j$(nproc --all)
```

For building the final ROM zip:
```
. build/envsetup.sh && brunch lineage_<device>-userdebug -j$(nproc --all)
```