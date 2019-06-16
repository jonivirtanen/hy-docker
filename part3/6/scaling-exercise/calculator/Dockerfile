FROM node:12-alpine AS build

WORKDIR /usr/app

COPY . .
RUN npm ci && npm run build

FROM node:12-alpine

WORKDIR /usr/app
COPY --from=build --chown=node /usr/app/dist /usr/app/dist
COPY --from=build --chown=node /usr/app/node_modules /usr/app/node_modules

RUN npm install -g serve

USER node
EXPOSE 3000

CMD ["serve", "-s", "-l", "3000", "dist"] 
