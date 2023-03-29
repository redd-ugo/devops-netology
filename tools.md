# Домашнее задание "Инструменты Git"  

## Ответы на задание 02-git-04-tools  

1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.

Используем команду `git show aefea`  
На выходе получаем:
* полный хеш `aefead2207ef7e2aa5dc81a34aedf0cad4c32545_
* комментарий **Update CHANGELOG.md**

2. Ответы на вопросы:
* Коммиту `85024d3` соответствует тег `v0.12.23`  Получили используя `git tag --points-at 85024d3`
* У коммита `b8d720` два родителя, их хеши:  
`56cd7859e05c36c06b56d013b55a252d0bb7e158`  
`9ea88f22fc6269854151c571162c5bcf958bee2b`  
Получили используя команду `git show b8d720` и `git show b8d720^2`  
* Список коммитов:  
`225466bc3e5f35baa5d07197bbc079345b77525e` Cleanup after v0.12.23 release  
`dd01a35078f040ca984cdd349f18d0b67e486c35` Update CHANGELOG.md  
`4b6d06cc5dcb78af637bbb19c198faff37a066ed` Update CHANGELOG.md  
`d5f9411f5108260320064349b757f55c09bc4b80` command: Fix bug when using terraform login on Windows  
`06275647e2b53d97d4f0a19a0fec11f6d69820b5` Update CHANGELOG.md  
`5c619ca1baf2e21a155fcdb4c264cc9e24a2a353` website: Remove links to the getting started guide's old location  
`6ae64e247b332925b872447e9ce869657281c2bf` registry: Fix panic when server is unreachable  
`3f235065b9347a758efadc92295b540ee0a5e26e` Update CHANGELOG.md  
`b14b74c4939dcab573326f4e3ee2a62e23e12f89` [Website] vmc provider links  
`33ff1c03bb960b332be3af2e333462dde88b279e` v0.12.24  
Получили командой `git log v0.12.23..v0.12.24 --pretty=oneline --reverse`

* Функция `func providerSource` добавлена в коммите `8c928e83589d90a031f811fae52a81be7153e82f`  
Поиск получен двумя командами. `git grep -p providerSource *.go` для определения файла `provider_source.go`, где была использована функция.  
Потом использовали  `git log -L :providerSource:provider_source.go`, для просмотра коммитов изменяющих эту функцию в файле

* Список коммитов в которых была изменена функция `globalPluginDirs`:  
commit 78b12205587fe839f10d946ea3fdc06719decb05  
commit 52dbf94834cb970b510f2fba853a5b49ad9b1a46  
commit 41ab0aef7a0fe030e84018973a64135b11abcd70  
commit 66ebff90cdfaa6938f26f908c7ebad8d547fea17  
commit 8364383c359a6b738a436d1b7745ccdce178df47  

Использовали команду `git log -L :globalPluginDirs:plugins.go | grep 'commit \w'`

* Автор функции `synchronizedWriters`:  
**Martin Atkins <mart@degeneration.co.uk>**  
Поиск изменений функции `git log -S 'synchronizedWriters' --oneline`, смотрим коммит
`git show 5ac311e2a9`


