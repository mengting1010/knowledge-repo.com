---
title: Is there a way to get a patch-compatible output from git-diff?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, git-diff can be used to generate a patch-compatible output.
---

**Contents**

[TOC]

1. Using the `--patch` Option 

The `--patch` option allows you to generate a patch-compatible output from `git-diff`. This option can be used to generate a patch file that can be applied to a different repository, or to a different branch of the same repository.

2. Format of the Output 

The output generated by the `--patch` option is in the unified diff format, which is a standard format for patches. This format shows the differences between two files, as well as the context of the changes.

3. Usage Example 

To generate a patch-compatible output from `git-diff`, use the following command:

`git diff --patch <commit1> <commit2>`

Where `<commit1>` and `<commit2>` are the two commits you want to compare. The output will be in the unified diff format, which can then be applied to a different repository or branch.

4. Additional Resources 

For more information on the `--patch` option and the unified diff format, please see the following resources: 

- [Git Diff Documentation](https://git-scm.com/docs/git-diff)
- [Unified Diff Format Documentation](http://www.gnu.org/software/diffutils/manual/html_node/Detailed-Unified.html)