# Unity Dependencies #
Unity on linux requires some packages to work properly
## Ubuntu & Debian ##
To install the dependencies on Ubuntu / Debian you'll need to use `apt-get`.
````
sudo apt-get install gconf-service lib32gcc1 lib32stdc++6 libasound2 libc6 libc6-i386 libcairo2 libcap2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libfreetype6 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libgl1-mesa-glx libgl1 libglib2.0-0 libglu1-mesa libglu1 libgtk2.0-0 libnspr4 libnss3 libpango1.0-0 libstdc++6 libx11-6 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxtst6 zlib1g debconf debconf-2.0 npm
````
## Fedora ##
since the packages are named differentially in Fedora, you'll need to run a differant command:
````
sudo dnf install compat-libstdc++-33.i686 alsa-lib.i686 alsa-plugins-pulseaudio.i686 glibc-devel glibc-devel.i686 cairo cairo-devel cairomm-devel libjpeg-turbo-devel pango pango-devel pangomm pangomm-devel libcap-devel.i686 libcap-devel.x86_64 cups-libs.i686 dbus-libs.i686 fontconfig.i686 freetype.i686 libgcc.i686 GConf2 mesa-dri-drivers.i686 mesa-libGLU.i686 gtk2 nss-mdns.i686 pango.i686 libX11.i686 libXcomposite.i686 libXcursor.i686 libXext.i686 libXi.i686 libXrandr.i686 libXrender.i686 zlib.i686 debconf npm libstdc++.i686
````
