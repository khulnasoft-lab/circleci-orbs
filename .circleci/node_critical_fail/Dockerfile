FROM node@sha256:b632a1ec41a0927d19a432c525641b9a4451251d0b0b63f1d764810a562ea4e1

RUN mkdir -p /home/node/ && apt-get update && apt-get -y install curl
COPY ./app/ /home/node/app/

# DEV NOTE: remember to re-enable healthcheck and remove debugging port 22 before final push!

# HEALTHCHECK CMD curl --fail http://localhost:8081/ || exit 1
EXPOSE 8081 22

CMD node /home/node/app/server.js
