FROM ruby:3.2.2

RUN apt-get update -qq && apt-get install -y postgresql-client

WORKDIR /app

COPY Gemfile Gemfile.lock ./
RUN bundle install

COPY . .
CMD ["rails", "server", "-e"]
# sock　file読みにいく