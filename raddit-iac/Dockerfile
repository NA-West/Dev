From ruby:2.3

Run apt-get update -qq && \
    apt-get install -y build-essential

ENV APP_Home /app
RUN mkdir ${APP_Home}
WORKDIR ${APP_Home}
COPY raddit-app/raddit/Gemfile* ${APP_Home}/
RUN bundle install

ADD raddit-app/raddit/ ${APP_Home}
CMD ["puma"]