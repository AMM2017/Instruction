# Перенос своего репозитория в эту организацию

Убеждаемся, что локальный репозиторий содержит все коммиты и ветки с помощью
```Bash
git status # Показывает текущую ветку и изменённые\подготовленные(staged) файлы
git branch # Выводит список всех веток
git log --pretty=format:"%h - %an, %ar : %s" # Показывает комиты текущей ветки
```
Удаляем существующий remote
```Bash
git remote remove origin
```
Создаём пустой(!) репозиторий в организации и копируем ssh url
Создаём новый remote
```Bash
git remote add origin %url%
```
Пушим нужные ветки (master, dev, ...) не забывая привязывать up-stream ветки
```Bash
git checkout master
git push -u origin master

git checkout dev
git push -u origin dev

...
```
