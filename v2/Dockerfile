FROM wenxinhe/ubuntu-dev:v1


ADD sources.list /etc/apt/sources.list
RUN apt-get update && apt-get install -y patch make g++ zlib1g-dev xvfb ruby-full

RUN gem sources --remove http://rubygems.org/
RUN gem sources -a http://ruby.taobao.org/
RUN gem sources --list

RUN gem install --no-rdoc --no-ri --verbose cucumber capybara capybara-mechanize rspec selenium selenium-client selenium-webdriver

ENV DISPLAY :99

# Install Xvfb init script
ADD xvfb_init /etc/init.d/xvfb
RUN chmod a+x /etc/init.d/xvfb
ADD xvfb-daemon-run /usr/bin/xvfb-daemon-run
RUN chmod a+x /usr/bin/xvfb-daemon-run

RUN apt-get install -y firefox
