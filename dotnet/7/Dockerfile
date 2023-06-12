FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"
LABEL		org.opencontainers.image.source = "https://github.com/gameconfigsx/ampimages"

ENV         DEBIAN_FRONTEND noninteractive

RUN         apt update -y \
            && apt upgrade -y \
            && apt install -y apt-transport-https wget iproute2 \
            && wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb \
            && dpkg -i packages-microsoft-prod.deb \
            && rm packages-microsoft-prod.deb \
            && apt update -y \
            && apt install -y aspnetcore-runtime-7.0 dotnet-sdk-7.0 libgdiplus

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
