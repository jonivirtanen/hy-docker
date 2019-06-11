FROM node:12-alpine

ENV FRONT_URL=http://localhost:5000

WORKDIR /srv/app/backend
COPY --chown=node ./backend-example-docker .
RUN npm install && chown -R node:node /srv/app/backend

USER node

EXPOSE 8000
CMD [ "npm", "start" ]
