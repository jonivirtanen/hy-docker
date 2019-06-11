FROM node:12-alpine AS build

WORKDIR /srv/app/frontend
COPY ./frontend-example-docker/ ./
RUN npm install &&\
    API_URL=http://localhost:8000 npm run build

FROM node:12-alpine
WORKDIR /srv/app/frontend
COPY --chown=node:node --from=build /srv/app/frontend/dist ./dist/
COPY --chown=node:node --from=build /srv/app/frontend/node_modules ./node_modules
RUN npm install -g serve
USER node

EXPOSE 5000
CMD [ "serve", "-s", "-l", "5000", "dist" ]
