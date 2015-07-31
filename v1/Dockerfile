# sshd
#
# VERSION               0.0.2

FROM vincent/ubuntu:v3

# utils
RUN apt-get update && apt-get install -y tree patch make g++ zlib1g-dev

RUN apt-get update && apt-get install -y ruby-full

RUN gem sources --remove http://rubygems.org/
RUN gem sources -a http://ruby.taobao.org/
RUN gem sources --list

RUN gem install --no-rdoc --no-ri --verbose cucumber capybara capybara-mechanize rspec
