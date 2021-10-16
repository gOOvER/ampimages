FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"

RUN 		    apt update -y \
 			      && apt install -y wget curl ca-certificates openssl git tar sqlite fontconfig tzdata iproute2 sudo
RUN         wget -qO - https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public | sudo apt-key add - \
            && add-apt-repository --yes https://adoptopenjdk.jfrog.io/adoptopenjdk/deb/ buster main \
            && apt update \
            && apt install adoptopenjdk-8-hotspot

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
