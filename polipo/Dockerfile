FROM debian

RUN apt-get update && apt-get install polipo -y && apt-get clean
USER proxy
ENV PARENT_PROXY localhost:1080
CMD polipo socksParentProxy="$PARENT_PROXY"