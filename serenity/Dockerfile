FROM alpine:edge

ARG target=i686
ARG toolchain=GNU

RUN apk add git bash curl build-base cmake samurai mpc1-dev mpfr-dev gmp-dev e2fsprogs
RUN git clone --depth=1 https://github.com/SerenityOS/serenity /serenity
RUN cd /serenity && Meta/serenity.sh rebuild-toolchain ${target} ${toolchain}

WORKDIR /serenity
