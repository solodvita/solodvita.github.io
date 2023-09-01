# Linux

## Некоторые команды

### Удаление


rm -rf имя_папки
- рекурсивно удалит папки и вложенные файлы, -f (force) для того, чтобы команда не запрашивала подтверждение удаления



failed to run command ‘/bin/bash’: No such file or directory

Сообщение об ошибке "failed to run command ‘/bin/bash’: No such file or directory" обычно означает, что система не может найти исполняемый файл оболочки Bash по указанному пути /bin/bash. Это может произойти по нескольким причинам:

which bash
 - указывает местоположение bash

/usr/bin/bash исполняемый файл тут. Что делать?

Если исполняемый файл Bash на вашей системе находится в /usr/bin/bash, а не в /bin/bash, то вам следует использовать правильный путь к исполняемому файлу Bash при выполнении команд. Просто замените /bin/bash на /usr/bin/bash в ваших командах. 

Если вы хотите запустить интерактивную оболочку Bash (терминал), используйте следующую команду:
/usr/bin/bash

Если у вас есть скрипт, который начинается с #!/bin/bash в шапке, убедитесь, что он также указывает на правильный путь:

bash

#!/usr/bin/bash

Если вы пытаетесь запустить скрипт, который вызывает Bash, например:

bash

myscript.sh

Убедитесь, что скрипт содержит правильную шапку, как указано выше.

## gparted

 `sudo apt install gparted`

## Ventoy

Видеоинструкция <a href="https://www.youtube.com/watch?v=iVKO9Hnzvwo&t=230s">Ventoy - Мультизагрузочная флешка на Linux</a>

`sudo sh Ventoy2Disk.sh -I /dev/sdd`

## Pass 
<a href="https://git.zx2c4.com/password-store/about/">Man page</a>
