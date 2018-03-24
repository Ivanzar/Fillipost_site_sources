---
{
  "post": {
    "name": "Documentation",
    "author": "Ivanzar",
    "description": "",
    "pattern": "main.liquid"
  }
}
---
# Документация
## Создание проекта
#### Linux:
```$ fillipost-cli create <project path>```
#### Windows:
```$ fillipost-cli.bat create <project path>```
## Сборка проекта
#### Linux:
```$ fillipost-cli build <project path>```
#### Windows:
```$ fillipost-cli.bat build <project path>```

---

## Команды

|                                    |                                                 |             |                                          |
|------------------------------------|-------------------------------------------------|-------------|------------------------------------------|
| **build `<project path>` `[flag]`**  | &emsp;Сборка проекта - генерация статических страниц. | &emsp;Флаги:      |                                          |
|                                    |                                                 | &emsp;&emsp;--resources  | Сборка только ресурсов (папка resources) |
|                                    |                                                 | &emsp;&emsp;--post [post file]  | Сборка отдельного поста (папка posts)    |
|                                    |                                                 | &emsp;&emsp;--posts-only | Сборка только постов (папка posts)
| **create `<project path>`**        | &emsp;Создание нового проекта.                        |              |                                          |
| **clean `<project path>`**         | &emsp;Удаляет деррикторию ``` project path/build ```. |              |                                          |

## Строение дериктории проекта
* _**project path**_&emsp;&nbsp;нзавние дерриктории проекта
  * _**build**_&emsp;&emsp;&emsp;дериктороия со сгенерированными старницами и ресурсами
  * _**patterns**_&emsp;&nbsp;&nbsp;дериктория с шаблоанми
  * _**posts**_&emsp;&emsp;&emsp;дериктория со старницми в Markdown формате(назвние файлов должно оканчиваться на .md)
  * _**resources**_&emsp;дерриктория с ресурасами проекта
  * _**snippets**_&emsp;&nbsp;&nbsp;шаблоны для вставки в код файлов дериктории patterns
## Шаблон старниц в дериктории post
**<p style="color: green">---</p>**

```
{
  "post": {
    "name": string,
    "author": string,
    "description": string,
    "pattern": string,
    "date": int
  },
  "variable1": ,
  "variable2": ,
  "variable3": ,
  "variableN": 
}
```

**<p style="color: green">--- <p>**

**<p style="color: #424242">Текст в Markdown формате<p>**


#### Описание:

**`---`** - начало заголовка


**`"post"`** - обязательное поле


**`"name"`** - название старницы, обязательно


**`"author"`** - имя автора, не обязательно


**`"description"`** - описание поста, не обязательно


**`"pattern"`** - шаблона для страницы(в папке `patterns`), обязательно


**`"date"`** - дата unix epo time, не обязательно


**`"variable"`** - другие поля, не обязательно

**`---`** - конец заголовка
