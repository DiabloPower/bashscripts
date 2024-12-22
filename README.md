# Bash Scripts
Scripts for the command line and Zenity (graphical environment)

These scripts are developed for use with graphical file managers like Nautilus, Caja, and Nemo, but they can also be used from the command line. Note that other environments are not supported or tested.

## Features
- Compatible with Nautilus, Caja, and Nemo file managers
- Includes Zenity dialogs for graphical interaction
- Usable from the command line or graphical file managers

## Installation
There are two installation scripts available:

### 1. Install Local Scripts (`install`)
This script installs the scripts either system-wide in `/usr/bin` or for the current user in the file managers' script directories.

**Run the install script**:
```bash
chmod +x install
./install
```

### 2. Install All Scripts (`install-all`)
This script installs the local scripts as well as additional scripts from an external source.

**Run the install-all script**:
```bash
chmod +x install-all
./install-all
```

**Additional Scripts Source**:
- GitHub Repository: [nautilus-scripts](https://github.com/cfgnunes/nautilus-scripts.git)
- Local ZIP File: `nautilus-scripts-main.zip` (if present)

## Compatibility
These scripts were developed on Zorin OS 17.2 but should run on all Debian-based systems. Tested on:

- Zorin OS 17.2
- Debian Bookworm (ARM)

## Usage
### Graphical File Managers
The scripts can be accessed via the context menu in Nautilus, Caja, or Nemo.

### Command Line
The scripts can also be executed directly from the command line if they are installed system-wide or for the current user:

```bash
script_name (like rsync-ssh-copy)
```

## License

```plaintext
# 
# Copyright (c) 2024 Ronny Hamann
# 
# License Terms:
# 
# 1. Modifications of this script are permitted for personal use.
# 2. Redistribution or reuse of the modified or unmodified script
#    is only allowed with prior written permission from the author.
# 
# Disclaimer of Warranty:
# 
# This script is provided "as is", without warranty of any kind, express or implied,
# including but not limited to the warranties of merchantability, fitness for a particular purpose,
# and noninfringement. In no event shall the author be liable for any claim, damages or other liability,
# whether in an action of contract, tort or otherwise, arising from, out of or in connection with the
# script or the use or other dealings in the script.
#
```

## Contributing
Feel free to open issues or submit pull requests if you want to contribute to the project.

## Contact
For any questions or feedback, please contact Ronny Hamann.
