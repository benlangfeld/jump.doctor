FROM ruby:2.5.0

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update -qqy && apt-get -qqyy install \
    nodejs \
    yarn \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app
ENV BUNDLE_PATH=/usr/local/bundle

COPY Gemfile /app
COPY Gemfile.lock /app
RUN bundle install