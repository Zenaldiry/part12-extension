
FROM node:24 AS test-stage
WORKDIR /usr/src/app

COPY package*.json ./
RUN npm ci

COPY . .

ENV NODE_ENV=test

RUN npm run test


FROM node:24 AS production-stage

WORKDIR /usr/src/app

COPY package*.json ./

ENV NODE_ENV=production
RUN npm ci --omit=dev


COPY . .

USER node

CMD ["node", "index.js"]
