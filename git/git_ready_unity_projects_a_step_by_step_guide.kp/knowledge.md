---
title: What are the steps for setting up a unity project for git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a .gitignore file in the root of the project and add the relevant folders and files to be excluded from version control.
---

**Contents**

[TOC]

#### Section 1: Create a .gitignore File
1. In the root of your Unity project, create a new file called .gitignore.
2. Add the following lines to the .gitignore file:

```
# This .gitignore file should be placed at the root of your Unity project directory
#
# Get latest from https://github.com/github/gitignore/blob/master/Unity.gitignore
#
# /[Ll]ibrary/
# /[Tt]emp/
# /[Oo]bj/
# /[Bb]uild/
# /[Bb]uilds/
# /Assets/AssetStoreTools*
#
# # Visual Studio 2015 cache directory
# .vs/
#
# # Autogenerated VS/MD/Consulo solution and project files
# ExportedObj/
# .consulo/
# *.csproj
# *.unityproj
# *.sln
# *.suo
# *.tmp
# *.user
# *.userprefs
# *.pidb
# *.booproj
# *.svd
# *.pdb
#
# # Unity3D generated meta files
# *.pidb.meta
# *.pdb.meta
# *.mdb
#
# # Unity3D Generated File On Crash Reports
# sysinfo.txt
#
# # Builds
# *.apk
# *.unitypackage
```

#### Section 2: Initialize a Git Repository
1. In the root of your Unity project, open the Terminal and run the command `git init`.
2. This will create a new git repository in your project folder.

#### Section 3: Add Files to the Repository
1. In the Terminal, run the command `git add .` to add all files and folders in your project to the repository.
2. This will stage all the changes to be committed.

#### Section 4: Commit the Changes
1. In the Terminal, run the command `git commit -m "Initial commit"`.
2. This will commit all the changes to the repository and add a commit message.
