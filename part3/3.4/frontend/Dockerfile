FROM node:alpine

ENV API_URL=http://localhost:8000

WORKDIR /app

COPY . .
RUN npm install && \
    chown -R node /app

USER node

EXPOSE 5000

CMD ["npm","start"]

