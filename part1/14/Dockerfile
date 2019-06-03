FROM ruby:2.6.0

ENV RAILS_ENV=production
ENV RAILS_LOG_TO_STDOUT=true
ENV SECRET_KEY_BASE=popporopoo
EXPOSE 3000

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt-get update && apt-get install nodejs yarn -y

WORKDIR /srv/app
COPY ./rails-example-project/ ./rails
WORKDIR /srv/app/rails

RUN bundle install

RUN rails db:migrate
RUN rake assets:precompile

CMD ["rails", "s"]
