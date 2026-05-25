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
- Checks if already downloaded, skips if true
- Allows user to specify install and download directory (Optional)
- Checks for existance of install and download directory, creates them if missing
- Checks if install directory is empty, user confirmation if not empty
- User confirmation before clearing directory (refresh install)
- Prunes root dir from package, that way we always extract to same install folder (useful for maintaining shortcuts across upgrades and avoiding multiple installs)
- Verifies downloaded archive against the MD5 checksum published on the downloads page (aborts on mismatch)
- Detects installed version by reading the shipped PSUnreal/Config/config.xml and skips install if already on the latest published version (works for manual installs too)

# Planned
- Add option to override install skip when latest version already installed, in order to force "refresh" install
- Add option to perform overwrite install, rather than "refresh" install (maybe not nessecaery since configs live elsewhere)

# Requirements
- Install lynx package

# Reccomended Usage
You can run this from anywhere, it will always download and install to the specified locations.

I prefer to use it like this:
- Clone and copy to your ~/bin or other $PATH and run 'updatepsu' from any terminal, anywhere
- Remember to 'sudo chmod +x ~/bin/updatepsu'
