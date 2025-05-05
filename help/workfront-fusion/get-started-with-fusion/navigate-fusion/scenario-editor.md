---
title: De scenario-editor
description: De scenario redacteur staat u toe om scenario's in een visuele interface tot stand te brengen en uit te geven.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# De scenario-editor

De scenario redacteur staat u toe om scenario&#39;s in een visuele interface tot stand te brengen en uit te geven.

![ redacteur Scenario ](assets/scenario-editor.jpg)

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configuraties op toegangsniveau*</td> 
   <td> 
     <p>U moet een [!DNL Workfront Fusion] beheerder voor uw organisatie zijn.</p>
     <p>U moet een [!DNL Workfront Fusion] beheerder voor uw team zijn.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Open de scenario-editor en voeg een module toe:

1. Klik **[!UICONTROL Scenarios]** {het pictogram van 1} Scenario&#39;s ![&#128279;](assets/scenarios-icon.png) in het linkerpaneel.
1. Klik het pictogram van het vraagteken ![ vraagpictogram ](assets/question-mark-full-size.png), dan vind en klik app of de dienst die u met wilt beginnen. Voor gedetailleerde informatie over het vormen van een module, zie [ een module ](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md) vormen.

## Beschikbare scenario-editoracties

### Uw scenario uitvoeren

| Handeling | Details |
|----------|----------|
| Het scenario testen | Controleer of het scenario wordt uitgevoerd zoals u verwacht voordat u het activeert. Nadat het scenario is geactiveerd, wordt het volgens het schema uitgevoerd. Als alles niet zoals verwacht loopt, zie [ fout behandeling ](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) toevoegen om te leren hoe te om fouten te behandelen. |

![ looppasscenario knoop ](assets/run-your-scenario.png)

### Planning

| Handeling | Details |
|----------|----------|
| Het scenario plannen | Door gebrek, loopt een scenario om de 15 minuten. U kunt dit veranderen door te bepalen wanneer en hoe vaak een geactiveerd scenario loopt. De scenario&#39;s van de fusie kunnen worden gepland zo vaak zoals om de 5 minuten te lopen. Voor meer informatie, zie [ Plan een scenario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

![ het plannen paneel ](assets/scheduling-scenario-editor.png)

### Besturingselementen

| Handeling | Details |
|----------|----------|
| Opslaan | Nadat u het scenario hebt opgeslagen, is er een nieuwe versie beschikbaar in het menu met drie punten voor het geval u deze in de toekomst wilt gebruiken. Eerder opgeslagen versies van scenario&#39;s zijn slechts beschikbaar gedurende 60 dagen. |
| Scenario-instellingen | Het deelvenster met scenario-instellingen bevat geavanceerde instellingen voor het scenario. Voor meer informatie over de beschikbare montages, zie [ scenario montages ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md) vormen. |
| Notities | Notities maken over het scenario. Andere gebruikers kunnen deze notities bekijken wanneer ze zich in het scenario bevinden. |
| Automatisch uitlijnen | De modules in uw scenario automatisch uitlijnen. |
| Uitleg stroom | Bekijk een animatie die toont hoe de gegevens door het scenario stromen. |
| Gereedschappen voor ontwikkelen | Met het gereedschap Ontwikkelen kunt u alle handmatige uitvoering van uw scenario controleren, alle uitgevoerde bewerkingen controleren en de details van elke uitgevoerde API-aanroep bekijken. U kunt zien welke module, verrichting, of enige reactie de fout veroorzaakte, en die kennis gebruiken om uw scenario te verfijnen. Voor meer informatie, zie [ zuivert een scenario ](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Meer | In het menu Meer kunt u blauwdrukken importeren of exporteren en het scenario terugzetten naar vorige versies. |

![ controles paneel ](assets/controls-editor-scenario.png)

### Gereedschappen

| Handeling | Details |
|----------|----------|
| Stroomregeling | Configureer instellingen om de manier te bepalen waarop gegevens worden doorlopen. Voor meer informatie, [ zie nodig verbinding ]. |
| Gereedschappen | De hulpmiddelensectie bevat verscheidene nuttige modules die uw scenario&#39;s kunnen verbeteren. Voor meer informatie, [ zie nodig verbinding ]. |
| Tekstparser | Gebruik het parserhulpmiddel van de Tekst om tekst voor gebruik in andere scenario&#39;s te ontleden. Voor de tekstparser is geen verbinding vereist. Voor meer informatie, [ zie nodig verbinding ]. |

![ hulpmiddelenpaneel ](assets/tools-scenario-editor.png)

### Favorieten

U kunt het pictogram Favorieten gebruiken om modules toe te voegen die u vaak gebruikt.

![ het paneel van Favorieten ](assets/favorites-scenario-editor.png)
