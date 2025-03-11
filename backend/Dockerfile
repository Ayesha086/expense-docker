#FROM node:20
#Intermediate container(IC-1)
FROM node:20.18.3-alpine3.21
#On top of IC-1 instruction-2 is executed ,and save this layer as 2 image.IC-1 is removed
RUN addgroup -S expense && adduser -S expense -G expense && \
#Create IC-2,On top of IC-1 instruction-3 is executed ,and save this layer as 3 image.IC-2 is removed
         mkdir /opt/backend && \
          chown -R expense:expense /opt/backend
WORKDIR /opt/backend
ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
USER expense
#because we are using host network
COPY  package.json ./
COPY *.js ./
RUN npm install
CMD ["node", "index.js"]
