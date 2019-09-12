FROM ubuntu:16.04

WORKDIR /mydir

ENV url http://localhost:8000

COPY . .
RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm install && \
    npm run build && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/*

EXPOSE 5000
CMD API_URL=$url npm start

