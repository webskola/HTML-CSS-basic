# Веб и  HTML

## Общая информация

0. [Сэр Тимоти Джон «Тим» Бернерс-Ли][1] — изобретатель Всемирной паутины и руководитель Консорциума всемирной паутины (*W3C*).
0. [Консорциум всемирной паутины][2] (W3C) — разрабатывает стандарты или «рекомендации» по технологиям разработки веб-страниц.
1. [HTML][3] — язык разметки документов во Всемирной паутине. Большинство веб-страниц содержат описание разметки на языке HTML. Язык HTML интерпретируется браузерами, результат отображается на экране монитора компьютера или мобильного устройства. Спецификацию разрабатывает W3C.

## HTML

### Синтаксис

HTML документ размечается специальными ключевыми словами — тегами.

#### Структура тегов

- Символ &lt;
- Название тега
- Символ &gt;

Пример:
```html
<название_тега>
```

#### Парные и непарные теги

Парные (открывающий и закрывающий):
```html
<название_тега>Содержимое тега</название_тега>
```
Непарные (одинарные):
```html
<название_тега>
```
или
```html
<название_тега />
```
обва варианта эквивалентны. Второй считается более строгий.

**С помощью тегов формируются элементы.**

Существует набор стандартных тегов. Полные списки:
- [htmlbook.ru](http://htmlbook.ru/html) (не содержит информацию об устаревших тегах)
- [w3schools.com](http://www.w3schools.com/tags/default.asp) (en)
- [html5doctor.com](http://html5doctor.com/element-index/) (en)

Но допускается использование нестандартных тегов.

#### Атрибуты

Атрибуты указывают дополнительное значение для тега (может влиять и не влиять на визуальное отображение элемента). Пишутся только в открывающем теге.

<ins>*Правильно*</ins>:
```html
<название_тега атрибут="значение">   </название_тега>

<название_тега атрибут="значение" />

<название_тега атрибут="значение">
```
<del>*Неправильно*</del>:
```html
<название_тега атрибут="значение">   </название_тега атрибут="значение">
```

##### Атрибуты-флаги

Атрибуты без значения

```html
<название_тега атрибут>   </название_тега>

<название_тега атрибут />

<название_тега атрибут>
```

### Комментарии

Нужны для того, чтобы комментировать фрагменты коды, когда необходимо пояснение

```html
<!-- Комментарий, не виден на сайте, но виден в коде -->
```

### Стандартные элементы

#### Блочные (__block__) элементы

##### Заголовки

```html
<h1>Заголовок первого уровня</h1>
<h2>Заголовок второго уровня</h2>
…
<h6>Заголовок шестого уровня</h6>
```
Всего существует 6 уровней заголовков. Только заголовки бывают разного уровня, остальные теги не нумеруются.

#### Абзац

```html
<p>Первый абзац</p>
<p>Второй абзац</p>
```

#### Горизонтальный разделитель

```html
<hr />
```

#### Перенос строки

```html
<br />
```

#### Простой блок

```html
<div>
	… … … … … …
	… … … … … …
	… … … … … …
</div>
```

### Строчные (__inline__) элементы

```html
<em>выделенный текст</em>
<strong>сильно выделенный текст</strong>
<span>сгруппированный текст</span>
<br />
```

О `<strong>` и `<em>` &mdash; читаем [HTML5 Doctor][11]

[Пример][10]

### Вложение элементов

#### Вложение однострочное

```html
<p>Donec sed odio dui. <strong>Nulla vitae</strong> elit libero, a pharetra augue. Donec id elit non mi porta gravida at eget metus. Vivamus sagittis lacus vel augue <em>laoreet</em> rutrum faucibus dolor auctor. Praesent commodo cursus magna, vel scelerisque nisl consectetur et.</p>
```

#### Вложение многострочное

```html
<section>
	<h1>Hello world!</h1>
	<div>
		<p>Donec sed odio dui. Nulla vitae elit libero, a pharetra augue. Donec id elit non mi porta gravida at eget metus. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Praesent commodo cursus magna, vel scelerisque nisl consectetur et.</p>
	</div>
</section>
```

### Пробельные символы

Любые использованые в коде переносы строк, табы, несколько пробелов подряд и другие пробельные символы в браузере отображаются как один пробел.

```html
Donec sed odio dui.       Nulla vitae elit libero,
a pharetra augue. 	Donec id elit non mi porta gravida at eget metus.
```

Результат: Donec sed odio dui. Nulla vitae elit libero, a pharetra augue. Donec id elit non mi porta gravida at eget metus.

### Специальные символы

Англ. __HTML entities__

#### Структура спецсимволов

- `&`
	- название или
	- `#` и номер (десятичный) или
	- `#x` и номер ([шестнадцатиричный][18])
- `;`

#### Пример

- `&cent;` — &cent;
- `&#162;` — &#162;
- `&#xA2;` — &#xA2;

Полезные ссылки:

- [w3schools: html_entities][12]
- [w3schools: html_symbols][15]
- [wikipedia][13]
- [htmlarrows.com][14]

### Базовая структура HTML-документа

```html
<!doctype html>
<html>
	<head>
		<title>First web page</title>
	</head>
	<body>
		<h1>Hello world!</h1>
		<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla vitae elit libero, a pharetra augue. Curabitur blandit tempus porttitor. Cras justo odio, dapibus ac facilisis in, egestas eget quam.</p>
	</body>
</html>
```

Пояснение:
- `<!doctype html>` — декларация HTML-документа, пишется в самом начале документа
- `<html>` — корневой элемент, объединяющий элементы `<head>` и `<body>`
- `<head>` — заголовочная часть HTML-документа, предназначена для технической информации адресованной браузеру и другим сервисам
- `<body>` — основная часть HTML-документа, предназначена для информации отображаемой на сайте
- `<title>` — заголовок документа, отображается в табе или закладках

### Кодировка

Кодировку HTML указывают внутри элемента `<head>` ([info][21]):
- `<meta charset="utf-8" />` &mdash; HTML5
- `<meta http-equiv="content-type" content="text/html; charset=UTF-8">` &mdash; HTML4

Ссылки:
- [Юникод][19]
- [Набор символов][20]

Сам файл должен быть закодирован в UTF-8 формат (Atom это делает по-умолчанию).

### Обобщение простых элементов

- h1 &hellip; h6 &mdash; _блочные элементы,_ заголовки;
- p &mdash; _блочный элемент,_ абзац;
- div &mdash; _простой блочный элемент,_ (часто используется для структурирования элементов);
- hr &mdash; _блочный элемент,_ горизонтальная линия;
- a &mdash; _строчный элемент,_ ссылка;
- b, strong &mdash; _строчные элементы,_ жирный и сильно выделенный элемент (см. [HTML5 Doctor][11]);
- i, em &mdash; _строчные элементы,_ курсивный и выделенный элемент (см. [HTML5 Doctor][11]);
- span &mdash; простой строчный элемент.

### Структурированные элементы

#### Списки

- нумерованные `ol`
- маркированные `ul`

Нумерованные
```html
<ol>
	<li>текст</li>
	<li>текст</li>
	<li>текст</li>
	…
</ol>
```

Маркерованные
```html
<ol>
	<li>текст</li>
	<li>текст</li>
	<li>текст</li>
	…
</ol>
```

## Таблицы

Простая структура

```html
<table>
	<tr>
		<th>текст</th>
		<th>текст</th>
		<th>текст</th>
	</tr>
	<tr>
		<td>текст</td>
		<td>текст</td>
		<td>текст</td>
	</tr>
</table>
```

Полная структура

```html
<table>
	<thead>
		<tr>
			<th>текст</th>
			<th>текст</th>
			<th>текст</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>текст</td>
			<td>текст</td>
			<td>текст</td>
		</tr>
	</tbody>
</table>
```

# Структурные элементы

- `<header>` — «шапка», заголовочная часть сайта, блока, раздела и т. п.
- `<footer>` — «подвал», заключительная часть сайта, блока, раздела и т. п.
- `<section>` — некий раздел в документе, например, тематически сгрупперованная информация, часто с заголовком.
- `<nav>` — блок с навигацией.
- `<article>` — содержание, например, статья в блоге, журнале, газете, комментарий, пост на форуме и т. д. Все что может рассматриваться как самостоятельный блок информации.

### Полезные ссылки

0. [w3.org][4]
1. [html5doctor.com][5]
1. [MDN][23]

[1]: https://ru.wikipedia.org/wiki/Бернерс-Ли,_Тим
[2]: https://ru.wikipedia.org/wiki/Консорциум_Всемирной_паутины
[3]: https://ru.wikipedia.org/wiki/HTML
[4]: http://www.w3.org/Consortium/ "World Wide Web Consortium (W3C)"
[5]: http://html5doctor.com/ "HTML5 Doctor, helping you implement HTML5 today"
[6]: ./index.ru.html "Документ"
[7]: ./tag_containers.ru.html "Парные и непарные теги"
[8]: ./attributes.ru.html "Атрибуты"
[9]: ./blocks.ru.html "Блочные элементы"
[10]: ./inline.ru.html "Строчные элементы"
[11]: http://html5doctor.com/i-b-em-strong-element/ "The i, b, em, &amp; strong elements | HTML5 Doctor"
[12]: http://www.w3schools.com/html/html_entities.asp
[13]: http://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references
[14]: http://htmlarrows.com/
[15]: http://www.w3schools.com/html/html_symbols.asp
[16]: https://ru.wikipedia.org/wiki/Двоичная_система_счисления
[18]: https://ru.wikipedia.org/wiki/Шестнадцатеричная_система_счисления
[19]: http://www.w3.org/International/articles/definitions-characters/
[20]: http://www.w3schools.com/tags/ref_charactersets.asp
[21]: http://www.w3schools.com/tags/att_meta_http_equiv.asp
[22]: http://generator.lorem-ipsum.info/
[23]: https://developer.mozilla.org/ru/docs/Web/HTML
