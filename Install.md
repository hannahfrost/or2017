# Install docker
### For Windows
\* Docker for Windows requires 64bit Windows 10 Pro and Microsoft Hyper-V. [Details](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install)

Download this file: https://download.docker.com/win/stable/InstallDocker.msi

Double click on the downloaded file to run the installer.

Open a command prompt (Press windows + r and type "cmd", or go to Start Menu > Windows System > Command Prompt) and type `docker run hello-world` to verify installation was correct.

You should see a message that states:
```
Hello from Docker!
This message shows that your installation appears to be working correctly.
```

### For Mac
\* Docker for Mac requires OS X El Capitan 10.11 or newer macOS release running on a 2010 or newer Mac, with Intel’s hardware support for MMU virtualization. The app will run on 10.10.3 Yosemite, but with limited support.

Download this file: https://download.docker.com/mac/stable/Docker.dmg

Double-click Docker.dmg to open the installer, then drag Moby the whale to the Applications folder.
Double-click Docker.app in the Applications folder to start Docker.

Open a terminal and type `docker run hello-world` to verify installation was correct.

You should see a message that states:
```
Hello from Docker!
This message shows that your installation appears to be working correctly.
```


### For Linux

Follow the guide for your distro at https://docs.docker.com/engine/installation/#supported-platforms


### If you have an older version of mac or windows try docker-machine:

```
docker-machine create --driver virtualbox containerhost
eval "$(docker-machine env containerhost)"
```


Open a terminal and type `docker run hello-world` to verify installation was correct.

You should see a message that states:
```
Hello from Docker!
This message shows that your installation appears to be working correctly.
```
