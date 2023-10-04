FROM alpine:3.18.3
ARG pblink="https://github.com/pocketbase/pocketbase/releases/download/v0.18.9/pocketbase_0.18.9_linux_amd64.zip"
ARG pbfile="pocketbase_0.18.9_linux_amd64.zip"
RUN apk update && apk add wget zip && mkdir /pocketbase

WORKDIR /pocketbase
EXPOSE 8090
RUN wget $pblink && unzip $pbfile 

ENTRYPOINT ["./pocketbase","serve","--http","0.0.0.0:8090"]
