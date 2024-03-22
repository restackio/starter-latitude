FROM node:18.17 as builder

WORKDIR /usr/src/app

RUN npm install -g @latitude-data/cli

COPY latitude.json ./latitude.json

RUN latitude prepare

COPY .latitude/app/package*.json ./

RUN npm install

COPY .latitude/app .

RUN npm run build

FROM node:18.17 as runner
WORKDIR /app

COPY --from=builder /usr/src/app .

ENV PORT 3500

CMD node /app/build/index.js

EXPOSE 3500