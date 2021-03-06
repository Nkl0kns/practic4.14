[< Перейти к главной странице](./readme.md)
# .gitignore

`.gitignore` - это файл, в котором находится файлы, для которых не должно вестись отслеживание версий.

---
 ## Синтаксис 

 1. Каждая строка - отдельный шаблон
2. Пустые строки игнорируются
3. Строки начинающиеся с # являются комментариями
4. Символ слеша "/" в начале строки указывает на текущую папку (где лежит .gitignore)
5. Звёздочка(*) заменяет любое количество символов
6. Две звёздочки(**) используются для указания всех подпапок.
7. Восклицательный знак(!) в начале строки инвертирует шаблон (используется для исключений)
8. Для экранирования спецсимволов используется обратный слэш "\". Для игнорирования всей директории, правило должно оканчиваться на слэш(/), в противном случае правило считается именем файла.
---
### Пример файла .gitignore
```
#Игнорировать файл foo.txt.
foo.txt
#Игнорировать html файлы
*.html
#Но конкретно foo.html не игнорировать
!foo.html
#Игнорировать rar файлы в корне проекта
#Допустим файл /temp/main.rar не будет проигнорирован т.к. он не в корне
/*.rar
#Игнорировать css файлы из папки bar не включая подпапки
#Допустим файл /bar/temp/main.css не будет проигнорирован т.к. он в подпапке temp
/bar/*.css
#Игнорировать js файлы из папки bar и подпапок, если таковые будут
/bar/**.*.js
```