#To execute docker build -t APPNAME .

# We need to pass it in docker build
# docker build -t helloexpress:arg --build-arg NODE_ENV_ARG=production .
# We need to check if this arg has setted correctly
# so, its a good idea enteder on container and check this arg
ARG NODE_ENV_ARG

ENV NODE_ENV=NODE_ENV_ARG

FROM node:18-slim

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "main.js"]