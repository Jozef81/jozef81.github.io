---
layout: post
title:  "Personal static web page  :star2:"
date:   2018-03-10 16:18:45 +0200
author: "Jozef Varga"
depth: 2
parent: /Projects/
categories: projects
---

# Zadanie 1: Osobná webová prezentácia na GitHub pages

Vytvorte webovú prezentáciu (webové sídlo) o sebe. Zamerajte sa jednak na vaše profesné záujmy (napr. projekty, ktoré riešite/riešili ste, čo vás v informatike najviac baví, fascinuje = váš developerský profil) a jednak vaše osobné záujmy, hobby.

V rámci developerského profilu vytvorte sekciu Webové publikovanie, kde budete publikovať všetky tri vaše vypracované zadania z predmetu.

Využite pritom technológie Git + GitHub Pages + Jekyll + Markdown. Využite potenciál statického generátora Jekyll a jeho templatovacích možností.

Podrobné požiadavky na vypracovanie a odovzdanie zadania (priemerná úroveň kvality):

- Sídlo musí obsahovať aspoň 5 podstránok, pri využití aspoň 3 rôznych rozložení (layout-ov)

- V rámci šablon musí byť použité:
	* aspoň 5 premenných
	* kolekcie alebo dátové súbory
    * aspoň 5 filtrov alebo tagov
    * aspoň 1 plugin (okrem pagination)
	
Source: [Zdroj zadania](https://wiki.fiit.stuba.sk/study/bc/info/wp/2017-18/zadanie1/)
	
# Riešenie

Mnou vytvorené statické sídlo je vytvorené pomocou generátora [**Jekyll**](https://jekyllrb.com/). Základný layout je postavený na téme [Minima](https://github.com/jekyll/minima), ktorá je upravená pre moje potreby. Štýl stránky je modifikovaný pomocou CSS súborov, ktorých základ je v rámci témy Minima. Časť CSS súborov je prebratých od [Alfred G. Fischer](http://a-g-f.github.com/metro-ui-jekyll/), ktoré sú tiež mierne upravené pre potreby konzistentného vzhľadu.

Použité obrázky su prevzaté z [PSDgraphics](http://www.psdgraphics.com)

Webové sídlo je rozdelené do niekoľkých častí. Každý logický celok má svoje vlastné rozloženie.

**Zoznam _layouts_:**
* default
	* základný layout, ktorý zahŕňa hlavičku, telo a pätičku stránky
	* tento layout používajú všetky ostatné
* docs
	* layout pre zobrazenie zoznamu postov v obrátenom chronologickom poradí
	* tak tiež obsahuje RSS feed
* home
	* tento layout opisuje vzhľad domovskej stránky
	* obsahuju tabuľku 2*2 s obrázkami ako linkami na podstránky
* post
	* obsahuje názov, dátum, meno autora a obsah postu
* cv
	* obdobný layout ako *post*, vyčlenený samostatne pre budúce úpravy
* page
	* jednoduchý layout pre zobrazenie názvu a obsahu stránky
	* aktuálne nevyužívam
* projects
	* toto rozloženie obsahuje dva zoznamy projektov, ktoré sú rozdelené na základe statusu projektu
	* zoznam obsahuje názov projektu, predmet, dátum
	
**Zoznam _includes_:**
* footer
	* obsahuje meno autora, email a linky na sociálne siete
* header
	* obsahuje názov stránky a navigačné menu
* head
	* obsahuje charset a css
* social
	* obsahuje zoznam sociálnych médií
	
**Použité prvky**
V jednotlivých layoutoch sú použité rôzne prvky. Najčastejšie použitými prvkami sú premenné _page.title_, _site.pages_, _page.date_. V layoute projects využívam premenné, ktoré používajú údaje z dátového súboru, ktorý obsahuje zoznam projektov s ich vlastnosťami ako je názov, predmet, dátum, url a status. 
Pri definovaní odkazov používam _relative_url_ a pri converzií dátumu _date_to_xmlschema_. V rámci navigačného menu používam dve zoraďovania, prvé je na základe mnou určeného poradia uloženého v premennej _sort_ a druhé je zoradenie projektov v navigácií podľa názvu.
	
**Použité pluginy:**
* [jekyll-jemoji](https://github.com/yihangho/emoji-for-jekyll)
* [jekyll-feed](https://github.com/jekyll/jekyll-feed)

	




