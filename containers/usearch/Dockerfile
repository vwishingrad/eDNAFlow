FROM debian:bookworm-slim

RUN apt-get update && apt-get install -y --no-install-recommends bash ca-certificates curl mawk && rm -rf /var/lib/apt/lists/*

RUN curl -fsSL https://raw.githubusercontent.com/rcedgar/usearch_old_binaries/main/bin/usearch11.0.667_i86linux64 -o /usr/local/bin/usearch && printf 'fa050a3029d33b7b25036a2cc8c6da97  /usr/local/bin/usearch\n' | md5sum -c - && chmod 0755 /usr/local/bin/usearch

LABEL org.opencontainers.image.title="USEARCH 11.0.667, 64-bit"
LABEL org.opencontainers.image.licenses="CC0-1.0"
LABEL org.opencontainers.image.source="https://github.com/vwishingrad/eDNAFlow"
