FROM rasa/rasa:3.6.20-full

USER root

WORKDIR /app

COPY . /app

RUN chown -R 1001:0 /app && chmod -R g+rw /app

USER 1001

ENV HOME=/tmp
ENV XDG_CACHE_HOME=/tmp/.cache

RUN rasa train

EXPOSE 5005

CMD ["run", "--enable-api", "--cors", "*", "--debug"]