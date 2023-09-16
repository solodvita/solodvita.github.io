
https://git-scm.com/book/ru/v2



## Как коммитить в несколько репозиториев на github?


https://techrocks.ru/2020/12/24/how-to-manage-several-github-accounts/

https://medium.com/@mityamitko/%D0%B4%D0%B2%D0%B0-%D0%B8-%D0%B1%D0%BE%D0%BB%D1%8C%D1%88%D0%B5-github-gitlab-%D0%B0%D0%BA%D0%BA%D0%B0%D1%83%D0%BD%D1%82%D0%B0-%D0%BD%D0%B0-%D0%BE%D0%B4%D0%BD%D0%BE%D0%BC-%D0%BA%D0%BE%D0%BC%D0%BF%D0%B5-b757efe4c3bb


## Как создать новую ветку и перейти на нее?
<a href="https://git-scm.com/book/ru/v2">Pro Git Book</a>

`git branch`  - это своего рода "менеджер веток", она умеет перечислять векти, создавать новые, удалять и переименовывать их.

`git branch main` - создается новый указатель на текущий коммит. git branch только создает новую ветку, но не переключает на нее.

`git log --oneline --decorate` - выводит на какую ветку показывает указатель HEAD


`git checkout main` - переключение на ветку main. Указател HEAD переместится на ветку main.

`git log` по умолчанию отобразит только историю коммитов для текущей ветки.

`git log --all` покажет исорию коммитов по всем веткам.

`git log master` - отобразит историю коммитов на ветке мастер

`git log --oneline --decorate --graph --all` - отбразит историю коммитов

`git checkout -b <newbranchname>` - создать новую ветку и переключиться на нее.

`git merge master` - слияние веток main и master

`git branch -d master` - удалить ветку master



