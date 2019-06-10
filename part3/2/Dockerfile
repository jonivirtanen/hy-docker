FROM python:alpine

RUN apk --no-cache add --update ffmpeg gcc libc-dev libxml2-dev libxslt-dev \
    curl php7 php7-bcmath php7-curl php7-openssl php7-simplexml && \
    pip install pycryptodomex yle-dl && \
    apk del gcc

WORKDIR /videos

ENTRYPOINT [ "/usr/local/bin/yle-dl" ]

