# Rails


## Create new app

`rails new blog -j esbuild --css bootstrap -a propshaft`

## Hello World on RoR

1. Создаем контроллер для "Hello, World"
`rails g controller Welcome index`
2. Откройте файл app/controllers/welcome_controller.rb и убедитесь что в нем есть следующий код

        class WelcomeController < ApplicationController
            def index
            end
        end

3. Создаем представление для контроллера. В файле `app/views/welcome` создайте файл `index.html.erb` с содержанием:
`Hello, World`

4. Настройте маршруты в файле `config/routes.rb`, чтобы установить корневой маршрут на контроллер  `Welcome`:
```
Rails.application.routes.draw do
  root 'welcome#index'
end
```
5. Запускаем сервер
`./bin/dev`

    Если вы хотите добавить курсоры во всех вхождениях выбранного текста, просто выделите этот текст.
    Затем используйте комбинацию клавиш Ctrl+Shift+L  для быстрого создания курсоров во всех местах, где выбранный текст повторяется.

Тег <span></span> является одним из элементов HTML и используется для определения инлайн-контейнера, который позволяет применять стили, атрибуты и скрипты к части текста или другого контента внутри веб-страницы. Важным свойством тега <span> является то, что он не придаёт особого семантического значения содержимому, который он обрамляет, а просто применяет стили или другие атрибуты к этому содержимому.

https://ionic.io/ionicons

https://infogra.ru/design/krutaya-shpargalka-po-sochetaniyu-tsvetov   Сочетание цветов

https://www.youtube.com/watch?v=X6CsbhSVUEc&t=309s  How to make a responsive navbar with tailwind css | tailwind css tutorial

https://www.youtube.com/watch?v=LlTxTHfk2tk   
Creating a README File That Makes Your Project Shine | readme file tutorial |


## Install Tailwind CSS with Ruby on Rails

Setting up Tailwind CSS in Ruby on Rails v7+ project.

https://tailwindcss.com/docs/guides/ruby-on-rails

Run your build process with ./bin/dev.
`./bin/dev`

## Scaffold

`rails new toy_app`

`bundle `




`rails g scaffold User name:string email:string`

`bundle exec rails db:migrame`

`bin/rails server -p 8000`

`rails g scaffold Micropost content:text user_id:integer`

`bundle exec rails db:migrate`

## Gem Devise

1. Добавляем в гемфайл gem "devise"
2. bundle
3. rails g devise:install. После запуска команды рейлс дает подсказки какие у нас должны быть настройки.

http://rubydev.ru/2011/10/rubydev_ruby_tutorial_metaprogramming_ruby

https://postmarkapp.com/  Этот сайт написан на руби и рэйлс. Подходит для transactionals emails(реагирует на какое-то событие на сайте). Почтовую рассылку через него делать нельзя. Сразу забанят.

https://github.com/ActiveCampaign/postmark-gem

bulk email messaging подходит для почтовой рассылки.
В каждом письме должна быть кнопка unsubscribe. Если этой кнопки нет - это нарушение terms of service.


https://www.refinerycms.com/ The most popular Ruby on Rails CMS