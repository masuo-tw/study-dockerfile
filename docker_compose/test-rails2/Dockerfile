FROM ruby:2.5.3

RUN apt-get update -qq && \
    apt-get install -y build-essential \
                       libpq-dev \       
                       nodejs            

RUN mkdir /rails2 
WORKDIR /rails2

ADD ./Gemfile $APP_DIR/Gemfile
ADD ./Gemfile.lock /rails2/Gemfile.lock

RUN bundle install
ADD . /rails2

