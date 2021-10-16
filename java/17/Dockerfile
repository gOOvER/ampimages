FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"

RUN 		    apt update -y \
 			      && apt install -y wget curl ca-certificates openssl git tar sqlite fontconfig tzdata iproute2 sudo apt-transport-https dirmngr gnupg software-properties-common
RUN         wget -qO - https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public | apt-key add -
RUN         add-apt-repository --yes https://adoptopenjdk.jfrog.io/adoptopenjdk/deb/
RUN         apt update
RUN         apt install adoptopenjdk-17-hotspot -y

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
