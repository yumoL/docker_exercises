FROM node:alpine AS builder

WORKDIR /app

ENV API_URL=http://localhost:8000

COPY . .

RUN npm install && \
    npm run build

FROM node:alpine

WORKDIR /app

COPY --from=builder /app/dist/ dist

RUN npm install -g serve && \
    chown -R node /app

USER node

EXPOSE 5000

CMD ["serve","-s","-l","5000","dist"]

