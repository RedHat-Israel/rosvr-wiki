# LeapMotion #
LeapMotion is a small device that tracks hands and can display them in Unity
## Driver Installation ##
To use LeapMotion on linux you'll need to install some drivers

first, download the linux binary [from here](https://developer.leapmotion.com/sdk/v2) and unzip it. After that, enter to the unzipped folder (there should be another folder there).

make sure that you're in the correct directory (`Leap_Motion_SDK_Linux_2.3.1` in the current version, the beginning should be the same in all versions)

### Debian & Ubuntu ###
Debian and Ubuntu users can use `dpkg` to install the .deb package.
````
cd LeapDeveloperKit_*_linux
sudo dpkg -i Leap-*-x86.deb # for 32 bit
sudo dpkg -i Leap-*-x64.deb # for 64 bit
````
### Fedora ###
Fedora users have to convert the .deb file to .rpm first. you'll need to make sure that you have `rpmbuild`:
````
sudo dnf install rpm-build rpm-build-libs
````
please note that the generated rpm arch is the same of your os (32 bit os will generate a 32-bit rpm file)
````
git clone https://github.com/bugzy/leap-fedora-rpm.git # via https
mv LeapDeveloperKit_*_linux/*.deb leap-fedora-rpm/SOURCES/
cd leap-fedora-rpm
make clean all
sudo dnf install RPMS/*/Leap*.rpm
````
### Running the daemon ###
You'll also need to run the daemon for LeapMotion to work properly:
````
sudo systemctl start leap.service
sudo systemctl enable leap.service
````

### Testing ###
After installing the drivers, you can test the LeapMotion by the `Visualizer` Utility:
````
Visualizer
````
## LeapMotion with Unity ##
LeapMotion can work with Unity on Linux too!
### Downloading the examples ###
First, you'll need to download the Unity assets by running this command:
````
git clone https://github.com/leapmotion/LeapMotionCoreAssets.git # via https
````
after downloading the assets, import them to Unity (`Open` and then select the folder).
### Adding the linux libraries to the Unity project ###
cd to the directory with the unzipped folder (that had the `.deb` files) and run the following commands (where <unity project root> is the directory of your cloned unity project):
````
cp LeapDeveloperKit_2.3.1+31549_linux/LeapSDK/lib/x86/libLeap.so <unity project root>/Assets/Plugins/x86/
cp LeapDeveloperKit_2.3.1+31549_linux/LeapSDK/lib/x64/libLeap.so <unity project root>/Assets/Plugins/x86_64/
cp LeapDeveloperKit_2.3.1+31549_linux/LeapSDK/lib/x86/libLeapCSharp.so <unity project root>/Assets/Plugins/x86/
cp LeapDeveloperKit_2.3.1+31549_linux/LeapSDK/lib/x64/libLeapCSharp.so <unity project root>/Assets/Plugins/x86_64/
````
### Running an example ###
In Unity, enter the LeapMotion folder and then to the Scenes folder. open a scene and press the Play button, put your hands above the LeapMotion and you should see them in Unity!
