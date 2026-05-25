```
                 _       _
 _   _ _ __   __| | __ _| |_ ___ _ __  ___ _   _
| | | | '_ \ / _` |/ _` | __/ _ \ '_ \/ __| | | |
| |_| | |_) | (_| | (_| | ||  __/ |_) \__ \ |_| |
 \__,_| .__/ \__,_|\__,_|\__\___| .__/|___/\__,_|
      |_|                       |_|
```

# updatepsu
Install, Refresh, and/or Update to the latest version of PlaneShift Unreal for Linux.

Useful for when official updater cannot be used, full release update is required, or to "refresh" a broken install.

# Features
- Always targets latest published full package
- Caches downloads — re-runs skip the download if the archive is already in your download folder
- Verifies downloaded archive against the MD5 checksum published on the downloads page (aborts on mismatch)
- Detects installed version by reading the shipped `PSUnreal/Config/config.xml` and skips install if already on the latest published version (works for manual installs too)
- Version-aware install prompt: silent on fresh installs, asks before refreshing same version, defaults to yes on updates, defaults to no on unknown existing installs
- Interactive paths — accept the defaults with Enter, or type a different download / install path at the prompt
- Creates the install and download directories if missing
- Prunes the root dir from the package so the install always lands at the same path (useful for maintaining shortcuts across upgrades and avoiding multiple installs)
- Preflights required tools (`lynx`, `wget`) and prints the exact install command for your distro if either is missing
- Colored, status-style output with a magenta-to-yellow gradient banner

# Requirements
- `lynx` (used to parse the downloads page)
- `wget` (used to download the package)

The script checks for both at startup and prints the exact install command for your distro (apt, pacman, dnf, zypper) if either is missing.

# Recommended Usage
The script is a single self-contained file. It will download and install to the paths you confirm at the prompt (defaults to `~/Downloads` and `~/PSUnreal`), so you can run it from anywhere.

**Quickest — just grab the script:**
```
wget https://raw.githubusercontent.com/mjevange/updatepsu/main/updatepsu
chmod +x updatepsu
./updatepsu
```

**Or clone the whole repo:**
```
git clone https://github.com/mjevange/updatepsu.git
cd updatepsu
bash updatepsu
```

To run it from anywhere afterward, copy `updatepsu` into a directory on your `$PATH` (e.g. `~/bin`) and you can invoke it as `updatepsu` from any terminal.
