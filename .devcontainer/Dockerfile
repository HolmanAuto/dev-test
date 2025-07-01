FROM mcr.microsoft.com/devcontainers/ruby:3.3.4-bullseye

# Install Node.js, Yarn, and Rails dependencies
RUN apt-get update \
    && apt-get install -y nodejs yarn \
    && gem install rails

# Set default working directory
WORKDIR /workspaces/dev-test
