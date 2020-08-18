Compilation of custom settings and tweaks
=========================================

This repository is a growing collection of settings and tweaks that I usually apply to the apps, tools and whatever that I use.

Usage instructions
==================

The settings are uploaded as patch files in order to keep as much as the default or already set settings of the config files. In order to apply this patches you will need the diffutils package, included in Linux distributions and MacOS. For Windows users, the easiest way to get a working enviroment is to install [Git for Windows](https://git-scm.com/) and run Git Bash.

In order to apply the patches, you will need to use the patch command:

```
patch "(settings file path)" "(patch file path)"
```

You can download the patch files from the subfolders of this repository. In order to get the settings file path, please refer to the specific readme instructions, since some can be really tricky to get.

On windows devices, you will need to convert the paths into an UNIX-style path. I personally move to the folder where the patch is and use the following command to convert the settings file path to UNIX-style:

```
patch $(echo "(settings file path)" | sed 's/^\([A-Z]\):\\/\/\L\1\//; s/\\/\//g') (patch file name)
```

Althought that sed expression is a nightmare to understand (as it was to make!), it works even if the path is not on the C drive, and seems to be pretty reliable.

Alternatively, you can do it manually:

- Replace the drive letter and the volume separator (C:) with a forward slash and the drive letter in lowercase (/c)
- Replace every backslash with a a forward slash

And you're good to go!

How to contribute
=================

Feel free to [create an issue](https://github.com/crberme/settings/issues/new) if something breaks or [create a pull request](https://github.com/crberme/settings/pulls) if you want to contribute!