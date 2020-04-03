FROM alpine

LABEL maintainer Wan-Yu Tang <wanyutang@gmail.com>

RUN apk --update add git less openssh && \
    rm -rf /var/lib/apt/lists/* && \
    rm /var/cache/apk/*

VOLUME /data
WORKDIR /data

# RUN tail -f /dev/null

ENTRYPOINT ["git"]
# CMD ["--help"]
CMD ["--help"]