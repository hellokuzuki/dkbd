FROM node:alpine

RUN npm install -g redis-commander
RUN echo '{}' > /root/.redis-commander
ENTRYPOINT ["redis-commander"]
EXPOSE 8081
