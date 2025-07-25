---
    Title: 🪟 Windows 🪟
    Summary: If you want to download on a Windows machine.
    weight: 6
---

There are five ways to run a Wattpad downloader on Windows: wpdl-py-cross (precompiled), wpdl-py-cross (Python), Wattpad_Downloader, Google Colab, and Docker.

*All of these methods have been tested on *Windows 11 only*. While they will most likely work on Windows 10, there is no guarantee.*

### wpdl-py-cross (precomiled):

Using the wpdl-py-cross (precompiled) method if by far the easiest way to download stories from Wattpad. Choose this option if you aren't sure what to pick.

This method involves running a precompiled version of [ZhiFenBL](https://github.com/ZhiFenBL)'s {{< linknewtab "https://github.com/ZhiFenBL/wpdl-py-cross" "wpdl-py-cross" >}}.

1) Download the Windows `.zip` from  {{< linknewtab "https://github.com/ZhiFenBL/bin-wpdl-py/releases/download/v0.0.1/windows-build-v0.0.1.zip" "GitHub" >}}.

2) Extract the `.zip` file.

3) Run the `wpdl_py_desktop.exe` file.

### wpdl-py-cross (Python):

This method involves running [ZhiFenBL](https://github.com/ZhiFenBL)'s {{< linknewtab "https://github.com/ZhiFenBL/wpdl-py-cross" "wpdl-py-cross" >}} using a python virtual environment.

1) Open `PowerShell`.

2) Run

```
python --version
```

If the Microsoft Store opens to `Python 3.13`, install it, and continue to the next step.

If it shows something like

```
Python 3.13.5 (tags/v3.13.5:6cb20a2, Jun 11 2025, 16:15:46) [MSC v.1943 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

then run
```
exit()
```
and continue to the next step

3) Download [wpdl-py-cross]()

*This guide is incomplete.*

### Wattad_Downloader:

This method involves running [AaronBenDaniel](https://github.com/AaronBenDaniel)'s {{< linknewtab "https://github.com/AaronBenDaniel/Wattpad_Downloader" "Wattpad_Downloader" >}} using a python virtual environment.

1) Open `PowerShell`.

2) Run

```
python --version
```

If the Microsoft Store opens to `Python 3.13`, install it, and continue to the next step.

If it shows something like

```
Python 3.13.5 (tags/v3.13.5:6cb20a2, Jun 11 2025, 16:15:46) [MSC v.1943 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

then continue to the next step

3) Download [Wattpad_Downloader](https://github.com/AaronBenDaniel/Wattpad_Downloader/archive/refs/heads/main.zip)

4) Extract the `.zip` file

5) Inside the extracted files, in the folder with the files `src`, `README.md`, and `requirements.txt`, etc, make a folder called `venv`.

6) Open the folder with the files in the Terminal by right clicking in the file explorer **while not hovering over a file** and selecting the option "Open in Terminal"

7) Create a Python virtual environment:

```
python -m venv venv
```

8) Activate the virtual environment:

```
./venv/Scripts/Activate.bat
```

9) Install requirements:

```
pip install -r requirements.txt
```

10) Run Wattpad_Downloader:

```
python src/main.py
```

**Follow steps 6, 8, and 10 to run `Wattpad_Downloader` again**

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

1) [Download Docker Desktop](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe).

2) Install Docker Desktop.

Docker provides their own {{< linknewtab "https://docs.docker.com/desktop/setup/install/windows-install/#install-docker-desktop-on-windows" "installation guide" >}}, follow it.

3) Run the following command inside of the terminal inside of Docker Desktop (it's in the bottom right)

```
docker run --restart=unless-stopped -p 5042:80 sowansow/wattpaddownloader:latest
```

If that fails, saying something along the lines of "permission denied" instead run

```
sudo docker run --restart=unless-stopped -p 5042:80 sowansow/wattpaddownloader:latest
```

This might ask for a password, use the password of whatever administrator account your computer has.

This command will automatically download WattpadDownloader and run it.

Once you've completed these steps, if everything worked right you should see something like this:

```
INFO:     Uvicorn running on http://0.0.0.0:80 (Press CTRL+C to quit)
INFO:     Started parent process [1]
INFO:     Started server process [100]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Started server process [93]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
...
```

If you see that, you can access your self-hosted instance of WattpadDownloader by going to [localhost:5042](http://localhost:5042/).