FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"
LABEL		org.opencontainers.image.source = "https://github.com/gameconfigsx/ampimages"

RUN         apt update \
            && apt -y upgrade \
            && apt install -y apt-transport-https dirmngr gnupg ca-certificates curl sudo
RUN         apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
RUN         echo "deb https://download.mono-project.com/repo/debian stable-buster main" | sudo tee /etc/apt/sources.list.d/mono-official-stable.list
RUN         apt update \
            && apt install -y mono-complete

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
