FROM node:12-bullseye
WORKDIR /app
RUN apt-get update && apt-get install -y python g++ make && \
    groupadd dev && useradd -m -g dev leandro
COPY package.json ./ 
COPY yarn.lock ./
RUN yarn install --production || npm install
COPY . .
RUN npm rebuild sqlite3
RUN mkdir -p /app/data && chown -R leandro:dev /app/data
USER leandro
EXPOSE 3000
CMD ["node", "src/index.js"]