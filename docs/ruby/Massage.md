# AMassage2

### Создаем приложение AMassage2
`rails new AMassage2 --css sass --database=postgresql`

`git checkout -b features` создаем ветку функции и сразу переключаемся на нее.

`git checkout main` переключаемся на ветку main
`git merge features` сливаем ветку features с веткой main
`git branch -d features` удаляем ветку футер
`git branch -d features` удаляем ветку даже если изменения не слиты

Деплоим
## Heroku

`rails db:system:change --to=postgresql`

`bundle`

`heroku login`

`heroku create`

`git push heroku main`

`heroku run rake db:migrate`

## Создаем статические страницы 

 `git checkout main` переключаемся на ветку майн 
 `git checkout -b static-pages` создаем новую ветку и переключаемся на нее

Создаем контроллер StaticPages с действиями home contacts
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

