---
title: De scenario-editor
description: De scenario redacteur staat u toe om scenario's in een visuele interface tot stand te brengen en uit te geven.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: f968b9141173725160cea36575ad4e02a09a5e3f
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# De scenario-editor

De scenario redacteur staat u toe om scenario&#39;s in een visuele interface tot stand te brengen en uit te geven.

![&#x200B; redacteur Scenario &#x200B;](assets/scenario-editor.jpg)

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

## Open de scenario-editor en voeg een module toe:

1. Klik **[!UICONTROL Scenarios]** {het pictogram van 1} Scenario&#39;s ![&#x200B; in het linkerpaneel.](assets/scenarios-icon.png)
1. Klik het pictogram van het vraagteken ![&#x200B; vraagpictogram &#x200B;](assets/question-mark-full-size.png), dan vind en klik app of de dienst die u met wilt beginnen. Voor gedetailleerde informatie over het vormen van een module, zie [&#x200B; een module &#x200B;](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md) vormen.

## Beschikbare scenario-editoracties

### Uw scenario uitvoeren

| Handeling | Details |
|----------|----------|
| Het scenario testen | Controleer of het scenario wordt uitgevoerd zoals u verwacht voordat u het activeert. Nadat het scenario is geactiveerd, wordt het volgens het schema uitgevoerd. Als alles niet zoals verwacht loopt, zie [&#x200B; fout behandeling &#x200B;](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) toevoegen om te leren hoe te om fouten te behandelen. |

![&#x200B; looppasscenario knoop &#x200B;](assets/run-your-scenario.png)

### Planning

| Handeling | Details |
|----------|----------|
| Het scenario plannen | Door gebrek, loopt een scenario om de 15 minuten. U kunt dit veranderen door te bepalen wanneer en hoe vaak een geactiveerd scenario loopt. De scenario&#39;s van de fusie kunnen worden gepland zo vaak zoals om de 5 minuten te lopen. Voor meer informatie, zie [&#x200B; Plan een scenario &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

![&#x200B; het plannen paneel &#x200B;](assets/scheduling-scenario-editor.png)

### Besturingselementen

Mogelijk moet u op het pictogram met drie punten in het gebied Besturingselementen klikken om een aantal van deze besturingselementen weer te geven.

| Handeling | Details |
|----------|----------|
| Opslaan <p>![&#x200B; sparen pictogram &#x200B;](assets/save-icon.png)</p> | Nadat u het scenario hebt opgeslagen, is er een nieuwe versie beschikbaar in het menu met drie punten voor het geval u deze in de toekomst wilt gebruiken. Eerder opgeslagen versies van scenario&#39;s zijn slechts beschikbaar gedurende 60 dagen. |
| Scenario-instellingen <p>![&#x200B; de montagespictogram van het Scenario &#x200B;](assets/scenario-settings-icon.png)</p> | Het deelvenster met scenario-instellingen bevat geavanceerde instellingen voor het scenario. Voor meer informatie over de beschikbare montages, zie [&#x200B; scenario montages &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md) vormen. |
| Notities  <p>![&#x200B; pictogram van Nota&#39;s &#x200B;](assets/notes-icon.png)</p> | Notities maken over het scenario. Andere gebruikers kunnen deze notities bekijken wanneer ze zich in het scenario bevinden. |
| Automatisch uitlijnen <p>![&#x200B; auto-richt pictogram &#x200B;](assets/auto-align-icon.png)</p> | De modules in uw scenario automatisch uitlijnen. |
| De modules van het onderzoek ![&#x200B; modules van het Onderzoek &#x200B;](assets/search-modules-icon.png)  </p> | Ga een onderzoekstermijn in om van een module de plaats te bepalen, dan de onderzoeksresultaten te klikken die aan die module moeten worden genomen. U kunt zoeken op modulenaam, id, type of toepassing. |
| Uitleg stroom  <p>![&#x200B; verklaar het pictogram van de Stroom &#x200B;](assets/explain-flow-icon.png) </p> | Een animatie weergeven waarbij bewegende stippen aangeven hoe gegevens door het scenario lopen. |
| DevTool <p>![&#x200B; DevTool pictogram &#x200B;](assets/devtool-icon.png)</p> | Gebruikend DevTool, kunt u alle handlooppas van uw scenario controleren, alle uitgevoerde verrichtingen herzien, en de details van elke uitgevoerde API vraag zien. U kunt zien welke module, verrichting, of enige reactie de fout veroorzaakte, en die kennis gebruiken om uw scenario te verfijnen. Voor meer informatie, zie [&#x200B; zuivert een scenario &#x200B;](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Blauwdruk exporteren  <p>![&#x200B; het Vervagen van de Uitvoer pictogram &#x200B;](assets/export-blueprint-icon.png) </p> | Een blauwdruk van het huidige scenario exporteren. |
| Blauwdruk importeren  <p>![&#x200B; het pictogram van de Vervaging van de Invoer &#x200B;](assets/import-blueprint-icon.png) </p> | Een eerder geëxporteerde scenarioblauwdruk importeren. |
| Vorige versie  <p>![&#x200B; Vorig versiepictogram &#x200B;](assets//previous-version-icon.png) </p> | Eerdere versies van dit scenario weergeven. |

![&#x200B; controles paneel &#x200B;](assets/controls-editor-scenario.png)

### Gereedschappen

| Handeling | Details |
|----------|----------|
| Stroomregeling | Configureer instellingen om de manier te bepalen waarop gegevens worden doorlopen. Voor meer informatie, [ zie nodig verbinding ]. |
| Gereedschappen | De hulpmiddelensectie bevat verscheidene nuttige modules die uw scenario&#39;s kunnen verbeteren. Voor meer informatie, [ zie nodig verbinding ]. |
| Tekstparser | Gebruik het parserhulpmiddel van de Tekst om tekst voor gebruik in andere scenario&#39;s te ontleden. Voor de tekstparser is geen verbinding vereist. Voor meer informatie, [ zie nodig verbinding ]. |

![&#x200B; hulpmiddelenpaneel &#x200B;](assets/tools-scenario-editor.png)

### Favorieten

U kunt het pictogram Favorieten gebruiken om modules toe te voegen die u vaak gebruikt.

![&#x200B; het paneel van Favorieten &#x200B;](assets/favorites-scenario-editor.png)
