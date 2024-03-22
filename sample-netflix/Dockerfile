FROM node:18.17 as builder

WORKDIR /usr/src/app

COPY latitude.json ./

RUN npm install -g @latitude-data/cli

RUN latitude build --docker --debug

COPY .latitude/app/package*.json ./

RUN npm install

COPY .latitude/app .

RUN npm run build

FROM node:18.17 as runner
WORKDIR /app

COPY --from=builder /usr/src/app .

ENV PORT 3000

CMD node build/index.js

EXPOSE 3000