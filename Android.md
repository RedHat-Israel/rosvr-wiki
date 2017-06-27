> make sure to download the right versions of all the tools and libraries in our Requirements page.>
 
> you may have to reset unity during the steps.>

# How to setup android on unity:
1) download and install unity

2) Click on File -> Build Settings -> on the left corner of the window you can see several platforms -> click on android.
there you will see "no android module loaded" and below a link to download page. Click on that link. It will download your Android-Unity-Setup. Install it and reset unity.

3)Click on Edit -> Preferences -> External tools. At the Bottom you will see Android and below sdk, jdk, ndk.

4)At this point you need to download the following things:

**A)JDK(Java Development Kit) - [Java Development Kit Download]**(http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

this link will open you an Oracle page.

Scroll down until you see the headline-

**Java SE Development Kit <8u131>(current version)**

sign the "Accept Licence Agreement" and download the jdk according to your Operating System(OS) and follow the installer instruction.

**B)Android SDK(Software Development Kit) - [Android SDK download link](https://androidsdkoffline.blogspot.co.il/p/android-sdk-tools.html)**

Click the above link.

**You do not need to download android studio**

download the Android sdk according to your Operating System(OS).

export the zip into a folder.

open the command line at this folder and go to the bin folder using  - cd bin

the run these commands -

sdkmanager build-tools;23.0.0

sdkmanager extras;google;usb_driver

sdkmanager platform-tools

**C)Android NDK(Native Development Kit) - [Android NDK download link]**(https://developer.android.com/ndk/downloads/index.html#stable-downloads)

Click on the above link or this link for older versions -  [older versions]
(https://developer.android.com/ndk/downloads/older_releases.html)

and download the version which specified in the Requirements page according to your OS.
Unity requires the 10e version.

5)Since you have downloaded the Development kits go to Unity and open Edit -> Preferences -> External Tools
and fill the path of the Development Kits' location according to the specified Development Kit. 

6)Go to Edit -> Project Settings -> Editor and under the Unity Remote change the device to any android device.

7)Download the Google VR SDK for Unity through this link - [Download](https://developers.google.com/vr/unity/download)
After the downloading run the installer. In the installer it will open you a window inside Unity, click import.

This will set your google cardboard option in the VR support, and will add the GVR Assets.

8) Go to Edit -> Project Settings -> Player -> Other Settings

Scroll down to the Rendering and click on the Virtual Reality Support, click on the little plus(+) and choose cardboard.

Scroll down to Identification and change the minimum API to at least 19.

And that's it. now you can build your Android VR apps :)

Unity might ask you to update the SDK API so agree to it.
