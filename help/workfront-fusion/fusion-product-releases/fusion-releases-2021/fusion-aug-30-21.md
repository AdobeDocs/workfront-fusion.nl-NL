---
title: Workfront Fusion release activity:&nbsp;Week van 30 augustus 2021
description: Workfront Fusion release activity:&nbsp;Week van 30 augustus 2021
author: Luke
draft: Probably
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: cac11147-5b3d-477b-869b-e255528c4bec
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Workfront Fusion release activity: Week van 30 augustus 2021

Op deze pagina worden alle verbeteringen beschreven die in Adobe Workfront Fusion in de week van 30 augustus 2021 zijn aangebracht.

Voor een lijst van alle recente veranderingen, zie [&#x200B; de versieactiviteit van de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Voor een lijst van recente insectenmoeilijke situaties in de Fusie van Workfront, zie de [&#x200B; pagina van de Updates van het Onderhoud van Workfront &#x200B;](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=nl-NL) en controleer om het even welke updates geëtiketteerd de Update van het Onderhoud van de Fusie van Workfront.

## Gebeurtenissen filteren die de module Workfront > Watch-gebeurtenissen activeren

1. Een aangepast filter instellen voor gebeurtenissen die de module Workfront > Watch-gebeurtenissen activeren

   Om het aantal onnodige scenario looppas te verminderen, hebben wij Workfront > de registratiemodule van het Controle bijgewerkt om gebeurtenis het filtreren toe te laten. U kunt nu een filter instellen wanneer u een webhaak maakt. Hierdoor kan het scenario alleen worden geactiveerd wanneer de gebeurtenis aan bepaalde criteria voldoet.

   Het gebeurtenisfilter biedt momenteel de volgende bewerkingen:

   * Gelijk: Trigger een scenario slechts wanneer een gebeurtenis de voorwaarden van de filter aanpast. U kunt bijvoorbeeld een filter instellen dat alleen een scenario activeert als de gebeurtenis in een bepaald project plaatsvindt.
   * Niet gelijk: activeer een scenario alleen als een gebeurtenis niet voldoet aan de voorwaarden van het filter. U kunt bijvoorbeeld een filter maken dat alleen een scenario activeert als de uitgave waarin een gebeurtenis plaatsvindt, geen status Gesloten heeft.

   Eerder, zou de module van het Horloge verslagen alle verslagen terugwinnen. Gebruikers kunnen alleen filteren door later filters in het scenario in te stellen.

   Als u wilt profiteren van het filteren van gebeurtenissen, maakt u een nieuwe webhaak in de module voor controlegebeurtenissen. Het is momenteel niet mogelijk om bestaande websites te bewerken om deze functionaliteit in te bouwen. We raden u ten zeerste aan nieuwe webhooks te maken met behulp van gebeurtenisfilters voor bestaande scenario&#39;s.

1. Filter gebeurtenissen uit die door de huidige verbinding worden geactiveerd.

   We hebben het meest gangbare gebeurtenisfilter toegevoegd om uw websites gemakkelijker in te stellen voor de module Workfront > Watch-gebeurtenissen. Nu, heeft webhaak een optie om uit om het even welke veranderingen te filtreren die door modules worden aangebracht gebruikend de verbinding die voor de module van de Gebeurtenissen van het Controle wordt gespecificeerd. Met andere woorden, als dit filter is ingeschakeld, kunnen wijzigingen die door de Workfront-gebruiker zijn aangebracht in verband met die verbinding, het scenario niet activeren.

   Eerder was dit filter niet beschikbaar. Daarom was het gemakkelijker voor veranderingen die in de modules van Workfront worden aangebracht om scenario&#39;s teweeg te brengen die die modules bevatten, potentieel veroorzakend scenario&#39;s om zich in een oneindige lijn teweeg te brengen.
