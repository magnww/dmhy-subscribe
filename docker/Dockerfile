FROM node:14-alpine

WORKDIR /root

COPY run.sh ./

RUN apk add --no-cache tzdata git

RUN chmod +x /root/run.sh && \
  git clone https://github.com/magnww/dmhy-subscribe.git && \
  yarn global add ./dmhy-subscribe

CMD /root/run.sh
