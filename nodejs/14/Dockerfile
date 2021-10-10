FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"

RUN         apt update \
            && apt -y install curl sudo ffmpeg iproute2 git sqlite3 libsqlite3-dev python3 python3-dev ca-certificates dnsutils tzdata zip \
            # Install NodeJS
            && curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash - \
            && apt update && apt install -y nodejs \
            # Install Yarn
            && curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/yarnkey.gpg >/dev/null \
            && echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
            && apt-get update && apt-get install yarn

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
