Нужно зараннее создать токен на https://github.com/settings/tokens и записать его себе куда-нибудь
Гит по идее должен запрашивать его каждый push/pull/clone (если приватный)
По стандарту он его не запоминает, мб для сессии в терминале 

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

Создаем новый репозиторий https://github.com/new

git config --global user.name "Юзернейм в гитхабе"
git config --global user.email "Почта"

Создаем папку с любым названием

cd "имя созданной папки"
git init

Тут создаете .txt файл и пишете в него что-нибудь

git status

git add .

git commit -m "Initial commit"

git remote add origin "ссылка на созданный репозиторий"

git push -u origin master


cd ..
git clone "ссылка на созданный репозиторий"

Должна появиться папка с именем вашего репозитория

cd "имя новой папки"

git pull origin master

git checkout -b new-branch

Изменяем наш текстовый файлик
Да, об этом ничего не сказано, так что по желанию
Но так хоть у слияния будет смысл

git add .
git commit -m "Придумайте какое-нибудь название"

git checkout master
git merge new-branch

git branch -d new-branch

git push origin master
