FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && \
    apt install -y build-essential bsdextrautils git python3 libglew-dev libsdl2-dev && \
    rm -rf /var/lib/apt/lists/* && \
    mkdir /sm64ex

WORKDIR /sm64ex

CMD echo 'usage: docker run --rm --mount type=bind,source=SM64EX_DIR,destination=/sm64ex sm64ex:latest make -j<jobs> <flags>'
