FROM debian

RUN apt-get update && apt-get install polipo -y && apt-get clean
RUN useradd -r polipo
USER polipo
ENV PARENT_ADDR localhost
ENV PARENT_PORT 1080
CMD polipo socksParentProxy="$PARENT_ADDR":"$PARENT_PORT"