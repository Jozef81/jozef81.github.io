---
layout: post
title:  "Document transformation to XHTML and PDF  :star2:"
date:   2018-05-02 18:18:18 +0200
author: "Jozef Varga"
depth: 2
parent: /Projects/
categories: projects
---

# Zadanie 3: XML prezentácia

Analyzujte možnosti zápisu jednoduchej prezentácie v jazyku XML. Identifikujte základné súčasti prezentácie a navrhnite XML elementy pre ich označkovanie (metadátové, štrukturálne, inline). Dbajte na znovupoužiteľnosť a vyvarujte sa redundancií. Návrh elementov zrealizujte opísaním typu dokumentu pomocou vybraného jazyka (DTD, XSD, RELAX NG) spolu s vysvetlením účelu jednotlivých elementov. Vo vami navhrnutom jazyku vytvorte ukážkovú prezentáciu, ktorá bude demonštrovať možnosti tvorby prezentácií podľa definície typu dokumentu.

Navrhnite a vytvorte XSLT šablóny pre konverziu prezentácie z XML do XHTML+CSS a pre konverziu prezentácie z XML do PDF. Klaďte dôraz na znovupoužitie jednotlivých šablon pre viaceré výstupné formáty. Umožnite zadávanie parametrov transformácií.

Súčasťou požiadaviek na zadanie je vytvorenie správy o zadaní 3, v ktorej zdokumentujete splenie jednotlivých bodov zadania. Správa bude súčasťou vašej stránky o Webovom publikovaní na GitHube.
	
Source: [Zdroj zadania](https://wiki.fiit.stuba.sk/study/bc/info/wp/2017-18/zadanie3/)
	
# Riešenie

Body zadania:

*    opis typu dokumentu + opis účelu navrhnutých elementov 
	- na opis typu dokumentu som si vybral xml schemu
	- korenovým elementom je prezentacia, ktorá obsahuje meta dáta a slidy
	- meta dáta obsahuju informácie o prezentácií ako je autor, zdroje a pod.
	- slidy obsahujú elementy určujúce jeho obsah a rozloženie
	- niektoré elementy obsahujú atribúty, ktoré sú definované pomocou číselníkov

*    vytvorenie ukážkovej XML prezentácie demonštrujúcej možnosti definície typu dokumentu 
	- ukážková prezentácia obsahuje všetky elementy definované v xml scheme, na prezentovanie obsahu
	
*    základný návrh XSL transformácií, ich vhodnosť, parametrizácia 
	- pre každý layout je vytvorený samostatný template
	- vačšina podelementov má svoje vlastné template-y podľa použitia
	- parametrami je možné nastaviť farbu a velkost pisma

*    vytvorenie XSLT pre konverziu prezentácie z XML -> XHTML+CSS 
	- ako už bolo spomenuté takmer každý element má vytvorený template
	- typy layoutov sú definované v xml scheme a pre kazdy je vytvoreny samostatny template

*    vytvorenie XSLT pre konverziu prezentácie XML -> PDF 
	- transformácie do PDF obsahujú transformáciu jednotlivých elementov
	- pre každý element typu slide je vytvorená nová stránka v PDF
	


	



