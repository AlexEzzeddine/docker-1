FROM debian
RUN apt update && \
	apt install -y gcc vim && \
	cd	/home && \
	echo "#include <stdio.h>\n#include <stdlib.h>\n\
		\nint main(void)\n{\n\n}" > main.c
WORKDIR /home
ENTRYPOINT ["bash", "-l", "-c", "vim main.c && bash"]

# docker build -t test_c .
# docker run -it --rm test_c