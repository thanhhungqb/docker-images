# credit: https://github.com/playniuniu/docker-scratch-gui
# docker build -t scratch-gui .
# docker run -d -p 8080:8601 --name scratch scratch-gui
# note: use with old version of node (<17)
# TODO: use copy to small size of image

FROM node:16.18-alpine as builder
LABEL MAINTAINER="thanhhungqb@gmail.com"

RUN apk add --update --no-cache git
WORKDIR /www
RUN git clone --depth=1 https://github.com/LLK/scratch-gui.git
RUN cd scratch-gui \
    && npm install \
    && npm run build

#FROM node:16.18-alpine
#COPY --from=builder /scratch-gui/build /usr/share/nginx/html

WORKDIR /www/scratch-gui
ENTRYPOINT ["npm", "start"]
