FROM debian:latest

ENV TSM3=http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get install -y --no-install-recommends apt-utils
RUN apt-get install -y wget bzip2
RUN wget -q -O teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2 ${TSM3}
RUN tar xfvj teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2

EXPOSE 9987/udp 30033/tcp 10011/tcp 41144/tcp

ENTRYPOINT sh ./teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh
#then run in terminal docker -t -i ID start
# ID look at the ENTRYPOINT
