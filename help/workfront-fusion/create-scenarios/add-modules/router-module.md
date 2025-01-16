---
title: Voeg een module van de Router toe en vorm routes
description: De module van de Router staat u toe om uw stroom in verscheidene routes te vertakken en de gegevens binnen elke route verschillend te verwerken. Zodra een module van de Router een bundel ontvangt, door:sturen het aan elke verbonden route in de orde de routes aan de module van de Router in bijlage waren.
author: Becky
feature: Workfront Fusion
exl-id: 8344cde4-df3e-4b72-9d10-46ff4b186400
source-git-commit: 839f6edf93df8a935b2c5d0a520bdc125fe60288
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Voeg een module van de Router toe en vorm routes

De module van de Router staat u toe om uw scenario in verscheidene routes te vertakken, en de gegevens binnen elke route verschillend te verwerken. Wanneer een module van de Router een bundel ontvangt, door:sturen het aan elke verbonden route in de orde de routes in bijlage aan de module van de Router waren.

Routes worden opeenvolgend verwerkt, niet parallel. Een bundel wordt niet verzonden naar de volgende route tot het volledig door de vorige route is verwerkt.


## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie</td> 
   <td> <p>Nieuw: [!UICONTROL Standard]</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidig: Geen [!DNL Workfront Fusion] vereiste licentie.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] [!DNL Workfront] -abonnement: uw organisatie moet het abonnement aanschaffen [!DNL Adobe Workfront Fusion] .</li><li>[!UICONTROL Ultimate] [!DNL Workfront] abonnement: [!DNL Workfront Fusion] is opgenomen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet [!DNL Adobe Workfront Fusion] aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Voeg een module van de Router aan een scenario toe

U moet een module van de Router toevoegen alvorens routes te vormen.

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u een router wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. In de scenario redacteur, klik op het juiste handvat van de module waarna u de router wilt toevoegen.
1. Selecteer **[!UICONTROL Flow Control]** > **Router** in de lijst van modules die toont.

   ![](assets/connect-the-router-350x108.png)

   of

   Om de module van de Router tussen twee modules op te nemen, klik op het moersleutelpictogram onder de route die de twee modules verbindt en selecteer **[!UICONTROL Add a router]** van het menu.

   ![](assets/insert-router-350x191.png)
1. Voeg de eerste route aan de router toe door op het juiste handvat van de router te klikken en een module toe te voegen, gelijkend op het toevoegen van om het even welke module.
1. Om een andere route toe te voegen, klik de routermodule. Er wordt een route weergegeven. Voeg modules aan deze route toe zoals gewenst.

   U kunt zoveel routes toevoegen als u wilt.

1. Om de orde van de routes te verifiëren, klik het auto-richt pictogram ![ auto-richt pictogram ](assets/auto-align.png).

   De routes worden geschikt in de orde zij uitvoeren. De hoogste route voert eerst uit.

1. (Facultatief) om routeorde te veranderen, ontkoppel de routes door op de weg van de router met de rechtermuisknop te klikken en ontkoppelen te selecteren, dan hen te slepen aan de routermodule in de gewenste orde. De eerste route in bijlage zal de eerste uit te voeren route (de hoogste route) zijn.

1. Ga aan [ toe Voeg een filter aan een route ](#add-a-filter-to-a-route).

## Een filter toevoegen aan een route

U kunt een filter op een route na de module van de Router aan filterbundels zetten. Slechts zullen de bundels die door de filter overgaan door de modules op de route worden behandeld.

Als de gegevens de filter van meer dan één route overgaan, worden de gegevens behandeld door beide routes. De hoogste route behandelt eerst de gegevens.

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waaraan u een filter wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik het moersleutelpictogram ![ Sleutel ](assets/wrench-icon.png) op de weg waar u een filter wilt plaatsen. Dit is de weg tussen de routermodule en de eerste module van de route.
1. Selecteer **Opstelling een filter.**
1. Voeg een label toe in het labelveld van het deelvenster dat wordt weergegeven. Dit etiket toont in het scenario.
1. Configureer filtervoorwaarden.

   Voor meer informatie, zie [ een filter aan een scenario ](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md) toevoegen.

1. Klik op **[!UICONTROL OK]** om de filterinstelling op te slaan.

1. Ga aan [ verder vormen een reserveroute ](#configure-a-fallback-route).

## Vorm een reserveroute

De reserveroute is de route die op om het even welke bundels uitvoert die geen filter tot een andere route overgaan.

U kunt een terugvalroute in het filterpaneel toelaten.

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u een reserveroute wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik het moersleutelpictogram ![ Sleutel ](assets/wrench-icon.png) op de weg waar u een filter wilt plaatsen. Dit is de weg tussen de routermodule en de eerste module van de route.
1. Selecteer **Opstelling een filter.**
1. Voeg een label toe in het labelveld van het deelvenster dat wordt weergegeven. Dit etiket toont in het scenario.
1. Schakel het selectievakje voor de terugvalroute in.

   ![](assets/fallback-route-350x260.png)

1. Klik op **[!UICONTROL OK]** om de filterinstelling op te slaan.

De route van de Fallback is duidelijk met een verschillende pijl in de module van de Router:

![](assets/arrow-sign-in-router-module-350x361.png)

## Voorbeeld: `if/else` use case

>[!BEGINSHADEBOX]

Een typisch gebruiksgeval van de reserveroute moet de stroom met één route voortzetten als aan de voorwaarde en met een andere route wordt voldaan als het niet is. zoals in de volgende stappen:

In dit voorbeeld, wordt de eerste route gevormd met een filter. Dit vertegenwoordigt de component `if` .

![](assets/set-up-a-filter-2-350x242.png)

De tweede route wordt gevormd als reserveroute. Dit vertegenwoordigt de component `else` .

![](assets/enable-fallback-route-option-350x238.png)

>[!ENDSHADEBOX]
