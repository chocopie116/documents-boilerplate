FROM haskell:7.8

RUN set -ex \
    && apt-get update -y \
    && apt-get install -y \
        fonts-ipafont \
        graphviz \
        locales \
        imagemagick \
        task-japanese \
    && echo "ja_JP.UTF-8 UTF-8" > /etc/locale.gen \
    && locale-gen \
    && update-locale LANG=ja_JP.UTF-8 \
    && apt-get clean \
    && rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/*

RUN set -ex \
    && cabal update \
    && cabal install erd \
    && rm -rf ~/.cabal/packages ~/.cabal/logs

WORKDIR  /srv
