#Git

######Авторизационные данные

```
git config --global user.name "Maksim Skrypnikov"
git config --global user.email mkskrypnikov@gmail.com
```

######Установка редактора
```
git config --global core.editor nano
```


######Создание репозитория

```
git init
```
######Добавление файлов и маски
```
git add index.html
git add *
git add *.js
git add .
```

######Текущий стстаус
```
git status
```

######Коммит
```
git commit -m "first commit"
git commit -a -m "first commit"
```

######История и подробная информация
```
git log
git show 1234567
```

######Удаление лишнего из add
```
git rm --cached name.txt
```

######Возврат по последнего коммита или до определенного
```
git commit --amend -m "Roboto Font"
git revert <commit-id>
```

#######Игнорирование файлов и каталогов
```
.gitignore

name.txt
tmp/
/tmp/
*.txt
```

#######Клонирование репозитория
```
git clone https://github.com/mkskrypnikov/spravka-git.git
```

######Работа с репозиторием
```
git remote -v
git remote add origin https://github.com/mkskrypnikov/spravka-git.git
```

######Отправка в удаленный репозиторий
```
git push -u origin master
git push
git push -all
```

#######Marcdown
```
создается файл README.md
```

```markdown
#Заголовки

**жирный**
*курсив*
~~зачеркнутый~~

1. нумерованный список
    1. подпункт

* список
    * подпункта 

[ссылка](url)
![картинка](url)

'''python
import pandas as pd
'''
```