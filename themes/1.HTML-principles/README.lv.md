# Tīmeklis un HTML

## Vispārējā informācija

0. Timotijs Džons "Tims" Bērnerss-Lī (angl.: *Timothy John "Tim" Berners-Lee*):
	- globālā tīmekļa izgudrotājs,
	- Vispasaules Tīmekļa konsorcija (*W3C*) pašreizējais vadītājs.
	- [wikipedia.org][1]
	- [w3.org][4]

0. Vispasaules Tīmekļa konsorcijs (angl.: *World Wide Web Consortium* jeb *W3C*) ([wikipedia.org][2]):
	- standarti jeb "rekomendācijas"

0. Hiperteksta iezīmēšanas valoda jeb HTML (no angļu: HyperText Markup Language):
	- tīmekļa lappušu izstrāde;
	- specifikāciju pamatā uztur W3C ([wikipedia.org][3]).

## HTML

### Sintakse

HTML-dokumentu iezīmē ar īpašiem atslēgvārdiem — tagiem.

#### Iezīmes (angl. *tag*) uzbūve

- Simbols &lt;
- Taga nosaukums
- Simbols &gt;

[Piemērs][6]:
```html
<taga_nosaukums>
```

#### Pāra un nepāra tagi

Pāra tagi:
```html
<taga_nosaukums>…</taga_nosaukums>
```

Nepāra tagi:
```html
<taga_nosaukums />
```
vai
```html
<taga_nosaukums>
```

Abi ir pieļaujami, taču pirmais tiek uzskatīts par stingrāku.

[Piemērs][7]

**Ar tagiem veido elementus.**

Eksistē standarta tagu apkopojums:

- [w3schools.com][23] (en)
- [html5doctor.com][24] (en)

taču ir pieļaujams izmantot nestandarta tagus.

#### Atribūti

Atriūtos norāda papildu parametrus tagam. Tie var ietekmēt elementa vizuālam izskatam. Atribūtus liek sākuma tagā, beigu tagā NEKAD neliek.

<ins>*PAREIZI*</ins>:
```html
<taga_nosaukums atribūts="vērtība">…</taga_nosaukums>
<taga_nosaukums atribūts="vērtība" />
<taga_nosaukums atribūts="vērtība">
```
<del>*NEPAREIZI*</del>:
```html
<taga_nosaukums atribūts="vērtība">…</taga_nosaukums atribūts="vērtība">
```

##### Karogatribūts (flags)

Atribūts bez vērtības.

```html
<taga_nosaukums atribūts>…</taga_nosaukums>
<taga_nosaukums atribūts />
<taga_nosaukums atribūts>
```

[Piemērs][8]

### Standarta elementi

#### Blokveida (__block__) elementi

##### Virsraksti

```html
<h1>Pirmā līmeņa virsraksts</h1>
<h2>Otrā līmeņa virsraksts</h2>
…
<h6>Sestā līmeņa virsraksts</h6>
```

Eksistē tikai sešu līmeņu virsraksti. Pārējie HTML-elementi netiek numurēti.

##### Rindkopa

```html
<p>… … …</p>
<p>… … …</p>
```

##### Horizontālais atdalītājs

```html
<hr />
```

##### Vienkāršs bloks

```html
<div>
	… … … … … …
	… … … … … …
	… … … … … …
</div>
```

[Piemērs][9]

### Rindas (__inline__) elementi

```html
<strong>stipri izcelts teksts</strong>
<em>izcelts teksts</em>
<span>sagrupēts teksts</span>
<br /> <!-- teksta pārnese -->
```

Par `<strong>` un `<em>` &mdash; sk. [HTML5 Doctor][11]

[Piemērs][10]

### Elementi elementu iekšā

#### __Inline__-elements blokā

```html
<p>Donec sed odio dui. <strong>Nulla vitae</strong> elit libero, a pharetra augue. Donec id elit non mi porta gravida at eget metus. Vivamus sagittis lacus vel augue <em>laoreet</em> rutrum faucibus dolor auctor. Praesent commodo cursus magna, vel scelerisque nisl consectetur et.</p>
```

#### Blokveida elementi blokā

```html
<section>
	<h1>Hello world!</h1>
	<div>
		<p>Donec sed odio dui. Nulla vitae elit libero, a pharetra augue. Donec id elit non mi porta gravida at eget metus. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Praesent commodo cursus magna, vel scelerisque nisl consectetur et.</p>
	</div>
</section>
```

### Atstarpes

Jebkuras atstarpes un *tab*-simboli, jebkurā skaitā pārlūks attēlo ka **vienu** atstarpi.

```html
Donec sed odio dui.       Nulla vitae elit libero,
a pharetra augue. 	Donec id elit non mi porta gravida at eget metus.
```

**Rezultāts:** Donec sed odio dui. Nulla vitae elit libero, a pharetra augue. Donec id elit non mi porta gravida at eget metus.

### Speciālie simboli

Angl. __HTML entities__

#### Uzbūve

- `&`
	- nosaukums vai
	- `#` un numurs (decimālais) vai
	- `#x` un numurs (heksadecimālais)
- `;`

#### Piemērs

- `&cent;` — &cent;
- `&#162;` — &#162;
- `&#xA2;` — &#xA2;

Vērtīgas norādes:

- [w3schools: html_entities][12]
- [w3schools: html_symbols][15]
- [wikipedia][13]
- [htmlarrows.com][14]

### HTML-dokumenta pamatstruktūra

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

Paskaidrojums:
- `<!doctype html>` — HTML-dokumenta deklarācija, tiek rakstīta pirmajā rindiņā
- `<html>` — saknes elements, kas satur `<head>` un `<body>`
- `<head>` — galvene, domāta tehniskās informācijas iekļaušanai (pārlūkam, tīmekļa servisiem)
- `<body>` — dokumenta pamatdaļa, kurā tiek iekļauta visa redzamā informācija
- `<title>` — dokumenta virsraksts, kurš ir redzams cilnēs (*tab*) vai grāmatzīmēs (*bookmark*)

### Kodējums

- [Unikods][19]
- [Simbolu kopas][20]
- kodējumu HTML norāda ([info][21]):
	- `<meta charset="utf-8" />` &mdash; HTML5
	- `<meta http-equiv="content-type" content="text/html; charset=UTF-8">` &mdash; HTML4

Pašam failam ir jābūt iekodētam UTF-8 kodējumā. *Atom* to dara pēc noklusējuma.

### Vienkāršo elementu apkopojums

- h1 &hellip; h6 &mdash; blokveida satura elementi, virsraksti;
- p &mdash; blokveida satura elements, rindkopa (paragrāfs);
- div &mdash; vienkāršs blokveida elements (lapas uzbūvei);
- hr &mdash; blokveida satura elements, horizontālā līnija;
- a &mdash; rindas elements, enkurs, (norāžu (*link*) izveidošanai);
- b, strong &mdash; rindas elements, treknraksts bez/ar uzsvaru (sk. [HTML5 Doctor][11]);
- i, em &mdash; rindas elements, slīpraksts bez/ar uzsvaru (sk. [HTML5 Doctor][11]);
- span &mdash; vienkāršs rindas elements.

### Strukturētie elementi

#### Saraksti

- numurēts `ol`
- nenumurēts `ul`

```html
<ol>
	<li>teksts</li>
	<li>teksts</li>
	<li>teksts</li>
	…
</ol>

<ul>
	<li>teksts</li>
	<li>teksts</li>
	<li>teksts</li>
	…
</ul>
```


#### Tabulas

Vienkārša struktūra
```html
<table>
	<tr>
		<th>teksts</th>
		<th>teksts</th>
		<th>teksts</th>
	</tr>
	<tr>
		<td>teksts</td>
		<td>teksts</td>
		<td>teksts</td>
	</tr>
</table>
```

Pilna struktūra
```html
<table>
	<thead>
		<tr>
			<th>teksts</th>
			<th>teksts</th>
			<th>teksts</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>teksts</td>
			<td>teksts</td>
			<td>teksts</td>
		</tr>
	</tbody>
</table>
```

### Noderīgās saites

0. [w3.org][4]
1. [html5doctor.com][5]

# Uzdevums \#1

Sastādīt divus HTML dokumentus, **katrā** ar:

0. Vienu virsrakstu
0. Diviem apakšvirsrakstiem
0. Divām rindkopām (attiecīgām apakšvirsrakstiem), kurās ir:
	- treknrakstā iezīmēti vārdi
	- slīprakstā iezīmēti vārdi
	- norāde uz otru dokumentu
	- norāde uz ārējo resursu, kas atveras jaunajā cilnē

Tekstam izmantot *Lorem ipsum* ģenerātoru, tādu kā [generator.lorem-ipsum.info][22]

# Uzdevums \#2

Izveidot *web*-lapas izkārtojuma pamatelementu (augošs uzdevums).

	doctype html
	html
	|
	+— head
	|	|
	|	+— title
	|
	+— body
		|
		h1 …
		|
		p …

[1]: https://lv.wikipedia.org/wiki/Tims_B%C4%93rnerss-L%C4%AB
[2]: https://lv.wikipedia.org/wiki/Vispasaules_T%C4%ABmek%C4%BCa_konsorcijs
[3]: https://lv.wikipedia.org/wiki/HTML
[4]: http://www.w3.org/Consortium/ "World Wide Web Consortium (W3C)"
[5]: http://html5doctor.com/ "HTML5 Doctor, helping you implement HTML5 today"
[6]: ./index.lv.html "Dokuments"
[7]: ./tag_containers.lv.html "Pāra un nepāra tagi"
[8]: ./attributes.lv.html "Atribūti"
[9]: ./blocks.lv.html "Blokveida elementi"
[10]: ./inline.lv.html "Inline elementi"
[11]: http://html5doctor.com/i-b-em-strong-element/ "The i, b, em, &amp; strong elements | HTML5 Doctor"
[12]: http://www.w3schools.com/html/html_entities.asp
[13]: http://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references
[14]: http://htmlarrows.com/
[15]: http://www.w3schools.com/html/html_symbols.asp
[19]: http://www.w3.org/International/articles/definitions-characters/
[20]: http://www.w3schools.com/tags/ref_charactersets.asp
[21]: http://www.w3schools.com/tags/att_meta_http_equiv.asp
[22]: http://generator.lorem-ipsum.info/
[23]: http://www.w3schools.com/tags/default.asp
[24]: http://html5doctor.com/element-index/
