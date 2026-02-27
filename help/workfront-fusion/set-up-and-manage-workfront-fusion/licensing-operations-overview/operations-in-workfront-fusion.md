---
title: Bewerkingen
description: Een bewerking in Adobe Workfront Fusion is een taak die door een module wordt uitgevoerd. Voor het volgen van doeleinden, is om het even welke succesvolle actie die door een module wordt uitgevoerd een verrichting.
author: Becky
feature: Workfront Fusion
exl-id: c14e2bb2-1cce-48ff-8bea-acc9829d3cf2
source-git-commit: d630251ec01f5e11bad0305a2f49fb447bf1dd1e
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 1%

---

# Bewerkingen

Een bewerking in Adobe Workfront Fusion is een taak die door een module wordt uitgevoerd. Voor het volgen van doeleinden, is om het even welke succesvolle actie die door een module wordt uitgevoerd een verrichting.

## Overwegingen bij het tellen van het aantal verrichtingen

* In het algemeen wordt elke succesvolle uitvoering in de stap beschouwd als een bewerking.
* De eerste module in een scenario loopt slechts eenmaal en wordt altijd geteld als één verrichting, zelfs als het geen bundel terugkeert.
* Het aantal keren dat de rest van de gebruikte modules afhangt van het aantal bundels dat zij moeten verwerken.  Één looppas van een module voor één bundel is één verrichting. Een uitzondering hierop is de aggregatormodule, die wordt geteld als één bewerking per set bundels die wordt verwerkt.
* Bewerkingen kunnen in waarde verschillen. Sommige zijn kleiner, eenvoudiger en andere zijn complexer. De verrichtingen tellen naar uw totaal ongeacht hoe eenvoudig of complex zij kunnen zijn.
* Bewerkingen worden meegeteld in het [!UICONTROL Finalization] -werkgebied van de uitvoering van een scenario.
* Het volgende wordt **niet** geteld als verrichtingen:
   * Alle filterstappen.
   * Elke handeling die fouten of haltes oplevert.
   * Om het even welke route die niet loopt omdat de regels van de route niet werden voldaan, zoals reserve of gehandicapte routes.
   * Om het even welke actie die niet loopt, of omdat een filter geen gegevens door toeliet of omdat het scenario wegens een fout werd gestopt.

>[!NOTE]
>
>Als uw organisatie routinematig meer bewerkingen probeert te gebruiken dan uw Workfront Fusion-pakket toestaat, raden wij u aan een upgrade naar het Ultimate-pakket Automation and Integration te overwegen.

## Bedrijfslimieten

Uw organisatie heeft mogelijk een limiet voor maandelijkse bewerkingen. Dit is gebaseerd op het Workfront-abonnement dat uw organisatie heeft aangeschaft. Het [!UICONTROL Ultimate] Workfront-plan biedt onbeperkte bewerkingen.

Als uw organisatie een maandelijkse limiet heeft, ontvangt u een melding wanneer uw organisatie de limiet bijna heeft bereikt. Als uw organisatie de limiet overschrijdt, neemt Workfront contact op met uw organisatie om ervoor te zorgen dat uw abonnement aan uw behoeften voldoet.

Workfront Fusion verzendt een melding wanneer uw organisatie de volgende percentages van de maandelijkse limiet van de organisatie bereikt:

* 50%
* 75%
* 90%
* 100%

## Het aantal bewerkingen weergeven dat in de afgelopen 30 dagen is uitgevoerd

U kunt een grafiek zien waarin het aantal uitgevoerde bewerkingen wordt weergegeven. Deze grafieken zijn beschikbaar op de volgende locaties:

* **dashboard van de Organisatie**: Verrichtingen die door de volledige organisatie worden gebruikt
* **dashboard van het Team**: Verrichtingen die door scenario&#39;s worden gebruikt die door dit team worden bezeten
* **de detailspagina van het Scenario**: Verrichtingen die door dit scenario worden gebruikt
