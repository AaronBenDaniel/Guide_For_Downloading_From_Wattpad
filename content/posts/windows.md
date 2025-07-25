---
    Title: 🪟 Windows 🪟
    Summary: If you want to download on a Windows machine.
    weight: 6
---

There are five ways to run a Wattpad downloader on Windows: wpdl-py-cross (precompiled), wpdl-py-cross (Python), Wattpad_Downloader, Google Colab, and Docker.

*All of these methods have been tested on *Windows 11 only*. While they will most likely work on Windows 10, there is no guarantee.*

### wpdl-py-cross (precomiled):

Using the wpdl-py-cross (precompiled) method if by far the easiest way to download stories from Wattpad. Choose this option if you aren't sure what to pick.

This method involves running a precompiled version of [ZhiFenBL](https://github.com/ZhiFenBL)'s `wpdl-py-cross`.

1) Download the Windows executable .zip from  [Github](https://github.com/ZhiFenBL/wpdl-py-cross/actions/runs/16499441334/artifacts/3607095145).

2) Extract the `.zip` file.

3) Run the `wpdl_py_desktop.exe` file.

### wpdl-py-cross (Python):

This method involves running [ZhiFenBL](https://github.com/ZhiFenBL)'s `wpdl-py-cross` using a python virtual environment.

*This guide is incomplete.*

### Wattad_Downloader:

This method involves running [AaronBenDaniel](https://github.com/AaronBenDaniel)'s `Wattpad_Downloader` using a python virtual environment.

*This guide is incomplete.*

### Google Colab:

This method involves hosting an instance of [TheOnlyWayUp](https://github.com/TheOnlyWayUp)'s `WattpadDownloader` on a Google Colab virtual machine.

*Note: This method requires a Google Account. If your account is part of a managed organization (work, school, etc) your account may not be able to use Google Colab.*

*Disabling third-party cookies can interfere with this method, make sure to enable them when you use this script.*

1) Open {{< linknewtab "https://colab.research.google.com/drive/15BVtjtboLrzTrnZ-9lQIKQaiMPR49H9g" "colab.research.google.com/drive/15BVtjtboLrzTrnZ-9lQIKQaiMPR49H9g" >}}.

2) Click the triangle "run" button in the top left.

3) Scroll down to the bottom of the page and ***WAIT***. The server needs a few minutes to start up.

The WattpadDownloader interface should appear after a few minutes and can be used as normal.

### Docker:

This method involves hosting an instance of [TheOnlyWayUp](https://github.com/TheOnlyWayUp)'s `WattpadDownloader` natively on your own machine.

1) [Download Docker Desktop](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe).

2) Install Docker Desktop.

Docker provides their own {{< linknewtab "https://docs.docker.com/desktop/setup/install/windows-install/#install-docker-desktop-on-windows" "installation guide" >}}, follow it.

3) Run the following command inside of the terminal inside of Docker Desktop (it's in the bottom right)

`docker run --restart=unless-stopped -p 5042:80 sowansow/wattpaddownloader:latest`

If that fails, saying something along the lines of "permission denied" instead run

`sudo docker run --restart=unless-stopped -p 5042:80 sowansow/wattpaddownloader:latest`

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