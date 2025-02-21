 # Иструкция для работы с Git и удалеными репозиториями 

 ## Что такое Git?
 Git - это одна из реализация распределенных систе контроля версий, имеющая как  локальные, так и удаленные репозитории. Является самой популяроной реализацией систем контроля версий в мире. 

  ![<GIT>](<images.png>)

### Линус Торвальдс
Финно-американский программист. Создатель операционной системы Linux, создатель git

![<Линус Торвальдс>](<Linus.webp>)

### GIT
>Это просто программа, которая берет
на себя вопросы контроля версий
над проектом
>>Сохраняет в памяти не файлы целиком,
а разницу между файлами

### GIT позволяет:
* Сохранять разные версии
* Перемещаться между ними

Скачать Git можно на [официальном сайте](https://git-scm.com/ "Скачать Git") 

 # Подсказка по GIT 

### Созадние репозитория
```sh 
git init 
```
### Создание коммитов
```sh
git commit -m "Message"
```
### Довабить файл или файлы к следующему коммиту
```sh
git add
```
### Вывод на экран истории всех коммитов с их хеш-кодами
```sh
git log
```
### Отобразить каждый коммит в одну сроку
```sh
git log --oneline
```
### Переход от одного коммита к другому
```sh
git checkout
```
### Вернуться к актуальному состоянию и продолжить работу
```sh
git checkout master
```
### Получить информацию от git о его текущем состоянии
```sh
git status
```
### Отобразить все ветки
```sh
git branch
```
### Добавить новую ветку
```sh
git branch <название новой ветки>
```
### Переход на другую ветку
```sh
git checkout <название новой ветки>
```
### Слить любую ветку с текущей
```sh
git merge <имя ветки для слияния с текущей>
```
## Конфликт изменений
Установка и настройка системы контроля версий.
При работе в двух ветках одновременно может
возникнуть ситуация, когда в одной и другой
ветке мы по-разному изменили блок текста.
Если затем мы попробуем слить эти ветки, Git
сообщит о конфликте и предложит выбрать,
какие же изменения записать. 
Поэтому у проекта в репозитории должен быть один
ответственный пользователь, наделённый правом проводить
слияния и разрешать конфликты.
### Удаление веток
```sh
git branch -d <название ветки для удаления>
```
## Инструкция по работе с удаленными репозиториями
### Как настроить совместную работу:
1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. “Подружить” ваш локальный и удалённый репозитории. GitHub при создании нового репозитория подскажет, как это можно сделать
4. Отправить (push) ваш локальный репозиторий в удалённый (на GitHub), при этом, возможно, 
вам нужно будет авторизоваться на удалённом репозитории
5. Провести изменения “с другого компьютера”
6. Выкачать (pull) актуальное состояние из удалённого репозитория
### Как сделать pull request:
* Делаем   (ответвление) репозитория fork
* Делаем git clone   версии репозитория СВОЕЙ
* Создаем новую ветку и в НЕЕ вносим свои изменения
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой GitHub
* На сайте GitHub нажимаем кнопку pull request