FROM node
ENV MONGODB_URI=mongodb://localhost:27017/fsmooc
ENV PORT=3000
EXPOSE 3000

WORKDIR /srv/app/
COPY ./fs-mooc-blogilista .

RUN apt-get update && apt-get install -y build-essential python 
RUN npm install

CMD [ "npm", "start" ]
