# Rails

## Scaffold

`rails new toy_app`

`bundle install`




`rails g scaffold User name:string email:string`

`bundle exec rails db:migrame`

`bin/rails server -p 8000`

`rails g scaffold Micropost content:text user_id:integer`

`bundle exec rails db:migrate`

http://rubydev.ru/2011/10/rubydev_ruby_tutorial_metaprogramming_ruby

https://postmarkapp.com/  Этот сайт написан на руби и рэйлс. Подходит для transactionals emails(реагирует на какое-то событие на сайте). Почтовую рассылку через него делать нельзя. Сразу забанят.

https://github.com/ActiveCampaign/postmark-gem

bulk email messaging подходит для почтовой рассылки.
В каждом письме должна быть кнопка unsubscribe. Если этой кнопки нет - это нарушение terms of service.


https://www.refinerycms.com/ The most popular Ruby on Rails CMS