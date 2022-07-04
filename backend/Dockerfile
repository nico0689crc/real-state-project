FROM ruby:3.1.1
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
WORKDIR /real-estate-project/backend
COPY Gemfile /real-estate-project/backend/Gemfile
COPY Gemfile.lock /real-estate-project/backend/Gemfile.lock
RUN bundle install
COPY . /real-estate-project/backend

EXPOSE 3001

CMD rails s -p 3001 -b '0.0.0.0'