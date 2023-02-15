FROM node:14-alpine

WORKDIR /root

COPY run.sh ./

RUN apk add --no-cache tzdata git

RUN chmod +x /root/run.sh && \
  git clone -b qbittorrent-v2 https://github.com/magnww/dmhy-subscribe.git && \
  yarn global add /root/dmhy-subscribe && \
  rm -rf /root/dmhy-subscribe

CMD /root/run.sh
