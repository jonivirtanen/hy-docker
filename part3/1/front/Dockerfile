FROM node:12-alpine AS build

WORKDIR /srv/app/frontend
COPY ./frontend-example-docker/ ./
RUN npm install &&\
    API_URL=http://localhost:8000 npm run build

FROM node:12-alpine
WORKDIR /srv/app/frontend
COPY --from=build /srv/app/frontend/dist ./dist/
COPY --from=build /srv/app/frontend/node_modules ./node_modules
RUN npm install -g serve

EXPOSE 5000
CMD [ "serve", "-s", "-l", "5000", "dist" ]
