FROM ruby:2.5.1

ENV APP_HOME /rails-code

RUN apt-get update -qq
RUN apt-get install -y \
    build-essential \
    libpq-dev \
    nodejs
RUN apt-get clean autoclean
RUN apt-get autoremove -y
RUN rm -rf \
    /var/lib/apt \
    /var/lib/dpkg \
    /var/lib/cache \
    /var/lib/log

RUN mkdir $APP_HOME
WORKDIR $APP_HOME

ADD Gemfile* $APP_HOME/
RUN bundle install

ADD . $APP_HOME

EXPOSE 3000
