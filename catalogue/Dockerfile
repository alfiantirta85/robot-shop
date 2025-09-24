FROM node:14-alpine

ENV INSTANA_AUTO_PROFILE=true

EXPOSE 8080

WORKDIR /opt/server

RUN apk add --update curl && rm -rf /var/cache/apk/*

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

