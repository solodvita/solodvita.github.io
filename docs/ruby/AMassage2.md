# AMassage2

Создаем приложение AMassage2
`rails new AMassage2 --database=postgresql`

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

## Создание блога
`rails new TestImage && cd TestImage && code .`

`rails g scaffold post title body:text`

`rails active_storage:install`

`rails db:migrate`

`rails s`

`rails db:migrate`

`rails s`

To create your database, run:

        bin/rails db:create

## Создаем статические страницы 

Создаем контроллер StaticPages с действиями home help
`rails g controller StaticPages home help`

Удаляем ветку локально 
`git branch -d <branch-name>

Удалите ветку на удалённом репозитории (если ветка была уже отправлена на удалённый репозиторий):
`git push origin --delete <branch-name>`
