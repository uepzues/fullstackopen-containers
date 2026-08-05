FROM node:lts-trixie-slim

WORKDIR /usr/src/app

COPY --chown=node:node . .

RUN npm ci

ENV DEBUG=todo_app:*

USER node

CMD ["npm", "start"]