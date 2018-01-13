FROM debian

RUN apt-get update && apt-get install polipo && apt-get clean
RUN useradd -r polipo
USER polipo
CMD polipo "POLIPO_PARAM"