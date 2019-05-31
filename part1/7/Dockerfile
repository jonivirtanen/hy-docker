
FROM ubuntu:latest

WORKDIR /usr/app
RUN apt-get update && apt-get install curl -y
COPY . .
RUN chmod +x curl.sh

ENTRYPOINT ["./curl.sh"]
