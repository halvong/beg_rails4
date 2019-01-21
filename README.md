Beg Rails 4 from Docker for Rails
01/20, Sunday

1. docker run -i -t --rm -v ${PWD}:/usr/src/app ruby:2.5.3 bash
2. cd /usr/src/app
3. gem install rails
4. rails new <rails_app> --skip-test --skip-bundle
5. exit
6. sudo chown $USER:$USER -R <rails_app>
7. docker build -t beg_rails4 .
8. docker run -p 3000:3000 beg_rails4 rails s -b 0.0.0.0
