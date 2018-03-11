---
layout: post
title:  "Virtual Wallet :star:"
date:   2017-05-25 22:47:47 +0200
author: "Jozef Varga"
depth: 2
parent: /Projects/
categories: projects
---

# Zadanie

V rámci predmetu *Vývoj aplikácií s viacvrstvovou architektúrou* sme mali za úlohu vytvoriť aplikácií s niekoľkými vrstvami. Konkrétne zadanie sme si mali vymyslieť sami. Na projekte sme pracovali vo dvojiciach, čo umožnilo aj precvičenie práce s verziovacím nástrojom Git. 

Spolu s kolegom [Petrom](https://github.com/PeterLiptak) sme vytvorili client-server aplikáciu, ktorá združovala informácie o používateľských účtoch a umožňovala presúvať prostriedky medzi účtami. Taktiež umožňovala filtrovať transakcie, ukladať si priateľov a pod. 

Architektúra aplikácie pozostávala s nasledujúcich komponentov:
* tučný server, na ktorom bežala celá biznis logika
* databáza obsahujúca celý dátovy model
* tenký klient, ktorý sa dopytoval na server pomocou EJB	


Celý projekt si môžete pozrieť na [githube](https://github.com/PeterLiptak/virtual_wallet). :smile:

