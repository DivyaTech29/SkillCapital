# FROM - Set Base Image
FROM openjdk:17
# LABEL - add custom data, just some key values
LABEL maintainer="Backend API Maintainers <nadavapallisaidivya@gmail.com>"
# ENV - Environment Variable
ENV APP_PATH /backend
ENV APP_VERSION 1.1
# RUN - execute commands
RUN mkdir /backend
# WORKDIR - working directory
WORKDIR /backend
# COPY - copy files to above image
COPY . /backend
# RUN - build related commands
RUN apt install maven
RUN mvn clean package
# EXPOSE - Bind a port to container
EXPOSE 8081
# CMD - default program to start
# CMD ["npm", "start"]
CMD ["java", "-jar", "skil_capital-0.0.1-snapshot.jar"]
