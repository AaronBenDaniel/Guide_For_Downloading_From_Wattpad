---
    Title: 🤖 Android 🤖
    Summary: If you want to download on an Android device.
    weight: 5
---

There are five options for downloading Wattpad stories on Android: wpd.my, wpdl-basic-android, Termux, Google Colab, and Docker.

### wpd.my

[wpd.my](https://wpd.my) is {{< linknewtab "https://github.com/TheOnlyWayUp/" "TheOnlyWayUp" >}}'s public instance of their project, {{< linknewtab "https://github.com/TheOnlyWayUp/WattpadDownloader" "WattpadDownloader" >}}. \
*Note: this website is liable to be removed by Wattpad at any time.*

### wp-epub-rs-emini

This method involves running a precompiled version of [ZhiFenBL](https://github.com/ZhiFenBL)'s {{< linknewtab "https://github.com/WattDownload/wp-epub-rs-emini" "wp-epub-rs-emini" >}}.

1) Go to the [GitHub releases page](https://github.com/WattDownload/wp-epub-rs-emini/releases) and download the file named `android-universal-wprust-*.*.*.apk`.

2) Install the `.apk`.

Open the `.apk` file in your device's file manager, if it says that the app cannot install from unknown sources, enable that feature in your file browser's app settings (via Android, not the built in settings).

3) Open the `WattDL` app.

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

# Docker:

This method involves hosting an instance of [TheOnlyWayUp](https://github.com/TheOnlyWayUp)'s {{< linknewtab "https://github.com/TheOnlyWayUp/WattpadDownloader" "WattpadDownloader" >}} natively on your own machine.

**This method is only available for a select few devices running Android 16 or later.**

### NOTE: When this guide tells you to run a command, DO NOT USE PASTING HINTS FROM YOUR KEYBOARD. It will most likely paste an incomplete command. Long-press and select the `paste` option instead.

### 1) Enable the Android Developer Mode.

Open your settings app and find the "About phone" option.

Scroll down to the bottom of the page and find the "Build number".

Repeatedly tap the "Build number". It won't appear to do anything at first, but you will start seeing messages about Developer Mode. Continue tapping until you get the message: "You are now a developer!"

### 2) Enable the Linux Development Environment.

Open your settings app and find the "System" option.

Near the bottom of the page find the "Developer options".

Under the "Debugging" header, find the "Linux development environment" option.

*This page has a **lot** of options, it might take some searching*

Open the page and enable the feature.

*A new app should have appeared on your phone called `Terminal`*

### 3) Install Docker Engine

Open the `Terminal` app.

***You must enable notification permissions***

Click `Install` \
*This step will take some time to complete* \
*Once everything in finished, a terminal prompt should open.*

Run the following commands: \
*These commands come from [Docker's official Debian install guide](https://docs.docker.com/engine/install/debian/#install-using-the-repository)*
```
# Add Docker's official GPG key:
sudo apt update
yes | sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/debian
Suites: $(. /etc/os-release && echo "$VERSION_CODENAME")
Components: stable
Signed-By: /etc/apt/keyrings/docker.asc
EOF

# Install Docker Engine
sudo apt update
yes | sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### 4) Clone and build `WattpadDownloader`

Run the following command:

```
git clone https://github.com/TheOnlyWayUp/WattpadDownloader
cd WattpadDownloader
sudo docker build -t wpd .
```

### 5) Run `WattpadDownloader`

Run the following command:

```
sudo docker run --rm -p 5042:80 wpd
```

***You should get a notification from the `Terminal` app about port 5042, click `Accept`.***

You should now be able to access your local instance of `WattpadDownloader` at [http://localhost:5042](http://localhost:5042).

When you are finished, simply close the `Terminal` app.

You must open the `Terminal` app and perform step 5 every time you wish to run the downloader after you have closed the app. You may not see the notification again after your first time.

*If something goes wrong and you mess something up (and you don't know how to recover), disable the `Linux Development Environment` option and restart the guide. This will clear the virtual machine's memory and you can start with a fresh install.*