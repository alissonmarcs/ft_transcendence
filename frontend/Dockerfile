FROM alpine

WORKDIR /app
COPY ./start.sh .
RUN apk add --no-cache nodejs npm && chmod +x ./start.sh