FROM ubuntu:20.04

RUN apt-get update -y

RUN apt-get install -y curl openjdk-11-jre-headless vim 

RUN curl -sL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs

RUN npm install -g firebase-tools

RUN mkdir /firebase
WORKDIR /firebase
