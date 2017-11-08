FROM debian
RUN apt update && \
	apt install -y git vim gcc
WORKDIR /home
ENTRYPOINT ["bash"]

# docker build -t my_linux .
# docker run -it --rm my_linux