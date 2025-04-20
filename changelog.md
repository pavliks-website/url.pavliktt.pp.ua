---
layout: default
title: URL shortener changelog
permalink: /changelog/
---

# Changelog
**URL Shortener uses semantic versioning: MAJOR.MINOR.PATCH**

## 3.0.1
 - Changed v1 link error message

## 3.0.0
 - v1 links are now deprecated and **no longer supported**
 - engine completely rewritten to use itty `Router`.
 - project is now open-source, source code available at [GitLab](https://gitlab.com/pavliks-website/url-shortener-backend)

## 2.2.1
 - *i dont remember anymore sry*

## 2.2.0
 - **Actually** implemented `/{link id}!` endpoint...

## 2.1.0
 - Added `/{link id}!` endpoint to get link metadata

## 2.0.0
 - Added `mode` field that determines length of the output URL.
 - Made links use pseudo-random generator instead of SHA256 hash.

## 1.0.0
 - Initial release
