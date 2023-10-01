# AMassage2

### Создаем приложение AMassage2
`rails new AMassage2 -j esbuild --css bootstrap --database=postgresql`

### Footer
`git checkout -b footer` создаем ветку футер и сразу переключаемся на нее.
`rails g stimulus copyright`
`git checkout main` переключаемся на ветку main
`git merge footer` сливаем ветку футер с веткой main
`git branch -d footer` удаляем ветку футер

Деплоим
## Heroku

`rails db:system:change --to=postgresql`

`bundle`

`heroku create`

`git push heroku main`

`heroku run rake db:migrate`

## Создание блога
`rails new TestImage && cd TestImage && code .`

`rails g scaffold post title body:text`

`rails active_storage:install`
 `bin/rails db:create`

`rails db:migrate`

`rails s`

`rails db:migrate`

`rails s`

To create your database, run:

        bin/rails db:create

## Создаем статические страницы 

 `git checkout main` переключаемся на ветку майн 
 `git checkout -b static-pages` создаем новую ветку и переключаемся на нее

Создаем контроллер StaticPages с действиями home help
`rails g controller StaticPages home contacts`
`rails g controller Pages home about contacts`



`git checkout main`
Switched to branch 'main'

`git merge static-pages` слияние веток


Удаляем ветку локально 
`git branch -d static-pages`

Удалите ветку на удалённом репозитории (если ветка была уже отправлена на удалённый репозиторий):
`git push origin --delete <branch-name>`

Вставка изображения
<%= image_tag("1.jpeg", alt: "Описание изображения") %>

///