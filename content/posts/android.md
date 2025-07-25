---
    Title: 🤖 Android 🤖
    Summary: If you want to download on an Android device.
    weight: 5
---

There are four options for running a Wattpad downloader on Android: wpdl-basic-android, Termux, Google Colab, and Docker.

### wpdl-basic-android

This method involves running a precompiled version of [ZhiFenBL](https://github.com/ZhiFenBL)'s {{< linknewtab "https://github.com/ZhiFenBL/wpdl-basic-android" "wpdl-basic-android" >}}. ***THIS IS A CLOSED-SOURCE APP.***

1) Download [wpdl-basic-android](https://github.com/ZhiFenBL/bin-wpdl-basic-android/releases/download/v0.0.1/wpdl-basic-0.0.1-universal.apk).

2) Install the `.apk`.

Open the `.apk` file in your device's file manager, if it says that the app cannot install from unknown sources, enable that feature in your file browser's app settings (via Android, not the built in settings).

3) Open the `WPDL-Basic` app.

### Termux:

{{< youtube Q-2tAbwtjyo >}}

*This guide has a video example.*

This method involves hosting an instance of [Feuerhamster](https://github.com/Feuerhamster)'s [wattpad-downloader](https://github.com/Feuerhamster/wattpad-downloader). Although it actually uses an older fork.

The following steps are based on this guide: https://wpdl-termux.wasmer.app.

1) Install Termux through the [Play Store](https://play.google.com/store/apps/details?id=com.termux), [F-Droid](https://f-droid.org/en/packages/com.termux/), or [GitHub](https://github.com/termux/termux-app/releases).

2) Open Termux and run this command:
```
curl -L https://tinyurl.com/4yjur5xk -o download.sh;/bin/bash download.sh
```

**NOTE: Every character in these commands is important. Do not leave out any periods (.), slashes (/), the semicolon (;), or any other character**.

This will download three scripts that can be used to control the downloader.

3) Run the following command:

```
./install.sh
```

Once this is completed, an instance of `wattpad-downloader` will be running on your device and it can be accessed at **{{< linknewtab "http://localhost:3000" "http://localhost:3000" >}}**.

To stop the downloader, run

```
./stop.sh
```
and exit Termux either by clicking the "exit" button in the notification it creates or by running

```
exit
```

To start the downloader again, open Termux and run

```
./start.sh
```

### Google Colab:

{{< youtube Byf209XnNKU >}}

*This guide has a video example.*

This method involves hosting an instance of [TheOnlyWayUp](https://github.com/TheOnlyWayUp)'s {{< linknewtab "https://github.com/TheOnlyWayUp/WattpadDownloader" "WattpadDownloader" >}} on a Google Colab virtual machine.

*Note: This method requires a Google Account. If your account is part of a managed organization (work, school, etc) you may not be able to use Google Colab.*

*Disabling third-party cookies can interfere with this method, make sure to enable them when you use this script.*

1) Open {{< linknewtab "https://colab.research.google.com/drive/15BVtjtboLrzTrnZ-9lQIKQaiMPR49H9g" "colab.research.google.com/drive/15BVtjtboLrzTrnZ-9lQIKQaiMPR49H9g" >}}.

2) Click the triangle "run" button in the top left.

3) Scroll down to the bottom of the page and ***WAIT***. The server needs a few minutes to start up.

The WattpadDownloader interface should appear after a few minutes and can be used as normal.

**It may sometimes fail on its first run. If the interface has not appeared and the output tells you it should have, try stopping the program and starting it again.**

To stop the downloader, close the tab. To start it again, follow these steps again.

### Docker:

This method involves hosting an instance of [TheOnlyWayUp](https://github.com/TheOnlyWayUp)'s {{< linknewtab "https://github.com/TheOnlyWayUp/WattpadDownloader" "WattpadDownloader" >}} natively on your own machine.

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

*This guide is incomplete.*