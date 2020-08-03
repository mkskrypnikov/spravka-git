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
Создание веток после клонирования (кроме master)
git branch <local-branch><origin/remote-branch>
или
git checkout --track <remote-branch>

```

#######Синхронизация с удаленным репозиторием
```
git push (отправка данных)
git fetch <origin> (получает данные но не merge)
git checkout origin/feature/sale (для дальнейшего просмотра)
git merge (для слияния)
git pull (git fetch + merge)

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
    * подпункт 

[ссылка](https://github.com/mkskrypnikov/spravka-git)
![картинка](https://staging.fofxacademy.com/wp-content/uploads/2020/01/install-git-for-multiple-users.png)

'''python
import pandas as pd
'''
```

#######Просмотр веток
```
git branch
```

#######Создание веток
```
git branch novaya/metka
```
#######Переключение между ветками
```
git checkout novaya/vetka

```
#######Объединение
```
git merge --no-ff novaya/metka
```
#######Визуализация меток
```
git log navaya/metka --graph --oneline
```
#######Удаление веток
```
git branch -d novaya/vetka
git push --delete origin novaya/vetka
```
#######Теги
```
git tag –a v1.0 –m "Версия 1.0"
git tag –a v1.0 –m "Версия 1.0" <commit-id>
```
#######Просмотр тегов
```
git tag
```
#######Принудительная отправка тегов
```
git push --tags
```
#######Удаление тегов
```
git tag -d v1.0
git push --delete origin v1.0
```
#######Работа с историей
```
git log
git log -- index.html
git show ffbf1e -- index.html
git log -p -- index.html
git log --grep 'Перво' (поиск по содержанию комментария коммита
git log -S'page' -p (поиск по содержанию файлов)
git log --all (поиск по всем веткам)
git blame -- <path> (поиск с авторством)
```
#######Откат изменений
```
git checkout <commit-id>
рекомендуется после создать новую ветку для коммита
git branch <name>
git checkout <name>
```

#######fast-forward
```
--no-ff
по умолчанию переключает указатель на метку
при выключеном делает новый коммит
```

#######отмена коммитов
```
git reset <mode> <commit-id>

— hard – передвигаем указатель на определённый коммит, не сохраняя
никаких изменений;
— soft – передвигаем указатель на определённый коммит, при этом
предыдущие изменения сохраняются в рабочем каталоге и index'е;
— mixed – передвигаем указатель на определённый коммит, при этом
предыдущие изменения сохраняются в рабочем каталоге, но не в index'е.

git reset <mode> HEAD~1<num>
```
#######Issue
```
Для закрытия Issue в коммит добавить коммент:
fixes #2 Добавили форму для отображения 
fixes #2 говорит о том, что закрывает issue с id = 2.

```

#######GITHUB FLOW
[GITHUB FLOW](https://guides.github.com/introduction/flow/)
```
1. Создаёте branch ;
2. В рамках branch 'а коммитите изменения;
3. Открываете Pull Request для обсуждения ваших изменений с коллегами
(code review, решение вопросов);
4. Делаете merge
```
#######PULL REQUESTS
```
— base –то, куда мы собираемся делать Pull Request;
— head –то, что мы собираемся использовать в качестве Pull Request'а
```
