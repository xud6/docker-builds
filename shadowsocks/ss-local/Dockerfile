FROM easypi/shadowsocks-libev

CMD ss-local -s "$SERVER_ADDR"  \
             -p "$SERVER_PORT"  \
             -m "$METHOD"       \
             -k "$PASSWORD"     \
             -b "$LOCAL_ADDR"   \
             -l "$LOCAL_PORT"   \
             "$EXTRA_OPTIONS"