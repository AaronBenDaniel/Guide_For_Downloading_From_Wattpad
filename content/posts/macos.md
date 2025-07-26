---
    Title: 💻 MacOS 💻
    Summary: If you want to download on a Mac.
    weight: 7
---

There are five ways to run a Wattpad downloader on MacOS: wpdl-py-cross (precompiled), wpdl-py-cross (Python), Wattpad_Downloader, Google Colab, and Docker.

*None of these methods have been tested by myself, as I do not have a Mac. They should all work, however.*

### wpdl-py-cross (precomiled):

Using the wpdl-py-cross (precompiled) method if by far the easiest way to download stories from Wattpad. Choose this option if you aren't sure what to pick.

This method involves running a precompiled version of [ZhiFenBL](https://github.com/ZhiFenBL)'s {{< linknewtab "https://github.com/ZhiFenBL/wpdl-py-cross" "wpdl-py-cross" >}}.

1) Download the MacOS `.zip` from  [Github](https://github.com/ZhiFenBL/bin-wpdl-py/releases/download/v0.0.1/macos-build-arm64-v0.0.1.zip).

2) ???

I don't know. I've never used a Mac, but the file you just downloaded should have what you need.

### wpdl-py-cross (Python):

This method involves running [ZhiFenBL](https://github.com/ZhiFenBL)'s {{< linknewtab "https://github.com/ZhiFenBL/wpdl-py-cross" "wpdl-py-cross" >}} using a python virtual environment.

1) Download and run the {{< linknewtab "https://www.python.org/ftp/python/3.13.5/python-3.13.5-macos11.pkg" "Python installer" >}}.

2) Clone {{< linknewtab "https://github.com/ZhiFenBL/wpdl-py-cross" "wpdl-py-cross" >}}:

```
git clone https://github.com/ZhiFenBL/wpdl-py-cross
cd wpdl-py-cross
```

3) Create a Python virtual environment:

```
mkdir venv
python3 -m venv venv
```

4) Activate the virtual environment:

```
source venv/bin/activate
```

5) Install `uv`:

```
pip install uv
```

6) Run wpdl-py-cross:

```
uv run flet run
```

**Follow steps 4 and 6 to run `wpdl-py-cross` again**

### Wattad_Downloader:

This method involves running [AaronBenDaniel](https://github.com/AaronBenDaniel)'s {{< linknewtab "https://github.com/AaronBenDaniel/Wattpad_Downloader" "Wattpad_Downloader" >}} using a python virtual environment.

1) Download and run the {{< linknewtab "https://www.python.org/ftp/python/3.13.5/python-3.13.5-macos11.pkg" "Python installer" >}}.

2) Clone {{< linknewtab "https://github.com/AaronBenDaniel/Wattpad_Downloader" "Wattpad_Downloader" >}}:

```
git clone https://github.com/AaronBenDaniel/Wattpad_Downloader
cd Wattpad_Downloader
```

3) Create a Python virtual environment:

```
mkdir venv
python3 -m venv venv
```

4) Activate the virtual environment:

```
source venv/bin/activate
```

5) Install requirements:

```
pip install -r requirements.txt
```

6) Run wpdl-py-cross:

```
python src/main.py
```

**Follow steps 4 and 6 to run `Wattpad_Downloader` again**

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

1) Install Docker Desktop.

Docker provides their own {{< linknewtab "https://docs.docker.com/desktop/setup/install/mac-install/" "installation guide" >}}, follow it.

2) Run the following command inside of the terminal inside of Docker Desktop (it's in the bottom right)

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