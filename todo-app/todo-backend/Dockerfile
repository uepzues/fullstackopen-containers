FROM node:lts-trixie-slim

RUN apt-get update && apt-get install -y --no-install-recommends dumb-init

ENV NODE_ENV production

WORKDIR /usr/src/app

COPY --chown=node:node . .

RUN npm ci --only=production

ENV DEBUG=todo_app:*

USER node

ENTRYPOINT [ "/usr/bin/dumb-init", "--" ]

CMD ["npm", "start"]