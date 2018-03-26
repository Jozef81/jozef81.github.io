---
layout: post
title:  "Personal static web page  :star2:"
date:   2018-03-26 18:18:18 +0200
author: "Jozef Varga"
depth: 2
parent: /Projects/
categories: projects
---

# Zadanie 2: Transformácia vybraného dokumentu do formátu DocBook

Predmetom 2. zadania je spracovanie vybraného dokumentu (ideálne bakalárskeho projektu) z pôvodného ľubovoľného (Word, OpenOffice, LaTeX, …) formátu do formátu DocBook a vygenerovanie cieľového tvaru v PDF. Výsledný dokument bude mať rozsah minimálne 10 a maximálne 15 strán. Do rozsahu sa nezapočítavajú úvodné strany (obsah, zoznamy obrázkov a tabuliek), použitá literatúra a prílohy.

Požadované a kontrolné konštrukcie sú:

* štandardné členenie textu na kapitola, podkapitola, podpodkapitola, príloha, generovaný obsah,
* zvýraznenie slov, zvýraznenie členenia textu odrážkami alebo číslovaním,
* odkazy na iné časti vlastného dokumentu, prípadne odkazy na URL,
* poznámka pod čiarou,
* zoznam použitej literatúry a zdrojov vrátane ich citácie v texte,
* vloženie obrázku a tabuliek, odkazy na ne v texte; zoznam obrázkov a tabuliek v úvode alebo závere textu,
* vytvorenie registra pojmov (indexu) s pojmami hierarchicky usporiadanými do dvoch úrovni, napríklad „cykly, while“, „cykly, for“ (najmenej ako ukážku na 10-15 pojmoch na predvedenie práce s registrom).

Súčasťou požiadaviek na zadanie je vytvorenie správy o zadaní 2, ktorá bude súčasťou vašej stránky o Webovom publikovaní na GitHube. Správa o rozsahu 150-250 slov bude obsahovať informácie o použitých elementoch a atribútoch, prípadne ukážky XML/XSLT demonštrujúce vykonané prispôsobenie DocBook šablon (nepovinné).

Na transformáciu zo zdrojového formátu DocBook do PDF použite upravenú šablónu na základe šablóny od Jiřího Koska (obsahuje i ukážku).
	
Source: [Zdroj zadania](https://wiki.fiit.stuba.sk/study/bc/info/wp/2017-18/zadanie1/)
	
# Riešenie

Pre riešenie tohto zadania som použil prvú časť svojej bakalárskej práce, ktorú som najskôr z formátu **doc** konvertoval do formátu **xml**. 
Následne som dokument vo formáte **xml** upravoval pomocou DocBook elementov a ich atribútov. 

### Použité elementy a atribúty DocBook-u 

* **bookinfo**  	- obsahuje úvodné strany dokumentu ako je titulná strana a anotácie
* **chapter**   	- element, ktorý vymedzuje oblasť v ktorej sa nachádza obsah jednej kapitoly
* **section**   	- delí kapitoly na podkapitoly
* **indexterm** 	- hovorí o kľučových slovách v texte; jeho potomci sú **primary** a **secondary**, ktorý určujú úroveň v registry pojmov
* **orderedlist** - slúži na vygenerovanie číslovaného zoznamu; jeho potomok je **listitem**, ktorý obsahuje položku zoznamu
* **table**		- generuje tabulku; atribútmi sú **frame** - štýl orámovania, **id** - referencovateľný identifikátor
				- jeho potomok **tgroup** určuje atribútmi formát tabuľky; **cols** - počet stĺpcov, **align** - zarovnanie textu, **colsep** - oddelovač stĺpcov, **rowsep** - oddeľovač riadkov
* **figure**		- použitý na zobrazovanie obrázkov v texte; tak isto ako table obsahuje atribút **id** - referencovateľný identifikátor
				- obsahuje **title** - názov, **imageobject** - obsahuje **imagedate**, ktoré referencujú na súbor s obrázkom pomocou atribútu **fileref**, **scale** - percentuálna veľkosť obrázku
* **emphasis**	- slúži na zvýraznenie časti textu; používam s atribútom **role**, ktorý určuje spôsob zvýraznenia
* **footnote**	- generuje poznámku pod čiarou
* **index**		- generuje register z použitých **indexterm**
* **bibliography**	- zlučuje elementy týkajúce sa bibliografie
* **bibliomixed**		- slúži na vytvorenie konkrétneho odkazu na bibliografický zdroj; obsahuje **title** - názov, **ulink** - odkaz na link na webe, používa atribút **url**
	
Do šablóny **thesis.xsl** som pridal vlastný element, ktorý umožňuje vytvárať zlomy strán. Jeho následné použitie je pomocou **&lt;?hard-pagebreak?&gt;**.

{% highlight xml %}
<!-- page breaks -->
<xsl:template match="processing-instruction('hard-pagebreak')">
	<fo:block break-after='page'/>
</xsl:template>
{% endhighlight %}
	



