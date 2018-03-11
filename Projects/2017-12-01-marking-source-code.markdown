---
layout: post
title:  "Marking source code"
date:   2018-03-10 16:18:45 +0200
author: "Jozef Varga"
depth: 2
parent: /Projects/
categories: projects
---

# Text zadania

Zdrojový kód je možné obohatiť o špecializované značky, obsahujúce vlastnosti častí zdrojových kódov, napríklad hodnotenie kvality inými vývojármi alebo automaticky určené pachy v zdrojovom kóde. Takéto značky sú obsahovo pomerne skromné. Zväčša obsahujú iba informácie určujúce ich typ, číselné hodnotenie a určenie pozície v zdrojovom kóde. Týchto značiek je však pomerne veľké množstvo a obsahujú dôležité informácie o zdrojovom kóde, ktoré vie využiť vývojár pri analýze a posudzovaní existujúceho zdrojového kódu ako aj pri implementovaní nového zdrojového kódu.

Analyzujte scenáre interakcie vývojárov so zdrojovým kódom a existujúce metódy zobrazujúce vlastnosti zdrojového kódu. Zvoľte jeden scenár a pre tento scenár navrhnite metódu vizualizácie vlastností zdrojového kódu, ktoré sú v tomto scenári pre vývojára užitočné. Vlastnosti navrhnutej metódy overte prostredníctvom implementovaného prototypu.

# Riešenie

V tejto práci sa venujeme vývoju rozšírenia do vývojárskeho prostredia, ktoré umožňuje rôznymi spôsobmi vizualizovať aplikačné logy priamo pri zdrojovom kóde. Podstatou práce je vytvorenie rozšírenia, ktoré podporí prácu vývojára pri vylaďovaní systému a odstraňovaní chýb. Hlavnou funkcionalitou rozšírenia je schopnosť spracovania aplikačné logy ako prúd dát a následnú vizualizáciu týchto dát vo vhodnej forme. 

Náplňou práce je analýza problému tvorby, spracovania a vizualizácie logov. Obsahuje rozbor dobrých zvykov pri tvorbe logu a existujúcich riešení vizualizácie. Práca opisuje taktiež návrh riešenia a samotnú implementáciu. Záverom práce je overenie riešenia a vyhodnotenie výsledkov.

Cieľom práce je odbremeniť vývojárov od nutnosti hľadať prepojenia medzi zdrojovým kód systému a aplikačnými logmi, ktoré generuje, a poskytnúť im spojitý pohľad na aplikáciu v prevádzke.
