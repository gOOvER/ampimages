FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"

RUN         apt update \
            && apt -y install curl sudo ffmpeg iproute2 git sqlite3 libsqlite3-dev python3 python3-dev ca-certificates dnsutils tzdata zip \
            && curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash - \
            && apt update
            && apt install -y nodejs

ENTRYPOINT  ["/ampstart.sh"]
