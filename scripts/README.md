# Bash Scripts Documentation
## compare-bin_iso
### Description
The compare-bin_iso script is used to compare files contained within BIN and ISO images. It supports both command-line execution and graphical environments (e.g., with Zenity).

### Usage
The script can be executed either from the command line or via a context menu in file managers (e.g., Nautilus, Caja, Nemo).

### Context Menu (File Manager)
1. Select the BIN and ISO files in the file manager.
2. Right-click on one of the selected files.
3. Choose the compare-bin_iso script from the context menu.

### Command Line
1. Open a terminal.
2. Navigate to the directory where the script is located.
3. Run the script, providing the paths to the BIN and ISO files as arguments:

```bash
./compare-bin_iso <path_to_BIN_file> <path_to_ISO_file>
```

### Workflow
1. File Path Input: The script prompts for the paths to the BIN and ISO files if they are not provided as arguments.
2. Password Prompt: If administrative rights are required, the script prompts for the root password.
3. File Comparison: The script compares the contents of the BIN and ISO files by executing a helper script (compare-bin_iso-helper).
4. Error Handling: The script displays appropriate error messages if any issues occur during execution.

### Notes
- Ensure you have the necessary permissions to execute the script.
- The script was developed on Zorin OS 17.2 and has been tested on Zorin OS 17.2 and Debian Bookworm (ARM). It should work on all Debian-based systems.

---

## direct-delete
### Description
The direct-delete script allows for the permanent deletion of selected files and folders. It provides a user-friendly interface for both graphical and non-graphical environments, ensuring that users are prompted to confirm the deletion before proceeding.

### Usage
The script can be executed either from the command line or via a context menu in file managers (e.g., Nautilus, Caja, Nemo).

### Graphical Environment
1. Select the files and folders you want to delete in the file manager.
2. Right-click on one of the selected items.
3. Choose the direct-delete script from the context menu.
4. A confirmation dialog will appear. Confirm the deletion to proceed.

### Command Line
1. Open a terminal.
2. Navigate to the directory where the script is located.
3. Run the script, providing the paths to the files and folders you want to delete as arguments:

```bash
./direct-delete <path_to_file_or_folder1> <path_to_file_or_folder2>
```

### Workflow
1. Confirmation Prompt: The script prompts the user to confirm the deletion of the selected files and folders.
    - In a graphical environment, this is done through a Zenity dialog.
    - In a non-graphical environment, this is done through a command-line prompt.
2. Deletion Process: If the user confirms, the script deletes the selected files and folders.
    - In a graphical environment, a progress dialog is displayed using Zenity.
    - In a non-graphical environment, a progress message is displayed in the terminal.
3. Completion Notification: The script notifies the user whether the deletion was successful or if it failed.

### Notes
- Ensure you have the necessary permissions to delete the selected files and folders.
- The script was developed on Zorin OS 17.2 and has been tested on Zorin OS 17.2 and Debian Bookworm (ARM). It should work on all Debian-based systems.

---

## Make-Desktop-File
### Description
The Make-Desktop-File script allows users to create .desktop files for selected executable files. These .desktop files can be used to easily launch applications from the desktop or application menu.

### Usage
The script can be executed either from the command line or via a context menu in file managers (e.g., Nautilus, Caja, Nemo).

### Graphical Environment
1. Select the executable files for which you want to create .desktop files in the file manager.
2. Right-click on one of the selected items.
3. Choose the Make-Desktop-File script from the context menu.
4. A confirmation dialog will appear if a .desktop file is successfully created. You have the option to edit the file or simply acknowledge its creation.

### Command Line
1. Open a terminal.
2. Navigate to the directory where the script is located.
3. Run the script, providing the paths to the executable files as arguments:

```bash
./Make-Desktop-File <path_to_executable1> <path_to_executable2>
```

### Workflow
1. Directory Creation: The script ensures that the target directory for .desktop files exists (~/.local/share/applications/user/).
2. File Validation: The script checks if each selected item is a valid, executable file.
3. .desktop File Creation: For each valid executable file, the script creates a corresponding .desktop file in the target directory.
4. Permission Setting: The script sets the appropriate permissions for the newly created .desktop files.
5. User Notification:
    - If .desktop files are successfully created, the user is notified via a Zenity dialog.
    - The user has the option to edit the created .desktop file or simply acknowledge its creation.
    - If the script encounters errors, appropriate error messages are displayed.

### Notes
- Ensure the selected files are executable.
- The script was developed on Zorin OS 17.2 and has been tested on Zorin OS 17.2 and Debian Bookworm (ARM). It should work on all Debian-based systems.

---

## rsync-copy
## Description
The rsync-copy script is used to copy files and directories from a source location to a destination using the rsync utility. It supports both graphical and non-graphical environments, providing progress feedback during the transfer.

### Usage
The script can be executed either from the command line or via a context menu in file managers (e.g., Nautilus, Caja, Nemo).

### Graphical Environment
1. Select the files and folders you want to copy in the file manager.
2. Right-click on one of the selected items.
3. Choose the rsync-copy script from the context menu.
4. A dialog will prompt you to select the destination directory.
5. The script will display a progress dialog and notify you upon completion.

### Command Line
1. Open a terminal.
2. Navigate to the directory where the script is located.
3. Run the script, providing the paths to the source files and directories as arguments:

```bash
./rsync-copy <source_file_or_directory1> <source_file_or_directory2> ...
```
4. A Dialog will prompt you to select the destination directory.
5. The script will display a progress dialog and notify you upon completion.

### Workflow
1. Source Validation: The script checks if source files or directories are provided as arguments.
2. Destination Selection:
    - In a graphical environment, a Zenity dialog prompts the user to select the destination directory.
    - In a non-graphical environment, the user is prompted to enter the destination path in the terminal.
3. File Transfer:
    - The script uses rsync to copy the source files and directories to the selected destination.
    - Progress is displayed either in a Zenity progress dialog (graphical) or in the terminal (non-graphical).
4. Completion Notification: The script notifies the user whether the transfer was successful or if it failed.

### Notes
- Ensure you have the necessary permissions to read the source files and write to the destination directory.
- The script was developed on Zorin OS 17.2 and has been tested on Zorin OS 17.2 and Debian Bookworm (ARM). It should work on all Debian-based systems.

---

## rsync-ssh-copy
### Description
The rsync-ssh-copy script is used to securely copy files and directories from a source location to a remote destination over SSH using the rsync utility. It supports both graphical and non-graphical environments, providing progress feedback during the transfer. A password is only required if no SSH key pair has been exchanged.

### Usage
The script can be executed either from the command line or via a context menu in file managers (e.g., Nautilus, Caja, Nemo).

### Graphical Environment
1. Select the files and folders you want to copy in the file manager.
2. Right-click on one of the selected items.
3. Choose the rsync-ssh-copy script from the context menu.
4. A dialog will prompt you to enter the destination path, SSH username, SSH host, and SSH password (if needed).
5. The script will display a progress dialog and notify you upon completion.

### Command Line
1. Open a terminal.
2. Navigate to the directory where the script is located.
3. Run the script, providing the paths to the source files and directories as arguments:

```bash
./rsync-ssh-copy <source_file_or_directory1> <source_file_or_directory2> ...
```

4. The script will prompt you to enter the destination path, SSH username, SSH host, and SSH password (if needed).

### Workflow
1. Source Validation: The script checks if source files or directories are provided as arguments.
2. Destination and SSH Information Input:
    - In a graphical environment, a Zenity form prompts the user to enter the destination path, SSH username, SSH host, and SSH password (if needed).
    - In a non-graphical environment, the user is prompted to enter the necessary information in the terminal.
3. File Transfer:
    - The script uses rsync over SSH to copy the source files and directories to the remote destination.
    - Progress is displayed either in a Zenity progress dialog (graphical) or in the terminal (non-graphical).
4. Completion Notification: The script notifies the user whether the transfer was successful or if it failed.

### Notes
- Ensure you have the necessary permissions to read the source files and write to the remote destination directory.
- The script was developed on Zorin OS 17.2 and has been tested on Zorin OS 17.2 and Debian Bookworm (ARM). It should work on all Debian-based systems.
