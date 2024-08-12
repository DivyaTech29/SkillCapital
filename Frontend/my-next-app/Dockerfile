FROM node:20
LABEL 
ENV APP_PATH /frontend
ENV APP_VERSION 1.1
RUN mkdir \frontend
WORKDIR \frontend
COPY . \frontend
RUN npm install
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
