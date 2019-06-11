FROM ruby:2.6.3-alpine3.8

ARG APP_ROOT=/container1
WORKDIR $APP_ROOT

RUN apk add --no-cache \
      build-base \
      curl-dev \
      libxml2-dev \
      libxslt-dev \
      linux-headers \
      less \
      mysql-dev \
      nodejs \
      ruby-dev \
      tzdata \
      yaml \
      yaml-dev

ADD Gemfile Gemfile.lock ./
COPY . ./
RUN bundle install
