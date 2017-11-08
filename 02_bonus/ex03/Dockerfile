FROM ubuntu

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5 && \
	echo "deb [ arch=amd64,arm64 ] http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/testing multiverse" | tee /etc/apt/sources.list.d/mongodb-org-3.6.list && \
	apt-get update && \
	apt-get install -y mongodb-org && \
	mkdir -p /data/db

WORKDIR /data/db

CMD ["mongod" , "--bind_ip_all"]

EXPOSE 27017

# docker build -t test_mongo .
# docker run --rm -it -p 27017:27017 test_mongo