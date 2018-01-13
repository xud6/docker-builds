FROM alpine:edge

RUN apk --update add polipo && \
    rm -rf /var/cache/apk/* && \
rm -rf /root/.cache

CMD polipo "POLIPO_CONFIG"