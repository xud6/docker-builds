FROM easypi/shadowsocks-libev

RUN adduser -S ss
USER ss
ENV LOCAL_ADDR 0.0.0.0
ENV LOCAL_PORT 1080
ENV METHOD aes-256-cfb
ENV PASSWORD myPassword!

CMD ss-local -s "$SERVER_ADDR"  \
             -p "$SERVER_PORT"  \
             -m "$METHOD"       \
             -k "$PASSWORD"     \
             -b "$LOCAL_ADDR"   \
             -l "$LOCAL_PORT"   \
             "$EXTRA_OPTIONS"