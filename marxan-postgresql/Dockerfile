FROM postgres:11
LABEL maintainer="hello@vizzuality.com"

ENV PG_MAJOR 11
ENV POSTGIS_MAJOR 2.5
ENV POSTGIS_VERSION 2.5.4+dfsg-1.pgdg90+1

RUN apt-get update \
      && apt-cache showpkg postgresql-$PG_MAJOR-postgis-$POSTGIS_MAJOR \
      && apt-get install -y --no-install-recommends \
           curl \
           unzip \
           less \
           postgresql-$PG_MAJOR-postgis-$POSTGIS_MAJOR=$POSTGIS_VERSION \
           postgresql-$PG_MAJOR-postgis-$POSTGIS_MAJOR-scripts=$POSTGIS_VERSION \
      && rm -rf /var/lib/apt/lists/*