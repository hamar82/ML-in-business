FROM python:3.9
LABEL maintainer="hamar82@gmail.com"
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
RUN python3 -m nltk.downloader punkt
RUN python3 -m nltk.downloader wordnet
EXPOSE 8180
EXPOSE 8181
VOLUME /app/app/models
COPY ./docker-entrypoint.sh /
RUN chmod +x /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh"]