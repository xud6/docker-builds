FROM debian

RUN apt-get update && apt-get install polipo -y && apt-get clean
RUN useradd -r polipo
RUN mkdir /var/log/polipo && chown -R polipo:polipo /var/log/polipo
USER polipo
ENV PARENT_PROXY localhost:1080
CMD polipo socksParentProxy="$PARENT_PROXY"