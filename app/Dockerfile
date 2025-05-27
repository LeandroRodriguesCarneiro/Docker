FROM node:12-alpine
WORKDIR /app
RUN addgroup dev && adduser-S -G leandro dev
USER leandro
COPY package.json .
RUN apk add --no-cache python2 g++ make
RUN yarn install --production
COPY . .
CMD ["node", "/src/index.js"]

EXPOSE 3000
