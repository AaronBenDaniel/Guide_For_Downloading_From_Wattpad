---
    Title: 🤖 Android 🤖
    Summary: If you want to download on an Android device.
    weight: 5
---

There are two options for running a Wattpad downloader on Android: the easy way, and the hard way.

### The Easy Way:

This method involves hosting an instance of [Feuerhamster](https://github.com/Feuerhamster)'s `wattpad-downloader`. Although it actually uses an older fork.

The following steps are based on this guide: https://wpdl-termux.wasmer.app.

1) Install Termux through the [Play Store](), [F-Droid](), or [GithHub](https://github.com/termux/termux-app/releases).

2) Open Termux and run this command: `curl -L https://tinyurl.com/4yjur5xk -o download.sh;/bin/bash download.sh` \
**NOTE: Every character in these commands is important. Do not leave out any periods (.), slashes (/), the semicolon (;), or any other character**.

This will download three scripts that can be used to control the downloader.

3) Run `./install.sh`

Once this is completed, an instance of `wattpad-downloader` will be running on your device and it can be accessed at **{{< linknewtab "http://localhost:3000" "http://localhost:3000" >}}**.

To stop the downloader, run `./stop.sh` and exit Termux either by clicking the "exit" button in the notification it creates or by running the `exit` command.

To start the downloader again, open Termux and run `./start.sh`.

### The Hard Way:

This method involves hosting an instance of [TheOnlyWayUp](https://github.com/TheOnlyWayUp)'s `WattpadDownloader`.

**This method is only available for a select few devices running Android 16.**

1) Enable the Android Developer Mode.

Open your settings app and find the "About phone" option.

Scroll down to the bottom of the page and find the "Build number".

Repeatedly tap the "Build number". It won't appear to do anything at first, but you will start seeing messages about Developer Mode. Continue tapping until you get the message: "You are now a developer!"

2) Open the "Developer options".

Open your settings app and find the "System" option.

Near the bottom of the page find the "Developer options".

Under the "Debugging" header, find the "Linux development environment" option.

*This page has a **lot** of options, it might take some searching*

Open the page and enable the feature.