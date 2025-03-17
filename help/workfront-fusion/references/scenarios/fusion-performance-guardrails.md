---
title: Fusion Performance Guardraals
description: De automatisering van het werk vereist snelle verwerking, zodat wordt  [!DNL Adobe Workfront Fusion]  ontworpen voor hoge prestaties. Omdat de langlopende scenario's het tempo van uw werk kunnen vertragen, hebben wij  [!DNL Workfront Fusion]  met prestaties-bewarende begeleiding ontworpen die uitvoeringstijd, gegevensgrootte, en andere scenario parameters beperken. [!DNL Workfront Fusion]  de ontwerpers zouden zich van deze gidsen bewust moeten zijn en hen in hun ontwerppraktijken moeten opnemen.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
source-git-commit: 1253470a23a2a9124824d5ab1ff2b5013d773517
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Garanties voor Fusieprestaties

Voor werkautomatisering is snelle verwerking vereist, dus [!DNL Adobe Workfront Fusion] is ontworpen voor hoge prestaties. Omdat de langlopende scenario&#39;s het tempo van uw werk kunnen vertragen, hebben wij [!DNL Workfront Fusion] met prestaties-bewarende garanties ontworpen die uitvoeringstijd, gegevensgrootte, en andere scenario parameters beperken. [!DNL Workfront Fusion] ontwerpers dienen zich bewust te zijn van deze instructies en deze op te nemen in hun ontwerppraktijken.

## Browsers

* Workfront Fusion ondersteunt alleen op Chrome gebaseerde browsers.

## Scenarios

* De time-out van de standaardscenario-uitvoering is **40 minuten**. Wanneer de uitvoering deze time-out bereikt, onderbreekt [!DNL Workfront Fusion] de uitvoering van het scenario na de volgende cyclus of bewerking, afhankelijk van het scenario. Dit dwingt het scenario om kort na het bereiken van de limiet van 40 minuten te stoppen
* De maximumgrootte van een scenario blauwdruk is **5 MB**, maar wij adviseren het houden van scenario grootte onder **3 MB**.

  App-modules die gegevens met een groot aantal velden maken of bijwerken, kunnen zeer grote blauwdrukken veroorzaken.

   * Wanneer u de app [!DNL Workfront] gebruikt, moet u alleen velden selecteren die nodig zijn voor het maken of bijwerken van gebruiksgevallen.
   * Wanneer u andere toepassingen gebruikt, gebruikt u aangepaste API-modules voor interactie met elk recordtype met een groot aantal velden.

* Hoewel er geen plafond is voor het aantal modules in een scenario, hebben scenario&#39;s met meer dan 150 modules een negatief effect op de prestaties van uw [!DNL Workfront Fusion] systeem. Daarom adviseren wij het creëren van scenario&#39;s met meer dan 150 modules niet.

## Bewerkingen

* De standaardverrichtingonderbreking is typisch **40 seconden**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## Bestanden

* De totale verwerkingscapaciteit van de fusie voor dossiers is **1 GB**. De limiet is gebaseerd op de totale geheugenkosten. Elke operatie draagt aan die kosten bij. Als één bestand van 400 MB wordt gedownload en geüpload, kost de totale bestandscapaciteit 800 MB.
* Organisaties op het Workfront Ultimate-plan hebben toegang tot meer dan 1 GB aan bestandsverwerking. Het Fusion-platform kan ondersteuning bieden voor afzonderlijke bestanden van maximaal 15 GB voor één actie (bijvoorbeeld uploadbestand), maar er zijn andere factoren die van invloed zijn op de gegevensoverdracht. De maximale bestandsgrootte van één actie is afhankelijk van de verbinding die Fusion voor webservices maakt. Gegevensoverdracht is de totale verwerking voor één uitvoering. Dit betekent dat meerdere acties in één uitvoering bijdragen aan de totale gegevensoverdracht. Fusion verwerkt bestanden totdat de uitvoerlimiet van 40 minuten is bereikt.

Voor meer informatie, zie [ Werkend met grote dossiers ](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Gebruik van servergeheugen

* Het geheugengebruik van de server voor één enkele uitvoering is beperkt tot **1 GB**.

  Veel factoren, zoals grote bestanden of complexe modules, kunnen het servergeheugengebruik beïnvloeden op manieren die moeilijk te voorspellen of te controleren zijn. Daarom kan de uitvoering van uw scenario de geheugenlimiet van 1 GB overschrijden, zelfs als het scenario alle andere prestatiegaranties volgt. Als de geheugenlimiet wordt overschreden, mislukt de uitvoering.

## Webhaken

* De standaardmaximumgrootte van een lading is **5 MB**.
* Webhooks zijn beperkt tot **100 verzoeken per seconde**. Wanneer deze limiet is bereikt, verzendt Workfront Fusion de status 429 ([!UICONTROL Too Many Requests]).
* In [!DNL Workfront Fusion] worden de payloads van de webhaak 30 dagen opgeslagen. De toegang tot van een Web-haaklading meer dan 30 dagen nadat het werd ontvangen resulteert in de fout &quot;[!UICONTROL Failed to read file from storage.]&quot;
* Webhaken worden automatisch gedeactiveerd als een van de volgende twee situaties van toepassing is:

   * De webhaak is langer dan 5 dagen niet verbonden met een scenario
   * De webhaak wordt alleen gebruikt in inactieve scenario&#39;s, die al meer dan 30 dagen inactief zijn.

* gedeactiveerde webhaken worden automatisch verwijderd en niet geregistreerd als ze niet zijn aangesloten op scenario&#39;s en meer dan 30 dagen in de gedeactiveerde status zijn geweest.

## Uitvoeringshistorie

* De geschiedenislogboeken van de uitvoering zijn beperkt tot een grootte van **100 MB**. Als de uitvoeringsgeschiedenis deze grootte overschrijdt, slechts zal eerste 100 MB worden getoond.
* Als een scenario veelvoudige gezamenlijke uitvoeringen heeft. er worden slechts 5 uitvoeringen weergegeven in het gedeelte Uitvoeringen van de pagina met de details van het scenario. Dit geldt zelfs wanneer meer dan vijf uitvoeringen worden uitgevoerd.

## Onvolledige uitvoeringen

* De onvolledige uitvoeringen zijn beperkt tot een totale grootte van **500 MB**. Als de limiet van 500 MB is bereikt, worden geen onvolledige uitvoeringen meer opgeslagen.

## Opnieuw

* Wanneer het gebruiken van de module van de Onderbreking en het specificeren van de richtlijn van het Opnieuw proberen, als een scenario achtereenvolgens 10 keer binnen een 2 minieme chronologie ontbreekt, zal het scenario automatisch worden gedeactiveerd.

## Herhaling

Recursie treedt op wanneer een scenario een nieuwe uitvoering van zich teweegbrengt, die een nieuwe uitvoering, etc. in een oneindige lijn teweegbrengt.

Bijvoorbeeld, wordt een scenario teweeggebracht wanneer een taak wordt gecreeerd, en dat scenario leidt tot twee taken. De nieuw gecreëerde taken allebei teweegbrengen opnieuw het scenario teweeg, dat vier nieuwe taken creeert. Telkens als een taak wordt gecreeerd, wordt het scenario teweeggebracht, en telkens als het scenario loopt, verdubbelt het aantal taken. Het aantal taken groeit exponentieel.

De recursie kan prestatieskwesties voor zowel de organisatie veroorzaken die het recursieve scenario, als aan andere organisaties bezit.

Overweeg het volgende met betrekking tot recursie:

* **wanneer een scenario recursie veroorzaakt, wordt het gedeactiveerd door het technische team van de Fusie om verdere prestatieskwesties te verhinderen.**
* Omdat de recursie een resultaat van scenario ontwerp is, moet u uw scenario&#39;s op een manier ontwerpen die ervoor zorgt dat het scenario geen acties omvat die het scenario teweegbrengen.

