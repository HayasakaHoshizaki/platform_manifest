# <img src="https://github.com/Project-Altermis/platform_manifest/blob/Sanitize/Project-Altermis.png" width="512"> #

### 如何同步源码/To Sync ###

```bash
# Initialize local repository
repo init -u https://github.com/Project-Altermis/platform_manifest -b Sanitize

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags --fail-fast
```

### 如何编译/To Build ###

```bash
# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch altermis_$device-userdebug

# To build
$ make bacon -j$(nproc --all)
