# <b> <i> Project Mist | Built with </i>💖

### Create a directory for the source files
* You can name this directory however you want, just remember to replace 
* WORKSPACE with your directory for the rest of this guide.
* This can be located anywhere (as long as the fs is case-sensitive)

```bash 
mkdir Mist
cd Mist
```

### Install Repo in the created directory

>> [Hint: This might take a long time]

```bash
repo init -u https://github.com/Mist-OS/manifest.git -b 13.0
```

>> [Hint: Want to save some space ? Then use this]

```bash
repo init --depth=1 -u https://github.com/Mist-OS/manifest.git -b 13.0
```

### Download the source
```bash 
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build
```bash
# Set up environment
. build/envsetup.sh
# Choose a target
lunch mist_$device-userdebug
# Build the code
mka bacon -jX
```

### Credits
 * [**AOSP**](https://android.googlesource.com) 
 * [**LineageOS**](https://github.com/LineageOS) 
 * [**CherishOS**](https://github.com/CherishOS) 
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**ArrowOS**](https://github.com/ArrowOS)
