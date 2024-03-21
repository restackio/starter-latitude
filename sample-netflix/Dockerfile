FROM node:18 as builder

WORKDIR /usr/src/app

COPY .latitude/app/package*.json ./

RUN npm install

COPY .latitude/app .

RUN npm run build

FROM node:18 as runner
WORKDIR /app

COPY --from=builder /usr/src/app .

ENV PORT 80

CMD node /app/build/index.js

EXPOSE 80