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
git clone github.com/atejeda/leap-fedora-rpm.git # via https
git clone git@github.com:atejeda/leap-fedora-rpm.git # via ssh
mv LeapDeveloperKit_*_linux/*.deb leap-fedora-rpm/SOURCES/
cd leap-fedora-rpm
make clean all
sudo dnf install RPMS/*/Leap*.rpm
````

