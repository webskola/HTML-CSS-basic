# CSS

## Noderīgās saites

0. [CSS (w3schools)][1]
0. [Validators][2]

## Iekļaušana

0. pašā html-elementā `<span style="…">…</span>`
1. html-elementā `<style>…</style>` (iekš `<head>…</head>`)
2. ārējā failā &#42;.css ar `<link rel="stylesheet" href="ceļš/uz/failu.css" />`
	- pārlūks iekešo &rarr; ātrāk ielādējas
	- HTML atsevišķi no CSS &rarr; pārskatāmāk

## Sintakse

	selektors {
		īpašība-1: vērtība-1;
		īpašība-2: vērtība-2;
		īpašība-3: vērtība-3-1 vērtība-3-2 … vērtība-3-M;
		…
		īpašība-N: vērtība-N;
	}

0. Selektors — norāda uz attiecīgo/-ajiem HTML dokumenta elementiem;
1. Īpašība — vizuālā noformējuma parametrs;
2. Vērtība  — vizuālā noformējuma parametra vērtība.

[Piemērs][3]

## Selektori <small>[Info][12]</small>

### Elementu selektori

- sakrīt ar taga nosaukumu;
- atlasa visus elementus.

Piemērs:

	p {
		…
	}

### Klašu selektori

- sākas ar `.`
- veido elementu grupu

[Piemērs][4]

	.red {
		…
	}

### ID selektori

- sākas ar `#`
- norāda uz unikālo elementu
- nedrīkst atkārtoties

[Piemērs][5]

	#info {
		…
	}

## Saliktie selektori <small>[Info][13]</small>

### Konteksta selektors

Atlasa elementu/-us, kas ir iekš kāda elementa, neatkarīgi no struktūras.

[Piemērs][6]

	p span {
		…
	}

### *Child*-selektors

Atlasa elementu/-us, kas ir iekš kāda elementa un ir tā tiešie pēcteči.

[Piemērs][7]

	p span {
		…
	}

### Kaimiņselektors

Atlasa elementu/-us, kas stāv aiz kāda elementa vienā līmenī.

[Piemērs][8]

	a + span {
		…
	}

	strong ~ em {
		…
	}

### Atribūtu selektors <small>[Info][11]</small>

	[atribūts] {
		…
	}

	[atribūts = "vērtība"] {
		…
	}

	[atribūts ^= "sākas ar"] {
		…
	}

	[atribūts *= "satur"] {
		…
	}

	[atribūts $= "beidzas ar"] {
		…
	}

[Piemērs][9]

## Mērvienības <small>[Info][10]</small>

### Absolūtās

- px (biežāk)
- cm
- mm
- in
- pt
- px

### Relatīvās

- em
- rem
- %
- utt.

Piemērs: elementa izmērs

	<div class="myelmt">…</div>

	.myelmt {
		width: 100px;
		height: 50px;
	}

#### Skaitīšanas sistēmas

	- [Binārā][21];
	- [Oktālā][22];
	- Decimālā;
	- [Heksadecimālā][23]:
		- *html-enities* veidošanai;
		- CSS krāsās.

## Krāsas

- RGB
	- HEX formātā
		- 3 cipari uz vienu krāsu
		- ja vienādi pa diviem — var lietot 3 ciparus
	- rgb(N, N, N) ar 3 decimālajiem cipariem
	- rgba(N, N, N, N) ar caurspīdīgumu
- HSL (hue, saturation, lightness)
	- hsl(N, N, N)
	- hsla(N, N, N, N) ar caurspīdīgumu
	- [info][14]

- krāsas vārds
	- red
	- lightblue *u.t.t.*
	- [info][15]

## Fons <small>[info][16]</small>

	background: [color][image][repeat][attachment][position]

- background
	- color
	- image
	- repeat
	- attachment
	- position
- background-size (atsevišķi)

[Piemērs][17]

## Teksts <small>[info][18]</small>

### Krāsa

	color: css krāsa

### Teksta īpašības

	text-align: left|right|center|justify|initial|inherit;
	text-decoration: none|underline|overline|line-through|initial|inherit;
	text-transform: none|capitalize|uppercase|lowercase|initial|inherit;
	text-indent: 0|vērtība px/em/rem/% utt.|initial|inherit;

	line-height: normal|number|length|initial|inherit;
	vertical-align: baseline|vērtība px/em/rem/% utt.|sub|super|top|text-top|middle|bottom|text-bottom|initial|inherit;
	white-space: normal|nowrap|pre|pre-line|pre-wrap|initial|inherit;

	letter-spacing: normal|vērtība px/em/rem/% utt.|initial|inherit;
	word-spacing: normal|vērtība px/em/rem/% utt.|initial|inherit;

### Šrifts <small>[info][19]</small>

Kopējā īpašībā vērtībās jānorāda tieši tādā secībā.

	font: [[font-style] [font-variant] [font-weight]] font-size/line-height font-family|initial|inherit;

Atsevišķas īpašības:

	font-style: normal|italic|oblique|initial|inherit;
	font-variant: normal|small-caps|initial|inherit;
	font-weight: normal|bold|initial|inherit;
	font-size: medium|xx-small|x-small|small|large|x-large|xx-large|smaller|larger|vērtība px/em/rem/% utt.|initial|inherit;
	font-family: nosaukums|"nosaukums vairākiem vārdiem"|initial|inherit;

[Piemērs][20]

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

[21]: http://lv.wikipedia.org/wiki/Binārā_skaitīšanas_sistēma
[22]: http://lv.wikipedia.org/wiki/Oktālā_skaitīšanas_sistēma
[23]: http://lv.wikipedia.org/wiki/Heksadecimālā_skaitīšanas_sistēma
