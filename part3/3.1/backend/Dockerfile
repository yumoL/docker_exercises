FROM ubuntu:16.04

ENV url http://localhost:5000

WORKDIR /mydir

COPY . .
RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm install && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/*

EXPOSE 8000
CMD FRONT_URL=$url npm start

