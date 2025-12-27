FROM postgres:16

# forcing amd64 pay attention
ADD https://github.com/tensorchord/VectorChord/releases/download/0.5.3/postgresql-16-vchord_0.5.3-1_amd64.deb /temp/
RUN apt-get update && \
    apt install postgresql-16-pgvector -y --no-install-recommends && \
    apt install /temp/postgresql-16-vchord_0.5.3-1_$(dpkg --print-architecture).deb && \
    rm -rf /temp && \
    rm -rf /var/lib/apt/lists/*