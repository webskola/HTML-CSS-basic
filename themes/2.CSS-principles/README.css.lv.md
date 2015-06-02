# CSS

## Noderīgās saites

0. [CSS (w3schools)][1]
0. [Validators][2]

## Iekļaušana

0. pašā html-elementā `<span style="…">…</span>`
1. html-elementā `<style>…</style>` (iekš `<head>…</head>`)
2. ārējā failā *.css ar `<link rel="stylesheet" href="ceļš/uz/failu.css" />`
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

[1]: http://www.w3schools.com/css/css_intro.asp
[2]: https://jigsaw.w3.org/css-validator/
[3]: ./css.html

