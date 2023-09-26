# updatepsu
Refresh Installation and/or Update to latest version of PlaneShift Unreal for Linux.
Useful for when the updater cannot be used or full release update is required.

# Features
- Always downloads the latest version of PlaneShift Unreal for Linux
- Allows user to specify download and install directory (Optional)
- Checks for existance of install directory
- Checks is install directory is empty
- Checks with user before clearing install directory

# Planned
- Add logic to check if user is already on latest version, provide option to skip
- Add option to overwrite, rather than clear install dir (maybe not nessecaery since configs live elsewhere)

# Requirements
- Install lynx package

# Reccomended Usage
You can run this from anywhere, it will always download and install to the specified locations.

I prefer to use it like this:
- Clone and copy to your ~/bin or other $PATH and run 'updatepsu' from any terminal, anywhere
- Remember to 'sudo chmod +x ~/bin/updatepsu'
