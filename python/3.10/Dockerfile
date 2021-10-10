FROM        cubecoders/ampbase

LABEL       author="Torsten Widmann" maintainer="info@goover.de"

RUN         apt update \
            && apt -y install git gcc g++ ca-certificates dnsutils curl tar iproute2 ffmpeg procps  \
            && apt -y install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libsqlite3-dev libreadline-dev libffi-dev libbz2-dev \
            && curl -O https://www.python.org/ftp/python/3.9.7/Python-3.10.0.tar.xz \
            && tar -xf Python-3.10.0.tar.xz
RUN         cd Python-3.10.0 \
            && ./configure --enable-optimizations \
            && make -j 4 \
            && sudo make altinstall

ENTRYPOINT  ["/ampstart.sh"]
CMD         []
