При установке Ruby RVM может потребоваться использовать sudo для установки зависимостей. Убедитесь, что пользователь, вызывающий команды RVM, имеет права sudo.

Если вы хотите, чтобы пользователь, у которого нет прав sudo, мог запускать команды RVM, вам необходимо отключить автоматическую установку зависимостей:


# Установка Ruby с помощью rvm

```rvm autolibs disable
```


```rvm install 2.1.1
```


# Rails

http://rusrails.ru/getting-started

---

https://dou.ua/lenta/articles/telegram-bot-ruby/

---


https://world.hey.com/dhh


https://www.8host.com/blog/ustanovka-ruby-on-rails-s-pomoshhyu-rbenv/

https://blog.rnds.pro/026-three-great-answers   Rails 7: три мощных ответа JavaScript’у в 2021+

https://rubyonrails.org/doctrine   Доктрина рейлс


https://github.com/abhaynikam/boring_generators    Boring generator Шлак или нет? Не разобрался



https://www.softcover.io/read/db8803f7/ruby_on_rails_tutorial_3rd_edition_russian/frontmatter 

  Ruby on Rails Tutorial
Learn Web Development with Rails
Michael Hartl

https://getbootstrap.com/docs/3.4/customize/ Scss переменные.


## Create new app

`rails new blog -j esbuild --css bootstrap -a propshaft`
`rails new blog --css bootstrap `

`rails g controller home index`

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

`rails db:system:change --to=postgesql`

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


https://www.refinerycms.com/ The most popular 

Ruby on Rails CMS


https://www.youtube.com/watch?v=kIPlfjDM1kY

## Avo

https://www.youtube.com/watch?v=yIpNJ5zwgCU&t=72s   Avo Admin Panel Gem | Ruby on Rails 7 Tutorial

https://www.youtube.com/watch?v=nqAnftA8LbA  Image Previews with Active Storage in Ruby on Rails 7

## Создание блога
`rails new TestImage && cd TestImage && code .`

`rails g scaffold post title body:text`

`rails active_storage:install`

`rails db:migrate`

`rails s`

```
app\models\post.rb

class Post < ApplicationRecord
    has_one_attached :image
end
```
```
controllers\post_controller.rb
 def post_params
      params.require(:post).permit(:title, :body, :image)
 end
```
```
views\posts\_form_html.erb
 <div>
    <%= form.label :image, style: "display: block" %>
    <%= form.file_field :image %>
  </div>
```

```
views\posts\_post.html.erb

<%= image_tag(post.image, class: "image") %>
```

```
\assets\stylesheets\application.css
.image {
    width: 300px;
     height: auto
}

.image-container {
    width: 300px;
     height: 300px
}
```
## Heroku

`rails db:system:change --to=postgresql`

`bundle`

`heroku create`

`git push heroku main`

`heroku run rake db:migrate`

```config\routs.rb
root "posts#index"
```
on local mashine 
`bin/rails db:create`
`rails db:migrate`

## Avo 
add gem 'avo'
gem 'devise' to Gemfile 

# Use Active Storage variants [https://guides.rubyonrails.org/active_storage_overview.html#transforming-images]
gem "image_processing", "~> 1.2"

`bundle`
`rails g avo:install`
`rails g scaffold post title body:text`
`rails g model comment body:text post:references`
```models\post.rb
class Post < ApplicationRecord
    has_many :comments
    has_one_attached :image
end
```
`rails active_storage:install`
`rails db:migrate`
`rails g devise:install`
`rails g devise user`
`rails g migration AddRoleToUser role:string`
`rails db:migrate`
`rails c`

https://www.youtube.com/watch?v=SxwFyK9OtfY   Layouts For Admin Users with Devise in Ruby on Rails 7


https://www.youtube.com/watch?v=tww-0bO4zCY   Flatpickr Date Picker in Ruby on Rails 7

https://www.youtube.com/watch?v=xhWGY_JCUOs   Generate QR Codes with Active Storage | Ruby on Rails 7 Tutorial

https://www.youtube.com/watch?v=oMEWpPvmyS0

Intro Ruby on Rails 7 For Beginners Tutorial Series
• 1 / 29
UA
5:12 / 11:43
Bing's ChatGPT with Ruby on Rails is Here! 

https://www.youtube.com/watch?v=Ith6FA0kxPc

Image Cropping With Active Storage & CropperJS | Ruby On Rails 7 Tutorial

https://www.youtube.com/watch?v=hck_SWp1cVA
UA
0:12 / 10:56
Mapkick Gem Spotlight | Ruby On Rails 7 Tutorial 

https://chartkick.com/mapkick


https://www.youtube.com/watch?v=Rw-MIHm62yE

Secure Your Secret Keys With Rails 7 Encrypted Credentials

https://www.youtube.com/watch?v=CnZnwV38cjo
Devise Google Login With Omniauth | Ruby On Rails 7 Tutorial

https://www.youtube.com/watch?v=Wt3EMm0_5Yo
Copyright Footers with Auto Dates (Because Clients) | Ruby on Rails 7 Tutorial

https://www.youtube.com/watch?v=B6BqxQBS06I

Turbo Crash Course For Twitter Likes With Devise User Sessions | Ruby on Rails 7 Tutorial

https://www.youtube.com/watch?v=d2-cd4RKFwA&t=24s

UA
0:38 / 29:01
Deploy A Rails 7 App To Heroku (Realtime Chatroom) | Turbochat Part 8 

https://www.youtube.com/watch?v=cWkISBYM_0g

Quickly Setup Bootstrap 4 in Rails 6 With Yarn And Webpack | Ruby On Rails 6 Beginner Tutorial

https://www.youtube.com/watch?v=7v2EMmfBJL8

User And Admin Accounts With Devise | Authentication Ruby On Rails 5.2 Tutorial

https://www.youtube.com/watch?v=0XRoQOGtSxE   PGHero Gem for Ruby on Rails 7

https://www.youtube.com/watch?v=UmAx1A6ic2M&t=608s  Deploy Rails 7.1 To AWS With Docker And Nginx!

https://www.youtube.com/watch?v=ZKdIPUfXQgc   Creating User Profile Pages For Blog Authors | Intro To Ruby On Rails For Beginners Part 14