## ---------------------------------------------
# Generic Wine image with Steam support
# ---------------------------------------------
FROM    cubecoders/ampbase

LABEL   author="Torsten Widmann" maintainer="info@goover.de"

## install required packages
RUN     dpkg --add-architecture i386
RUN     apt update
RUN     apt install -y --no-install-recommends wget iproute2 gnupg2 software-properties-common libntlm0 winbind xvfb xauth python3 libncurses5-dev:i386 libncurses6 dbus libgdiplus lib32gcc-s1
RUN     apt install -y alsa-tools libpulse-dev libasound2 libao-common gnutls-bin gnupg locales numactl
RUN     useradd -d /home/container -m container

# Install wine and with recommends
RUN     sh -c 'echo " deb https://dl.winehq.org/wine-builds/debian/ bullseye main" >> /etc/apt/sources.list.d/wine.list'
RUN     wget -nc https://dl.winehq.org/wine-builds/winehq.key
RUN     apt-key add winehq.key
RUN     apt update
RUN     apt install --install-recommends winehq-stable cabextract -y

# Set up Winetricks
RUN	    wget -q -O /usr/sbin/winetricks https://raw.githubusercontent.com/Winetricks/winetricks/master/src/winetricks
RUN     chmod +x /usr/sbin/winetricks

ENTRYPOINT  ["/ampstart.sh"]
CMD         []