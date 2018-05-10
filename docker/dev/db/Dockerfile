FROM mariadb

RUN apt-get update \
    && apt-get install -y gzip wget \
    && wget -O test_tree.sql.gz "https://drive.google.com/uc?export=download&id=1FfQb3ZmfQrkdaqw2LY1y1K55-DOIdH64" \
    && gunzip test_tree.sql.gz \
    && mysql < test_tree.sql \
    && rm test_tree.sql.gz test_tree.sql \
    && apt-get rm gzip \
    && apt-get rm wget
