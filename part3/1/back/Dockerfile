FROM node:12-alpine

WORKDIR /srv/app/backend
COPY ./backend-example-docker .
RUN npm install

ENV FRONT_URL=http://localhost:5000

EXPOSE 8000
CMD [ "npm", "start" ]
