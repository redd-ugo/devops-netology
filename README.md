# devops-netology  

## Тестовая запись  
Простая строчка  


## Terraform  

В целях улучшения будущей работы с **Terraform** используем *.gitignore* в соответствующем каталоге.
Правила, добавленные в *.gitignore*:  
*  Локальные папки внутри директории
*  Файлы *.tfstate*
*  Файлы аварийных логов  _crash.log_ и _crash.\*.log_
*  Файлы _\*.tfvars_ в которых могут содержаться конфиденциальные данные (пароли, закрытые ключи и т.п.)
*  Переопределенные файлы типа *override*
*  Файлы конфигурации интерфейса командной строки

## Использование PyCharm
Изменяем и комитим через PyCharm