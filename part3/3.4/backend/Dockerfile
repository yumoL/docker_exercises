FROM node:alpine

ENV FRONT_URL=http://localhost:5000

WORKDIR /app

COPY . .
RUN npm install && \
    chown -R node /app

USER node

EXPOSE 8000

CMD ["npm","start"]



