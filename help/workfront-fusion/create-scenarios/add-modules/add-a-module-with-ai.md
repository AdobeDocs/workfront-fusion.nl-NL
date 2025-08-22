---
title: Een scenario-segment genereren met behulp van AI
description: U kunt AI gebruiken om een tekstherinnering in te gaan beschrijvend wat u een segment van uw scenario nodig hebt te doen. De fusie produceert dan één of meerdere modules die die acties uitvoeren, die u in uw scenario kunt gebruiken.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Een scenario-segment genereren met behulp van AI

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

U kunt AI gebruiken om een tekstherinnering in te gaan beschrijvend wat u een segment van uw scenario nodig hebt te doen. De fusie produceert dan één of meerdere modules die die acties uitvoeren, die u in uw scenario kunt gebruiken.

De geproduceerde scenario segmenten bevatten modules voor één enkele schakelaar. Om modules voor een verschillende schakelaar te produceren, creeer een afzonderlijke herinnering, dan sluit zich aan bij de scenariosegmenten in uw scenario.

Zoals met om het even wat die van AI wordt geproduceerd, adviseren wij dat u de geproduceerde modules tweemaal controleert en test om ervoor te zorgen dat zij zoals bedoeld presteren.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie</td> 
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] Workfront-abonnement: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>[!UICONTROL Ultimate] Workfront-abonnement: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Uw organisatie moet aan de volgende voorwaarden voldoen om deze functionaliteit te kunnen gebruiken:

* Uw organisatie moet hebben deelgenomen aan het Workfront AI Assistant Beta-programma.
* Adobe moet een ondertekende Adobe Gen AI-overeenkomst in het bestand hebben voor uw organisatie.

  Voor meer informatie bij het ondertekenen van de overeenkomst, zie [ de overeenkomst van Adobe Gen AI ](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement) in het artikelAI Hulpoverzicht in de documentatie van Workfront ondertekenen.

## Momenteel ondersteunde AI-moduletoepassingen

De Fusion AI kan momenteel modules genereren die verbinding maken met de volgende toepassingen:

* Adobe Firefly
* Azure OpenAI
* Microsoft Graph
* Adobe Workfront Planning
* Adobe Analytics
* Adobe PDF Services
* Adobe Marketo
* Adobe Frame.io
* Dropbox
* NetSuite
* Google-agenda
* Atlassian Jira
* GitLab
* Spotiseren
* Bitmap
* OpenAI
* Slack

## Modules genereren

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u een module wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik het **pictogram AI van de Medewerker** AI Medewerker pictogram ![ dichtbij de hoger-juiste hoek van het scherm.](assets/ai-assistant-icon.png)
1. Typ een tekstprompt in het deelvenster AI-assistent.

   Voor uiteinden op herinneringen, zie [ Uiteinden voor het creëren van herinneringen voor scenario segmenten ](#tips-for-creating-prompts-for-scenario-segments) in dit artikel.

   AI Assistant genereert de module of set modules.
1. (Voorwaardelijk) Voeg indien nodig uw API-token voor de toepassing toe aan de modules.
1. Controleer de modules om ervoor te zorgen dat zij voor de aangewezen toepassing en de actie worden gevormd.
1. (Voorwaardelijk) als de geproduceerde scenario sectie niet in bijlage aan uw scenario is, sleep het in plaats.

Wij adviseren het testen van de modules om ervoor te zorgen dat zij zoals bedoeld presteren.

## Tips voor het maken van aanwijzingen voor scenario-segmenten

Tekstopdrachten moeten minimaal de volgende informatie bevatten:

* De toepassing waarmee u verbinding maakt
* De handeling of handelingen die u wilt uitvoeren

>[!IMPORTANT]
>
>U kunt meer dan één module tegelijkertijd produceren, maar kunt slechts modules voor één toepassing tezelfdertijd produceren.

>[!BEGINSHADEBOX]

**Voorbeelden**:

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`
Dit omvat de toepassing `Workfront Planning` en de handeling `delete records` . Deze herinnering leidt tot drie modules, voor elk verslag dat zal worden geschrapt.
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`
Dit omvat de toepassing `Workfront Planning` en de handeling `change campaign summary` .
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`
Dit omvat de toepassing `Workfront Planning` en de handeling `get field details` .

Het volgende voorbeeld is NOT correct:

* `Generate an image in Adobe Firefly and upload it to Dropbox`

  Dit voorbeeld is onjuist omdat het meerdere toepassingen bevat

>[!ENDSHADEBOX]

Houd rekening met het volgende wanneer u tekstaanwijzingen maakt:

* Gebruik directe, eenvoudige taal.
* Controleer en test uw scenario segment. Als het niet zoals verwacht uitvoert, verfuw herinnering en probeer opnieuw.
