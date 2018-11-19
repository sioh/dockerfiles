FROM openjdk:8-jre-slim

MAINTAINER Silvio Haehner <info@sioh.de>

ENV PORT 8010
ENV LT_VERSION 4.3
ENV NGRAMS_VERSION 20150819
ENV NGRAMS_LANG de
ADD https://www.languagetool.org/download/LanguageTool-$LT_VERSION.zip /LanguageTool-$LT_VERSION.zip

RUN unzip LanguageTool-$LT_VERSION.zip && \
    rm LanguageTool-$LT_VERSION.zip

WORKDIR /LanguageTool-$LT_VERSION

EXPOSE $PORT

CMD java -cp languagetool-server.jar org.languagetool.server.HTTPServer --port $PORT --public --allow-origin "*"
