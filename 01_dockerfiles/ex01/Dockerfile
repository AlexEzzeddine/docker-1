FROM debian
EXPOSE 10011 9987/udp 30033
RUN apt-get update && \
	apt-get install -y bzip2 wget && \
	wget http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2 && \
	tar xvjf teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2
CMD ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]

# docker run -d --rm -p=10011:10011 -p 9987:9987/udp -p 30033:30033 ts