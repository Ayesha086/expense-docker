FROM node:20
WORKDIR /opt/backend
COPY  package.json .
COPY *.js .
RUN npm install
#ENV DB_HOST="mysql"
ENV DB_HOST="localhost" 
#because we are using host network
CMD ["node", "index.js"]