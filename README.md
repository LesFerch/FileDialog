# FileDialog

[![image](https://user-images.githubusercontent.com/79026235/152910441-59ba653c-5607-4f59-90c0-bc2851bf2688.png)Download the zip file](https://github.com/LesFerch/FileDialog/releases/download/1.0.0/FileDialog.zip)

## Windows command line file and folder dialog for use in scripts

Compatible with Windows 7, 8, 10, and 11.

# How to Download and Run

1. Download the zip file using the link above.
2. Extract **FileDialog.exe**.
3. Open a Cmd prompt and run **FileDialog.exe** with no parameters to see the built-in help.
5. Use **FileDialog.exe** in your scripts when you need a file open, file save, or folder select dialog.

**Note**: Some antivirus software may falsely detect the download as a virus. This can happen anytime you download a new executable and may require extra steps to whitelist the file. In testing, no issues were encountered using Windows Defender on Windows 10 and 11, but a false positive "virus detected" occurred on Windows Server 2022.

# Summary

**FileDialog** is a command line file dialog tool for use in Windows scripts. It can provide a:
- File Open dialog
- File Save dialog
- Folder select dialog

# How to Use

**Filedialog.exe** is typically run from within a script (batch file, VBScript, PowerShell, etc.).

## See the built in help

Running **FileDialog** with no parameters will display the built-in help:
```
Usage: FileDialog.exe DialogType [~DialogTitle] [StartPath] [DialogFilter] [Multi]
DialogType must be one of: Open Save Folder
Parameters may be specified in any order and are not case sensitive
Prefix DialogTitle with ~ Example: ~"Select an image file"
DialogTitle must be quoted if it contains spaces
If StartPath is quoted, omit or double up trailing backslash
Forward slashes may be used in place of backslash without any need to double up
Relative paths are supported (e.g. .\MyStuff or ..\MyStuff)
StartPath may also be one of: Documents Libraries OneDrive Public ThisPC UserProfile
Multiselect is supported for File Open dialogs and is off by default.
Example: FileDialog.exe Open C:\Users "*.ini|*.ini" multi
Example: FileDialog.exe Open C:\Users\ "*.ini|*.ini" ~"Select one or more INI files"
Example: FileDialog.exe Save "C:\Users" "Text files (*.txt)|*.txt"
Example: FileDialog.exe Save "C:\Users\\" "Text files (*.txt)|*.txt"
Example: FileDialog.exe Open "C:\Users" "Image Files(*.PNG;*.JPG)|*.PNG;*.JPG|All files (*.*)|*.*"
Example: FileDialog.exe Folder ThisPC
At start, ? is written to  HKCU\Software\FileDialog
On Cancel, '' is written to  HKCU\Software\FileDialog
Upon user selection, a single, unquoted item is written to HKCU\Software\FileDialog Default
Selected items are written in CSV format to the console and HKCU\Software\FileDialog ItemList
Selected items are also written as a multi-string to HKCU\Software\FileDialog ItemListM
```

\
\
[![image](https://user-images.githubusercontent.com/79026235/153264696-8ec747dd-37ec-4fc1-89a1-3d6ea3259a95.png)](https://github.com/LesFerch/FileDialog)