FROM ruby

RUN apt-get update && \
	apt-get install -y nodejs && \
	gem install rails

ONBUILD RUN mkdir /opt/app
ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install && \
			rails db:migrate

ONBUILD EXPOSE 3000

# docker build -t ft_rails .