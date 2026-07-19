FROM node:20-alpine

RUN apk add --no-cache git

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm install

COPY . .
RUN npx tsc -b

ENV OUTPUT_DIR=/tmp/output

CMD ["node", "dist/index.js"]
