FROM openjdk:11.0.3-slim-stretch

MAINTAINER Silvio Haehner <info@sioh.de>

ENV PORT 8010
ENV LT_VERSION 4.5
ADD https://www.languagetool.org/download/LanguageTool-$LT_VERSION.zip /LanguageTool-$LT_VERSION.zip

RUN apt-get -y install unzip && unzip LanguageTool-$LT_VERSION.zip && \
    rm LanguageTool-$LT_VERSION.zip

WORKDIR /LanguageTool-$LT_VERSION

EXPOSE $PORT

CMD java -cp languagetool-server.jar org.languagetool.server.HTTPServer --port $PORT --public --allow-origin "*"
