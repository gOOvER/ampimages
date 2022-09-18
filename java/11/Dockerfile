FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"
LABEL		org.opencontainers.image.source = "https://github.com/gameconfigsx/ampimages"

RUN 		apt update -y
RUN			apt install -y wget curl ca-certificates openssl git tar sqlite3 fontconfig tzdata iproute2 sudo apt-transport-https dirmngr gnupg software-properties-common
RUN         mkdir -p /etc/apt/keyrings
RUN         wget -O - https://packages.adoptium.net/artifactory/api/gpg/key/public | tee /etc/apt/keyrings/adoptium.asc
RUN         echo "deb [signed-by=/etc/apt/keyrings/adoptium.asc] https://packages.adoptium.net/artifactory/deb $(awk -F= '/^VERSION_CODENAME/{print$2}' /etc/os-release) main" | tee /etc/apt/sources.list.d/adoptium.list
RUN         apt update
RUN         apt install temurin-11-jdk -y

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
