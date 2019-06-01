---
templateKey: blog-post
title: Runelite Troubleshooting
date: '2019-06-01T01:45:47-07:00'
description: Troubleshooting problems with the runelite client
tags:
  - runelite
---



## Client closing when loading
This looks like corrupted jagex cache issue. Try to delete %userprofile%\jagexcache on Windows or $HOME/jagexcache on macOS and Linux.

### Settings being reset

If you see something like IllegalArgumentException: Malformed \uxxxx in client.log and your client is not launching (launcher closing immediately but nothing opens) open %userprofile%\.runelite\settings.properties on Windows or $HOME/.runelite/settings.properties on macOS and Linux and check if it contains weird \u0000 symbols at bottom. If yes, delete them and save the file.
