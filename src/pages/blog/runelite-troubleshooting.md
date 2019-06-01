---
templateKey: runelite-client
title: Troubleshooting problems with the client
date: '2018-04-09T12:38:54-04:00'
description: >-
   Troubleshooting problems with the runelite client
tags:
  - blog
---


## Client closing when loading
This looks like corrupted jagex cache issue. Try to delete %userprofile%\jagexcache on Windows or $HOME/jagexcache on macOS and Linux.

### Settings being reset

If you see something like IllegalArgumentException: Malformed \uxxxx in client.log and your client is not launching (launcher closing immediately but nothing opens) open %userprofile%\.runelite\settings.properties on Windows or $HOME/.runelite/settings.properties on macOS and Linux and check if it contains weird \u0000 symbols at bottom. If yes, delete them and save the file.
