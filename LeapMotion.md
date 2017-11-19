# LeapMotion

LeapMotion is a small device that tracks hands and can display them in Unity

## Driver Installation ##

To use LeapMotion on linux you'll need to install its SDK. Download the
[Linux SDK 2.3.1 ](https://developer.leapmotion.com/sdk/v2).

> Note: *LeapMotion SDK is not open source project*, you will have to register
and agree to terms and conditions to download the SDK.

following:

```bash
tar -xf Leap_Motion_SDK_Linux_2.3.1.tgz
cd LeapDeveloperKit_2.3.1+31549_linux
sudo alien -rv --scripts Leap-*-x64.deb
sudo dnf install leap-2.3.1+31549-2.x86_64.rpm
```

## Running ##

LeapMotion requires running its daemon:

```
sudo -i
leapd
```
To test if LeapMotion works, after starting the daemon and connecting the device,
run the `Visualizer` utility.

## LeapMotion with Unity ##

> Make sure you have LeapMotion drivers installed first.

```
git clone https://github.com/RedHat-Israel/rosvr-leapmotion.git
export ARCH="x86_64"
export PROJECT_ASSETS="rosvr-leapmotion/Assets/Plugins/${ARCH}/"
export LEAP_LIB_PATH="/usr/bin/Playground_Data/Plugins/${ARCH}"
cp "${LEAP_LIB_PATH}/libLeap.so" $PROJECT_ASSETS
cp "${LEAP_LIB_PATH}/libLeapCSharp.so" $PROJECT_ASSETS
```

Now you can open the project in Unity.

*Example Scene*
In Unity, enter the LeapMotion folder and then to the Scenes folder.
Open a scene and press the Play button, put your hands above the LeapMotion
and you should see them in Unity!
