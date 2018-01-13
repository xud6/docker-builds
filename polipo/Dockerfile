FROM debian

RUN apt-get update && apt-get install polipo -y && apt-get clean
RUN useradd -r polipo
USER polipo
CMD polipo socksParentProxy=localhost:1080