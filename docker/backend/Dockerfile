FROM ruby:3.3.0

ENV LANG=C.UTF-8 \
  TZ=Asia/Tokyo

WORKDIR /app
RUN apt-get update -qq && apt-get install -y nodejs default-mysql-client
COPY ./docker/backend/Gemfile /app/Gemfile
COPY ./docker/backend/Gemfile.lock /app/Gemfile.lock
RUN bundle install

CMD ["rails", "server", "-b", "0.0.0.0"]
