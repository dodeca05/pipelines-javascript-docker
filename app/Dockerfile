# syntax=docker/dockerfile:1

FROM ecrdev.clouz.io/openshift/nodejs:18-dev
ENV NODE_ENV=production

WORKDIR /app

COPY ["package.json", "package-lock.json*", "./"]

RUN npm install --production

COPY . .

EXPOSE 8080
CMD [ "node", "server.js" ]
