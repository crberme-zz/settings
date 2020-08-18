Windows Terminal Settings
=========================

The included settings.json patch makes the following changes:

- Enabled acrylic transparency. Almost opaque, but enought to be noticeable.
- Hidden Azure Cloud Shell profile.
- Added Git Bash profile. It uses the same font face and size as Mintty.
- Enabled dark theme

To avoid flicker while using Git bash, open %USERPROFILE%/.inputrc (create one if it doesn't exist) and add the following line:

```
set bell-style none
```

(See [microsoft/terminal: GIT Bash has bad flicker](https://github.com/microsoft/terminal/issues/7200#issue-674299990))

Usage instructions
==================

Before applying the patch, you will need to get your settings.json path. In order to get it, open Windows Terminal, open the dropdown menu and click on "Settings". Depending on the text editor that opens the settings file, the next steps may vary:

- Notepad:

    1. File>Save As...
    2. Open the Save as Type dropdown menu and select: All types(\*.*)
    3. Right click the now visible settings.json file while holding the Shift key
    4. Click on Copy as path

- Visual Studio Code:

    1. Open the command palette
    2. Select Copy Path of Active File

When you have the settings file path, refer to the repository README for available tools and their usage instructions.