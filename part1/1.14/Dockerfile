FROM ruby:2.6.0

WORKDIR /mydir

COPY . .
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN bundle install
RUN rails db:migrate
CMD rails s
