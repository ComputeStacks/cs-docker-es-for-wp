FROM nginx:stable

COPY docker-entrypoint.sh /
COPY nginx.conf /etc/nginx/nginx.conf
COPY nginx-lb /usr/local/bin/

RUN set -ex; \
    \
    apt-get update; \
    apt-get install -y \
            openssl \
            ca-certificates \
    ; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
    ; \
    chmod +x /docker-entrypoint.sh \
    && chmod +x /usr/local/bin/nginx-lb

ENTRYPOINT [ "/docker-entrypoint.sh" ]
CMD ["nginx", "-g", "daemon off;"]
