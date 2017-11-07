FROM debian:latest

RUN mkdir /app
WORKDIR /app

RUN apt-get update && apt-get -y install \
    curl \
	lib32gcc1 \
	&& rm -rf /var/lib/apt/lists/*

RUN curl -sqL "https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz" | tar zxvf -

RUN ./steamcmd.sh +quit

CMD ["/bin/sh"]