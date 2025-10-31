---
title: Voeg een module van de Router toe en vorm routes
description: De module van de Router staat u toe om uw stroom in verscheidene routes te vertakken en de gegevens binnen elke route verschillend te verwerken. Zodra een module van de Router een bundel ontvangt, door:sturen het aan elke verbonden route in de orde de routes aan de module van de Router in bijlage waren.
author: Becky
feature: Workfront Fusion
exl-id: 8344cde4-df3e-4b72-9d10-46ff4b186400
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Voeg een module van de Router toe en vorm routes

De module van de Router staat u toe om uw scenario in verscheidene routes te vertakken, en de gegevens binnen elke route verschillend te verwerken. Wanneer een module van de Router een bundel ontvangt, door:sturen het aan elke verbonden route in de orde de routes in bijlage aan de module van de Router waren.

Routes worden opeenvolgend verwerkt, niet parallel. Een bundel wordt niet verzonden naar de volgende route tot het volledig door de vorige route is verwerkt.


## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Elk Adobe Workfront Workflow-pakket en elk Adobe Workfront Automation and Integration-pakket</p><p>Workfront Ultimate</p><p>Workfront Prime en Select packages, met extra aanschaf van Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licenties</td> 
   <td> <p>Standard</p><p>Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Voeg een module van de Router aan een scenario toe

U moet een module van de Router toevoegen alvorens routes te vormen.

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u een router wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. In de scenario redacteur, klik op het juiste handvat van de module waarna u de router wilt toevoegen.
1. Selecteer **[!UICONTROL Flow Control]** > **Router** in de lijst van modules die toont.

   ![&#x200B; verbind de route &#x200B;](assets/connect-the-router-350x108.png)

   of

   Om de module van de Router tussen twee modules op te nemen, klik op het moersleutelpictogram onder de route die de twee modules verbindt en selecteer **[!UICONTROL Add a router]** van het menu.

   ![&#x200B; de router van het Tussenvoegsel &#x200B;](assets/insert-router-350x191.png)
1. Voeg de eerste route aan de router toe door op het juiste handvat van de router te klikken en een module toe te voegen, gelijkend op het toevoegen van om het even welke module.
1. Om een andere route toe te voegen, klik de routermodule. Er wordt een route weergegeven. Voeg modules aan deze route toe zoals gewenst.

   U kunt zoveel routes toevoegen als u wilt.

1. Om de orde van de routes te verifiëren, klik het auto-richt pictogram ![&#x200B; auto-richt pictogram &#x200B;](assets/auto-align.png).

   De routes worden geschikt in de orde zij uitvoeren. De hoogste route voert eerst uit.

1. (Facultatief) om routeorde te veranderen, klik op de module van de Router met de rechtermuisknop aan en selecteer **de routes van de Orde** Belemmering en laat vallen de routes in de orde u hen binnen wilt uitvoeren. De routes worden duidelijk door de eerste module die de router (de eerste module van de route) volgt.

   ![&#x200B; route van de Orde &#x200B;](assets/order-routes.png)

1. Ga aan [&#x200B; toe Voeg een filter aan een route &#x200B;](#add-a-filter-to-a-route).

## Een filter toevoegen aan een route

U kunt een filter op een route na de module van de Router aan filterbundels zetten. Slechts zullen de bundels die door de filter overgaan door de modules op de route worden behandeld.

Als de gegevens de filter van meer dan één route overgaan, worden de gegevens behandeld door beide routes. De hoogste route behandelt eerst de gegevens.

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waaraan u een filter wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik het moersleutelpictogram ![&#x200B; Sleutel &#x200B;](assets/wrench-icon.png) op de weg waar u een filter wilt plaatsen. Dit is de weg tussen de routermodule en de eerste module van de route.
1. Selecteer **Opstelling een filter.**
1. Voeg een label toe in het labelveld van het deelvenster dat wordt weergegeven. Dit etiket toont in het scenario.
1. Configureer filtervoorwaarden.

   Voor meer informatie, zie [&#x200B; een filter aan een scenario &#x200B;](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md) toevoegen.

1. Klik op **[!UICONTROL OK]** om de filterinstelling op te slaan.

1. Ga aan [&#x200B; verder vormen een reserveroute &#x200B;](#configure-a-fallback-route).

## Vorm een reserveroute

De reserveroute is de route die op om het even welke bundels uitvoert die geen filter tot een andere route overgaan.

U kunt een terugvalroute in het filterpaneel toelaten.

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u een reserveroute wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik het moersleutelpictogram ![&#x200B; Sleutel &#x200B;](assets/wrench-icon.png) op de weg waar u een filter wilt plaatsen. Dit is de weg tussen de routermodule en de eerste module van de route.
1. Selecteer **Opstelling een filter.**
1. Voeg een label toe in het labelveld van het deelvenster dat wordt weergegeven. Dit etiket toont in het scenario.
1. Schakel het selectievakje voor de terugvalroute in.

   ![&#x200B; route van de Fallback &#x200B;](assets/fallback-route-350x260.png)

1. Klik op **[!UICONTROL OK]** om de filterinstelling op te slaan.

De route van de Fallback is duidelijk met een verschillende pijl in de module van de Router:

![&#x200B; het teken van de Pijl in router &#x200B;](assets/arrow-sign-in-router-module-350x361.png)

## Voorbeeld: `if/else` use case

>[!BEGINSHADEBOX]

Een typisch gebruiksgeval van de reserveroute moet de stroom met één route voortzetten als aan de voorwaarde en met een andere route wordt voldaan als het niet is. zoals in de volgende stappen:

In dit voorbeeld, wordt de eerste route gevormd met een filter. Dit vertegenwoordigt de component `if` .

![&#x200B; Opstelling een filter in route &#x200B;](assets/set-up-a-filter-2-350x242.png)

De tweede route wordt gevormd als reserveroute. Dit vertegenwoordigt de component `else` .

![&#x200B; laat reserveoptie &#x200B;](assets/enable-fallback-route-option-350x238.png) toe

>[!ENDSHADEBOX]
