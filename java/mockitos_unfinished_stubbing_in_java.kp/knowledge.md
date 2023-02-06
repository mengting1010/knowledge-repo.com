---
title: Mockito has identified incomplete stubbing
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Mockito detects when a method is stubbed but never used or when a stubbed method does not have an explicit answer defined.
---

**Contents**

[TOC]

## What is Unfinished Stubbing?
Unfinished stubbing is a warning that is generated by the Mockito framework when a test is run and it detects that one or more stubbing calls have been made but not completed. This can occur when a mock object is created, but the expected behavior for the mock object is not specified.

## Why is Unfinished Stubbing a Problem?
Unfinished stubbing can lead to unexpected behavior in tests as the mock object will not respond as expected. This can cause tests to fail unexpectedly or to produce incorrect results. It can also lead to code that is difficult to debug and maintain.

## How to Avoid Unfinished Stubbing
The best way to avoid unfinished stubbing is to ensure that all stubbing calls are completed before running a test. This can be done by double-checking that all expected behavior is specified for each mock object. Additionally, Mockito provides a “verifyNoMoreInteractions” method which can be used to verify that no more interactions have been made with a mock object than what was expected.

## How to Resolve Unfinished Stubbing
If unfinished stubbing is detected, the best way to resolve the issue is to first identify which mock object is causing the problem and then to complete the stubbing for that object. This can be done by adding the expected behavior for the mock object or by removing any unnecessary stubbing calls. Once the issue has been resolved, the test can be re-run to verify that the issue is fixed.