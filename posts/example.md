---
{
  "post": {
    "name": "Example",
    "author": "Ivanzar",
    "description": "",
    "pattern": "main.liquid"
  }
}
---
## Шаг 1. Создание проекта
Создайте проект в каталоге FilliEx.
#### Linux:
```$ fillipost-cli create your_path/FilliEx```
#### Windows:
```$ fillipost-cli.bat create your_path/FilliEx```
## Шаг 2. Создание шаблона
Перейдите в папку **your_path/FilliEx/patterns/**. Создайте файл **main.liquid**.

Скопируйте и вставьте следующий код:
<pre class="html4strict" style="font-family:monospace;"><span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">meta</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;viewport&quot;</span> <span style="color: #000066;">content</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;width=device-width, initial-scale=1&quot;</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">meta</span> <span style="color: #000066;">charset</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;UTF-8&quot;</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">title</span>&gt;</span>{{ post.name }}<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">title</span>&gt;</span>
&nbsp;
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">link</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;https://fonts.googleapis.com/css?family=Roboto:900,400&quot;</span> <span style="color: #000066;">rel</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">link</span> <span style="color: #000066;">rel</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;text/css&quot;</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;./resources/style/main.css&quot;</span>&gt;</span>
&nbsp;
{% include 'head.liquid' %}
&nbsp;
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">div</span> <span style="color: #000066;">id</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;page-content&quot;</span>&gt;</span>{{ post.content }}<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">div</span>&gt;</span></pre>

## Шаг 3. Создание сниппета
Перейдите в папку **your_path/FilliEx/snippets/**. Создайте файл **head.liquid**.

Скопируйте и вставьте следующий код:
<pre class="html4strict" style="font-family:monospace;"><span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">link</span> <span style="color: #000066;">rel</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;text/css&quot;</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;./resources/style/head.css&quot;</span>&gt;</span></pre>
<pre class="html4strict" style="font-family:monospace;"><span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">div</span> <span style="color: #000066;">id</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;page-head&quot;</span>&gt;</span>
	<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">div</span> <span style="color: #000066;">id</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;page-head--title&quot;</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">h3</span>&gt;</span>Example<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">h3</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">div</span>&gt;</span></pre>

## Шаг 4. Создание файлов CSS
Перейдите в папку **your_path/FilliEx/resources/style/**. Создайте файлы **head.css** и **main.css**.
Скопируйте и вставьте в **main.css** следующий код:
<div class="css" style="font-family:monospace;color: #006;">body <span style="color: #00AA00;">&#123;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">margin</span><span style="color: #00AA00;">:</span> <span style="color: #cc66cc;">0</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">font-family</span><span style="color: #00AA00;">:</span> <span style="color: #ff0000;">'Roboto Regular'</span><span style="color: #00AA00;">,</span> <span style="color: #993333;">sans-serif</span><span style="color: #00AA00;">;</span><br />
<span style="color: #00AA00;">&#125;</span><br />
<br />
<span style="color: #cc00cc;">#page-</span><span style="color: #000000; font-weight: bold;">content</span> <span style="color: #00AA00;">&#123;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">margin-left</span><span style="color: #00AA00;">:</span> <span style="color: #933;">50px</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">margin-right</span><span style="color: #00AA00;">:</span> <span style="color: #933;">50px</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">margin-top</span><span style="color: #00AA00;">:</span> <span style="color: #933;">120px</span><span style="color: #00AA00;">;</span><br />
<span style="color: #00AA00;">&#125;</span></div>

Скопируйте и вставьте в **head.css** следующий код:
<div class="css" style="font-family:monospace;color: #006;"><span style="color: #cc00cc;">#page-head</span> <span style="color: #00AA00;">&#123;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">overflow</span><span style="color: #00AA00;">:</span> <span style="color: #993333;">hidden</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">position</span><span style="color: #00AA00;">:</span> <span style="color: #993333;">fixed</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">width</span><span style="color: #00AA00;">:</span> <span style="color: #933;">100%</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">top</span><span style="color: #00AA00;">:</span> <span style="color: #cc66cc;">0</span><span style="color: #00AA00;">;</span><br />
<span style="color: #00AA00;">&#125;</span><br />
<br />
<span style="color: #cc00cc;">#page-head--title</span> <span style="color: #00AA00;">&#123;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">background-color</span><span style="color: #00AA00;">:</span> <span style="color: #cc00cc;">#3F51B5</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">height</span><span style="color: #00AA00;">:</span> <span style="color: #933;">50px</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">color</span><span style="color: #00AA00;">:</span> <span style="color: #993333;">white</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">line-height</span><span style="color: #00AA00;">:</span> <span style="color: #933;">50px</span><span style="color: #00AA00;">;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">text-indent</span><span style="color: #00AA00;">:</span> <span style="color: #933;">10px</span><span style="color: #00AA00;">;</span><br />
<span style="color: #00AA00;">&#125;</span><br />
<br />
<span style="color: #cc00cc;">#page-head--title</span> h3 <span style="color: #00AA00;">&#123;</span><br />
&nbsp; &nbsp; <span style="color: #000000; font-weight: bold;">margin-top</span><span style="color: #00AA00;">:</span> <span style="color: #933;">0px</span><span style="color: #00AA00;">;</span><br />
<span style="color: #00AA00;">&#125;</span></div>

## Шаг 4. Создание поста
Перейдите в папку **your_path/FilliEx/posts/**. Создайте файл **example.md**.
Скопируйте и вставьте следующий код:
**<p style="color: green">---</p>**

```
{
  "post": {
    "name": "Example",
    "pattern": "main.liquid"
  }
}
```

**<p style="color: green">--- <p>**

**<p style="color: #424242"># Hello FilliPost !<p>**

## Шаг 5. Сборка и запуск
Собирите проект командой build
#### Linux:
```$ fillipost-cli build your_path/FilliEx```
#### Windows:
```$ fillipost-cli.bat build your_path/FilliEx```
Перейдите в папку **your_path/FilliEx/build/**. Откройте в браузере файл **example.html**

![example](./resources/img/example.png)

