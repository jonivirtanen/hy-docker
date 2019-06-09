FROM node

WORKDIR /srv/app/
COPY ./backend-example-docker ./backend
WORKDIR /srv/app/backend
RUN npm install

EXPOSE 8000
CMD [ "npm", "start" ]
