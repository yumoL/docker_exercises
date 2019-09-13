FROM ubuntu:16.04

WORKDIR /mydir

ENV url http://localhost:8000
COPY . .
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN npm install
RUN npm run build
EXPOSE 5000
CMD API_URL=$url npm start

