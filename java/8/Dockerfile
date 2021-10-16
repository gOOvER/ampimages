FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"

RUN 		    apt update -y \
 			      && apt install -y wget curl ca-certificates openssl git tar sqlite fontconfig tzdata iproute2 sudo
RUN         apt-key adv --keyserver keyserver.ubuntu.com --recv-keys A1EAC8B7 \
            && echo 'deb https://rpardini.github.io/adoptium-deb-installer stable main' > /etc/apt/sources.list.d/rpardini-adoptium.list \
            && apt update \
            && apt install adoptium-8-installer

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
