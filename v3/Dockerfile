FROM wenxinhe/cucumber:v2


RUN apt-get update && apt-get install -y qt5-qmake qt5-default libqt5webkit5-dev

RUN gem install --no-rdoc --no-ri --verbose capybara-webkit

RUN gem install --no-rdoc --no-ri --verbose headless 
