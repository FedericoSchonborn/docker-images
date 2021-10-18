FROM alpine:edge

ARG target=i686
ARG toolchain=GNU

RUN apk add --no-cache build-base bash python3 git curl cmake samurai mpc1-dev mpfr-dev gmp-dev e2fsprogs && \
    git clone --depth=1 https://github.com/SerenityOS/serenity /serenity && \
    cd /serenity && Meta/serenity.sh rebuild-toolchain ${target} ${toolchain}

WORKDIR /serenity
