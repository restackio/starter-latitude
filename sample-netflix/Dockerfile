FROM node:18 as builder

WORKDIR /usr/src/app

COPY .latitude/app/package*.json ./

RUN npm install

COPY .latitude/app .

RUN npm run build

FROM node:18 as runner
WORKDIR /app

COPY --from=builder /usr/src/app .

ENV PORT 3000

CMD node build/index.js

EXPOSE 3000