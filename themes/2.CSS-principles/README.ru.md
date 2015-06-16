# CSS

## Полезные ссылки

0. [CSS (w3schools)][1]
0. [Валидатор][2]

## Подключение и применение

0. В качестве атрибута в любом html-элементе `<span style="…">…</span>`
1. В html-элементе `<style>…</style>` (чаще всего внутри `<head>…</head>`)
2. Во внешнем файле &#42;.css, подключается в HTML с помощью кода `<link rel="stylesheet" href="путь/к/файлу.css" />`
	- браузер кеширует &rarr; быстрее загружается
	- HTML отдельно от CSS &rarr; легче читается

## Синтаксис

```css
селектор {
	свойство-1: значение-1;
	свойство-2: значение-2;
	свойство-3: значение-3-1 значение-3-2 … значение-3-M;
	…
	свойство-N: значение-N;
}
```

0. Селектор — указание на соответствующий HTML-элемент;
1. Свойство — параметр визуального оформления;
2. Значение — значение визуального оформления.

[Пример][3]

## Селекторы <small>[Info][12]</small>

### Селекторы элементов

- совпадает с название тега (без угловых скобок);
- определяет внешний вид для всех заданных элементов.

```css
p {
	…
}
```

### Селекторы классов

- начинается с `.`
- оформляет группу элементов

[Пример][4]

```css
.red {
	…
}
```

### ID селекторы

- наичнаются с `#`
- ссылаются на уникальный элемент
- в HTML не может использоваться больше одного раза

[Пример][5]

	#info {
		…
	}

_Крайне не рекомендуется к использованию. Поскольку в современной верстке почти никогда нельзя быть уверенным, что элемент никогда больше не повторится._

## Сложные селекторы <small>[Info][13]</small>

### Контекстные селекторы

Выбирает элементы, которые находятся внутри другого элемента, причем независимо от уровня вложения.

[Пример][6]

```css
p span {
	…
}
```

### *Child*-селектор

Выбирает элементы, которые находятся непосредственно внутри другого элемента (прямые потомки).

[Пример][7]

```css
p > span {
	…
}
```

### Соседние селекторы

Выбирает элементы, которые стоят за элементом, на одном уровне.

[Пример][8]

Ближайший сосед

```css
a + span {
	…
}
```

## Единицы измерения <small>[Info][10]</small>

### Абсолютные

- px (используется чаще всего)
- cm
- mm
- in
- pt

### Относительные

- em
- rem
- %

Пример: размер элемента

```html
<div class="myelmt">…</div>
```
```css
.myelmt {
	width: 100px;
	height: 50px;
}
```

## Цвета

### Системы счисления <small>[info][29]</small>

- [двоичная][21];
- [восьмеричная][22];
- десятичная;
- [шестнадцатеричная][23]:
	- для создания *html-enities*;
	- цвета CSS.

Указание цветов:
- RGB
	- В HEX формате
		- 6 цифр, пример `#AF89D1` или `#af89d1`
		- 3 цифры (если в каждой паре одинаковые цифры), пример `#AA88DD` можно предстваить как `#A8D` или `#a8d`
	- rgb(N, N, N) c тремя десятичными цифрами
	- rgba(N, N, N, N) c тремя десятичными цифрами и уровнем полупрозрачности (дробное значение от 0 до 1)

- название цвета
	- red
	- lightblue *и т. п.*
	- [info][15]

## Фон <small>[info][16]</small>

	background: [color] [image] [repeat] [attachment] [position]

- background
	- color
	- image
	- repeat
	- attachment
	- position
- background-size (отдельно)

[Пример][17]

## Текст <small>[info][18]</small>

### Цвет

	color: #FF00AC

### Свойства текста

	text-align: left|right|center|justify|initial|inherit;
	text-decoration: none|underline|overline|line-through|initial|inherit;
	text-transform: none|capitalize|uppercase|lowercase|initial|inherit;
	text-indent: 0|vērtība px/em/rem/% utt.|initial|inherit;

	line-height: normal|number|length|initial|inherit;
	vertical-align: baseline|vērtība px/em/rem/% utt.|sub|super|top|text-top|middle|bottom|text-bottom|initial|inherit;
	white-space: normal|nowrap|pre|pre-line|pre-wrap|initial|inherit;

	letter-spacing: normal|vērtība px/em/rem/% utt.|initial|inherit;
	word-spacing: normal|vērtība px/em/rem/% utt.|initial|inherit;

### Шрифт <small>[info][19]</small>

Общее свойство для указания параметров шрифта.

	font: [[font-style] [font-variant] [font-weight]] font-size/line-height font-family|initial|inherit;

Отдельные свойства:

	font-style: normal|italic|oblique|initial|inherit;
	font-variant: normal|small-caps|initial|inherit;
	font-weight: normal|bold|initial|inherit;
	font-size: medium|xx-small|x-small|small|large|x-large|xx-large|smaller|larger|vērtība px/em/rem/% utt.|initial|inherit;
	font-family: название|"название из нескольких слов"|initial|inherit;

[Пример][20]

## Списки <small>[info][24]</small>

Общее свойство: значения указываются в произвольном порядке.
```css
list-style: list-style-type list-style-position list-style-image
```

Отдельные свойства:

0. list-style-type — тип маркера, возможные значения:
	- для ненумерованных списков: *circle*, *square*, **disc** (по умолчанию)
	- для нумерованных списков: **decimal** (по умолчанию), *lower-alpha*, *lower-roman*, *upper-alpha*, *upper-roman* utt. — sk. [info][25]
0. list-style-position — значения: **outside** (по умолчанию), *inside* — [info][26]
0. list-style-image — картинка как маркер, [info][27], vērtības: **none** (по умолчанию) или *url("путь/к-файлу.ext")*

[Piemērs][28]:
```html
<ul class="my-circle">
	<li>Lorem</li>
	<li>Ipsum</li>
	<li>Dolor</li>
</ul>
```
```css
ul.my-circle {
  list-style-type: circle;
}
```

[1]: http://www.w3schools.com/css/css_intro.asp
[2]: https://jigsaw.w3.org/css-validator/
[3]: ./css.html
[4]: ./class.html
[5]: ./id.html
[6]: ./context.html
[7]: ./child.html
[8]: ./sibling.html
[9]: ./attribute.html
[10]: http://www.w3schools.com/cssref/css_units.asp
[11]: http://www.w3schools.com/css/css_attribute_selectors.asp
[12]: http://www.w3schools.com/css/css_selectors.asp
[13]: http://www.w3schools.com/css/css_combinators.asp
[14]: https://css-tricks.com/yay-for-hsla/
[15]: http://www.w3schools.com/cssref/css_colornames.asp
[16]: http://www.w3schools.com/css/css_background.asp
[17]: ./background.html
[18]: http://www.w3schools.com/css/css_text.asp
[19]: http://www.w3schools.com/css/css_font.asp
[20]: ./font.html
[21]: https://ru.wikipedia.org/wiki/Двоичная_система_счисления
[22]: https://ru.wikipedia.org/wiki/Восьмеричная_система_счисления
[23]: https://ru.wikipedia.org/wiki/Шестнадцатеричная_система_счисления
[24]: http://www.w3schools.com/css/css_list.asp
[25]: http://www.w3schools.com/cssref/pr_list-style-type.asp
[26]: http://www.w3schools.com/cssref/pr_list-style-position.asp
[27]: http://www.w3schools.com/cssref/pr_list-style-image.asp
[28]: ./list.html
[29]: https://ru.wikipedia.org/wiki/Система_счисления
