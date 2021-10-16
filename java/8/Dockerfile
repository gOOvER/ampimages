FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"

RUN 		    apt update -y \
 			      && apt install -y wget curl ca-certificates openssl git tar sqlite fontconfig tzdata iproute2 sudo
RUN         apt-key adv --keyserver keyserver.ubuntu.com --recv-keys A1EAC8B7
RUN         echo 'deb https://rpardini.github.io/adoptium-deb-installer stable main' > /etc/apt/sources.list.d/rpardini-adoptium.list \
RUN         apt update \
            && apt install -y adoptium-8-installer

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
