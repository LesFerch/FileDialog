# FileDialog

[![image](https://user-images.githubusercontent.com/79026235/152910441-59ba653c-5607-4f59-90c0-bc2851bf2688.png)Download the zip file](https://github.com/LesFerch/FileDialog/releases/download/1.2.1/FileDialog.zip)

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
Usage: FileDialog DialogType [~DialogTitle] [StartPath] [DialogFilter] [Multi] [Retro]
DialogType must be one of: Open Save Folder
Parameters may be specified in any order and are not case sensitive
Prefix DialogTitle with ~ Example: ~"Select an image file"
Parameters must be quoted if they contains spaces
If StartPath is quoted, omit or double up trailing backslash
Forward slashes may be used in place of backslash without any need to double up
Relative paths are supported (e.g. .\MyStuff or ..\MyStuff)
StartPath may also be one of: Documents Libraries OneDrive Public ThisPC UserProfile
Multiselect is supported for File Open and Folder dialogs and is OFF by default.
The Retro parameter will give you old school Open, Save, and Folder select dialogs
Microsoft's modern dialogs insist on going to Libraries for Documents, Pictures, and so on
Use the Retro parameter to avoid Libraries
Environment variables are supported. Be sure to quote them if they contain spaces.
Example: FileDialog Open C:\Users "*.ini|*.ini" Multi
Example: FileDialog Open C:\Users\ "*.ini|*.ini" ~"Select an INI file"
Example: FileDialog Save "C:\Users" "Text files (*.txt)|*.txt"
Example: FileDialog Save "C:\Users\\" "Text files (*.txt)|*.txt"
Example: FileDialog Open "C:\Users" "Image Files(*.PNG;*.JPG)|*.PNG;*.JPG|All files (*.*)|*.*"
Example: FileDialog Open UserProfile
Example: FileDialog Folder ThisPC
Example: FileDialog Open "%UserProfile%\Pictures" Retro
Example: FileDialog Open "C:\Users\Public\Documents" Retro
Example: FileDialog Open "%LocalAppData%"
At start, ? is written to  HKCU\Software\FileDialog
On Cancel, '' is written to  HKCU\Software\FileDialog
Upon user selection, a single, unquoted item is written to HKCU\Software\FileDialog Default
Selected items are written in CSV format to the console and HKCU\Software\FileDialog ItemList
Selected items are also written as a multi-string to HKCU\Software\FileDialog ItemListM
```


## Usage Examples

Example 1:
`FileDialog Open "%UserProfile%\Pictures\Misc" "Image Files(*.PNG;*.JPG)|*.PNG;*.JPG|All files (*.*)|*.*"`\
![image](https://user-images.githubusercontent.com/79026235/163309637-419b7aba-ec49-4d4a-b307-ce8ac0677f54.png)


Example 2:
`FileDialog Open "%UserProfile%\Documents" "Text Files|*.txt"`\
![image](https://user-images.githubusercontent.com/79026235/163312124-804e5a58-eecb-46dc-b8dd-c52278567b7a.png)

Example 3:
`FileDialog Open "%UserProfile%\Documents" "Text Files|*.txt" Retro`\
![image](https://user-images.githubusercontent.com/79026235/163312322-16e9dedc-83a4-4eab-b312-7717ebe03c86.png)

Example 4:
`FileDialog Folder Downloads`\
![image](https://user-images.githubusercontent.com/79026235/163312451-88d5afc4-9ac6-4650-9165-3e2b4e28253c.png)

Example 5:
`FileDialog Folder "%UserProfile%\Downloads" Retro`\
![image](https://user-images.githubusercontent.com/79026235/163312686-5bc42060-b1dc-40e6-aaf9-f0a5a7418557.png)
\
\
[![image](https://user-images.githubusercontent.com/79026235/153264696-8ec747dd-37ec-4fc1-89a1-3d6ea3259a95.png)](https://github.com/LesFerch/FileDialog)
