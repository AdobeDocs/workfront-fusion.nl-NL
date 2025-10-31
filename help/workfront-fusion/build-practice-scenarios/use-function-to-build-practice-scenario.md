---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Een functie gebruiken om een project bij te werken in een basisscenario
description: Leer hoe u een functie toevoegt om een tijdelijk item bij te werken in Workfront.
author: Becky
feature: Workfront Fusion
exl-id: aa082ac8-48e8-4569-880e-024dd77feaa1
source-git-commit: 3a977d805c10fda7209b0634c6e32e818a980691
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Een functie gebruiken om een project bij te werken in een basisscenario

Het bijwerken van een Workfront-werkitem is een veelgebruikte manier om Workfront Fusion te gebruiken. In dit voorbeeld gebruikt u een functie om de naam van een project in hoofdletters te wijzigen.

Fusion omvat vele soorten functies die u toestaan om voorwaardelijke logica op uw gegevens om te zetten en uit te voeren. Voor meer informatie bij het gebruiken van functies, zie [ Overzicht van de Functie ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

Dit voorbeeld wijzigt het scenario dat in [ wordt gecreeerd leidt tot een basisscenario ](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Vereisten

U moet het scenario tot stand brengen dat in [ wordt beschreven leidt tot een basisscenario ](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) alvorens deze procedure te volgen.

## Een functie gebruiken om een project bij te werken

### Voeg de module Record bijwerken toe aan uw scenario

1. Open het scenario in de scenarioredacteur.
1. Beweeg de cursor over de gedeeltelijke cirkel rechts van de sectie van de tweede module en klik vervolgens op **[!UICONTROL Add another module]** .
1. Selecteer Adobe Workfront in de lijst met toepassingen en kies vervolgens de module **[!UICONTROL Update Record]** .
1. Selecteer in het veld Id het ID-blok onder de module Object omzetten. Dit is identiteitskaart van het project dat output door die module was.

   ![ identiteitskaart van voorwerp van de Bekeerling ](assets/id-convert-object.png)

1. Selecteer Project in het veld Type record, omdat het object dat u wilt bijwerken een project is.
1. Selecteer Naam in het gebied Selecteer velden voor kaart.

   Er wordt een naamveld geopend.
1. Ga aan [ kaart de functie voor de naamupdate ](#map-the-function-for-the-name-update) verder.

### De functie toewijzen voor de naamupdate

Wanneer dit scenario een verzoek in een project omzet, is de naam van het project het zelfde als het verzoek. De functie neemt deze naam en geeft alle letters in die naam een hoofdletter.

1. Klik het **gebied van de Naam**.

   Het deelvenster Toewijzing wordt geopend.
1. In het mappingpaneel, klik het **Tekst en binaire functies** pictogram. ![ de functies van de Tekst pictogram ](assets/toolbar-icon-text&binary-functions.png)
1. Selecteer de functie **bovenaan**.

   De functie wordt weergegeven in het veld Naam, inclusief de opmaak voor de invoer die de functie verwacht.

   De invoer voor dit voorbeeld is de naam van de uitgave waaruit het project is geconverteerd.

1. Plaats de cursor tussen de ronde haakjes, want dit is waar de invoer naartoe gaat.
1. In het mappingpaneel, klik het **pictogram van de output van de Module 0} {.** ![ het outputpictogram van de Module ](assets/toolbar-icon-functions-you-map-from-other-modules.png)
1. Selecteer het naamblok dat door de eerste module werd uitgevoerd.

   Het naamblok wordt weergegeven in de functie.

   ![ het blok van de Naam in functie ](assets/map-name.png)

1. Klik **O.K.** om de modulemontages te bewaren.

### Testen en activeren

1. Test het scenario door **in werking te stellen eens** in de laag-linkerhoek van het scherm te klikken.
1. Onderzoek de output om ervoor te zorgen dat het scenario zoals verwacht liep.
1. Wanneer u wordt tevreden dat het scenario zoals verwacht werkt, klik **plannend** knevel in laag-linkervan het scherm aan ****.

   Dit activeert het scenario. De actieve scenario&#39;s lopen volgens het programma dat in de trekkermodule wordt geplaatst.
1. Klik in Workfront Fusion op **[!UICONTROL Save]** in de linkerbenedenhoek om de voortgang van het scenario op te slaan.

   >[!IMPORTANT]
   >
   >Sla de bestanden vaak op terwijl u ze gebruikt en test een scenario.

## Bronnen

* [Items toewijzen met behulp van functies](/help//workfront-fusion/create-scenarios/map-data/map-using-functions.md)
