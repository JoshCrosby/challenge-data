FROM mariadb

RUN apt-get update \
    && apt-get install -y wget \
    && cd /docker-entrypoint-initdb.d \
    && wget -O test_tree.sql.gz "https://drive.google.com/uc?export=download&id=1FfQb3ZmfQrkdaqw2LY1y1K55-DOIdH64"
