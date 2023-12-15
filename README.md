# работа с git

## перед началом работы
в тексте команды отображены следующим образом:

`git`

```shell
git init
git checkout -b BRANCH-NAME
```

если текст большими буквами через дефис в треугольных скобках - YOUR-EXAMPLE, то это условные значения, которые устанавливаются на ваш выбор
- YOUR-GITHUB-NAME - имя пользователя на GitHub
- YOUR-GITHUB-REPOSITORY-NAME - имя репозитория на GitHub
- YOUR-GITHUB-EMAIL, электронная почта на GitHub и т. д. и т. п.

---

*предварительные требования*:
- вам нужно [установить](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git) **git** на ваш ПК, если не установлен
- вам нужно [установить](https://apps.microsoft.com/detail/9N0DX20HK701?hl=ru-ru) **Windows Терминал** на ваш ПК, если не установлен

## у вас нет репозитория и вам нужно создать новый
1. создайте **удаленный** **GitHub* репозиторий на сайте [github.com](https://github.com/), если доступ к репозиторию не был вам выдан
2. создайте папку на вашем ПК в удобном месте (например, C:\Users\YOUR-USER\MY-PROJECTS-FOLDER)
3. создайте **локальный** ***git*** репозиторий в папке которую вы ранее создали (шаг 2). для этого кликните ПКМ (правую кнопку мыши) выберите выберите Открыть с помощью -> Windows Terminal, открыв Терминал введите команду `git init` и нажмите Enter
4. добавьте конфигурацию вашей учетной записи в **локальном** репозиторий, используя следующие команды:
```pwsh
git config user.name "YOUR-GITHUB-NAME"
git config user.email "YOUR-GIHUB-EMAIL@EXAMPLE.COM"
```
5. добавьте ссылку на удаленный репозиторий на GitHub с помощью команды `git remote add origin https://github.com/YOUR-GITHUB-NAME/YOUR-GITHUB-REPOSITORY-NAME.git`, где *git remote add origin https://github.com/YOUR-GITHUB-NAME/YOUR-GITHUB-REPOSITORY-NAME.git* - ссылка на ваш репозиторий
6. добавьте файлы для отслеживания изменений в *staging area* с помощью команды `git add .` или `git add --all` или `git add -A`
7. создайте и смените ветку одной командой `git checkout -b BRANCH-NAME`
8. создайте коммит с помощью команды `git commit -m "ANY-MESSAGE-YOU-WANT-TO-LIVE"`
9. отправьте изменения в удаленный репозиторий с помощью команды `git push -u origin BRANCH-NAME`

## как внести изменения в репозиторий
Для того, чтобы добавить новые файлы или зафиксировать изменения в существующих, вам следует:
1. добавьте файлы для отслеживания в *staging area* с помощью команды `git add .`
2. выполнить комманду `git commit -m "ANY-MESSAGE-YOU-WANT-TO-LIVE"`
3. отправьте изменения в удаленный репозиторий с помощью команды `git push -u origin dev`

Для того, чтобы изменить ветку на новую, вам следует:
1. вы можете сменить ветку с помощью команды `git switch BRANCH-NAME'
2. либо вы можете создать и сменить ветку одной командой `git checkout -b BRANCH-NAME`

