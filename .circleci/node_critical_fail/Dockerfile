FROM node@sha256:ca75f977b1c9e9a2cc5480efe5b7df07ce38373316e30b91eeadddb6a025b8a8

RUN mkdir -p /home/node/ && apt-get update && apt-get -y install curl
COPY ./app/ /home/node/app/

# DEV NOTE: remember to re-enable healthcheck and remove debugging port 22 before final push!

# HEALTHCHECK CMD curl --fail http://localhost:8081/ || exit 1
EXPOSE 8081 22

CMD node /home/node/app/server.js
