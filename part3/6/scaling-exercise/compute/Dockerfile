FROM node:12-alpine

WORKDIR /usr/app

COPY --chown=node . .

RUN npm ci

USER node
EXPOSE 3000

CMD ["node", "./index.js"] 
