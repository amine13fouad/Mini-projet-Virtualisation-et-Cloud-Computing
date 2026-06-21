FROM rasa/rasa:3.6.20-full

WORKDIR /app

COPY . /app

RUN rasa train

EXPOSE 5005

CMD ["run", "--enable-api", "--cors", "*", "--debug"]