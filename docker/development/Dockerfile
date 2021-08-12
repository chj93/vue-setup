FROM node:12.13.0-alpine

RUN apk add --no-cache \
    bash \
    git \
    tzdata \
  && yarn global add @vue/cli@latest

COPY docker/development/docker-entrypoint.sh /
RUN chmod +x /docker-entrypoint.sh
EXPOSE 8080/tcp
WORKDIR /app

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["yarn", "serve"]
