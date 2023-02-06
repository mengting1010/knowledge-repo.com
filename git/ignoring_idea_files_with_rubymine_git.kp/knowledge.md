---
title: How to prevent git from tracking .idea files generated by rubymine
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Add .idea/ to your .gitignore file.
---

**Contents**

[TOC]

1. Create A Global Gitignore File

Create a global `.gitignore` file in your home directory that will be used across all repositories. This file should include the following line to ignore the `.idea` folder created by RubyMine:

```
.idea/
```

2. Configure Global Gitignore

Configure Git to use the global `.gitignore` file that you just created. To do this, run the following command:

```
git config --global core.excludesfile ~/.gitignore
```

3. Add Local Exclusions

If you want to exclude certain files or folders from being tracked in a particular repository, you can add additional lines to the `.gitignore` file in the root of the repository.

4. Commit Changes

Finally, commit the changes to the `.gitignore` file to ensure that the exclusions will be applied.