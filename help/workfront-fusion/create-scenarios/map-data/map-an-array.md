---
title: Een array- of arrayelement toewijzen
description: U kunt een array of afzonderlijke arrayelementen toewijzen aan een moduleveld in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 0534ad8a-af80-46d2-857d-de882a235edb
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Een array- of arrayelement toewijzen

Een array is een bundelitem dat het volgende kan bevatten:

* Een of meer waarden van hetzelfde type (eenvoudige array)
* Een of meer verzamelingen van hetzelfde type (complexe array)

>[!BEGINSHADEBOX]

**Voorbeeld:**

* **Complexe serie**: De [!UICONTROL Watch emails] module keert een serie van gehechtheid voor elke e-mail terug. Elke bijlage vertegenwoordigt een verzameling die een naam, inhoud, grootte enzovoort kan bevatten.

>[!ENDSHADEBOX]

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Een volledige array toewijzen

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waarin u een array wilt toewijzen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik in de module waaraan u de array wilt toewijzen, op het veld waar u de array wilt toewijzen. Dit is het veld waaraan de array wordt toegewezen.

1. Wijs het item toe in het vak dat wordt weergegeven.

   In het deelvenster kunt u velden op dezelfde manier toewijzen als bij elk ander type item. Als u niet elk item afzonderlijk wilt invullen, maar een andere array wilt toewijzen aan het doelveld, gebruikt u de knop [!UICONTROL Map] . In dit geval moet u ervoor zorgen dat beide arrays (de bronarray en de doelarray) dezelfde structuur hebben.

   U kunt elk gewenst aantal items aan een array toevoegen.

U kunt een array in afzonderlijke bundels verdelen met behulp van een iterator. Zie [[!UICONTROL Iterator] module in Adobe Workfront Fusion &#x200B;](/help/workfront-fusion/references/modules/iterator-module.md) voor meer informatie.

## Items toewijzen aan een nieuwe array

Met sommige velden in Workfront Fusion kunt u elementen toewijzen aan een array. U kunt bijvoorbeeld een array met items in de checklist maken in de Workfront Boards > Add checklist item module. Wanneer de module wordt uitgevoerd, worden alle items in de controlelijst aan de kaart toegevoegd.

Om het even welk modulegebied dat &quot;Add punt&quot;toont leidt tot een serie.

![&#x200B; voeg punt &#x200B;](assets/add-item.png) toe

Elementen toevoegen aan de array:

1. Klik **toevoegen punt**
1. Voer in het deelvenster dat wordt geopend details in over het item.
1. Klik **toevoegen**.
1. (Facultatief) herhaal stappen 1-3 voor elk element u aan de  serie wilt toevoegen.

## Matrixelementen toewijzen


### Array-elementen toewijzen op nummer

Array-elementen worden tussen vierkante haakjes weergegeven als een getal na de naam van de array. Met dit indexnummer kunt u een afzonderlijk element van een array in een veld toewijzen.

![&#x200B; Kaart eerste element &#x200B;](assets/map-array-1st-element.png)

>[!NOTE]
>
>Array-indexering in Workfront Fusion begint bij 1.

Een arrayelement toewijzen:

1. Klik op het veld waar u het element wilt toewijzen.

   Het deelvenster Toewijzing wordt geopend.

1. Zoek de array met het element dat u wilt toewijzen.
1. Klik op de vervolgkeuzepijl naast de array.
1. Klik op het element dat u wilt toewijzen.

   Het element wordt toegewezen, met index 1. Hierdoor wordt het eerste element in de array toegewezen.

1. Om een verschillend element van de serie in kaart te brengen, klik op [ 1 ] en ga het indexaantal van het serieelement in dat u wilt in kaart brengen.

   ![&#x200B; toegang tot een ander element &#x200B;](assets/access-another-element.png)

### Het element van een array toewijzen met een bepaalde sleutel

Sommige arrays bevatten verzamelingen met sleutelwaardeitems, zoals metagegevens, kenmerken, enzovoort. Als u een van deze waarden wilt gebruiken, kunt u een element opzoeken op basis van de opgegeven sleutelwaarde en de bijbehorende waarde ophalen uit het waardeitem. We raden u aan een formule te gebruiken die een combinatie van de functies `map()` en `get()` gebruikt.



>[!BEGINSHADEBOX]

In het volgende voorbeeld wordt de uitvoer van de [!DNL Jira] App getoond.

![&#x200B; Output van module Jira &#x200B;](assets/output-of-jira-app-350x100.png)

In dit voorbeeld wordt een bestandsnaam opgehaald uit een array van bijlagen, voor de specifieke bijlage met een id van 10108.

In dit voorbeeld wordt de volgende uitvoer gegenereerd:

![&#x200B; Output van module Jira &#x200B;](assets/output-from-jira-350x261.png)

De formule kan als volgt worden toegelicht:

* `map`

   1. De eerste parameter van de functie `map()` is het gehele arrayitem.
   1. De tweede parameter is de onbewerkte naam van het waardeitem. Als u de onbewerkte naam wilt verkrijgen, plaatst u de muisaanwijzer op het item in het deelvenster [!UICONTROL mapping] :

      ![&#x200B; verkrijgt ruwe naam &#x200B;](assets/obtain-raw-name-350x124.png)

      >[!NOTE]
      >
      >Alle parameters zijn hoofdlettergevoelig. Hoewel in dit voorbeeld het label van het item alleen in hoofdletters verschilt van de onbewerkte naam, is het nodig de onbewerkte naam te gebruiken.

   1. De derde parameter is de onbewerkte naam van het sleutelitem:

      ![&#x200B; Derde parameter &#x200B;](assets/3rd-parameter-350x166.png)

   1. De vierde parameter is de opgegeven sleutelwaarde.

  Omdat de functie `map()` een array retourneert (omdat er meer elementen met de opgegeven sleutelwaarde kunnen zijn), is het nodig de functie `get()` toe te passen om het eerste element op te halen:

* `get`

   1. De eerste parameter van de functie `get()` is het resultaat van de functie `map()` .

   1. De tweede parameter is de index van het element. In dit voorbeeld is de index `1` .

In dit voorbeeld wordt de volgende uitvoer gegenereerd:

![&#x200B; Output van de module van Jira &#x200B;](assets/output-from-jira-350x261.png)

>[!ENDSHADEBOX]

Voor meer informatie over de `map()` functie, zie [&#x200B; functies van de Serie &#x200B;](/help/workfront-fusion/references/mapping-panel/functions/array-functions.md).

Voor meer informatie over de `get()` functie, zie [&#x200B; Algemene functies &#x200B;](/help/workfront-fusion/references/mapping-panel/functions/general-functions.md).

## Arrayelementen omzetten in een reeks bundels

Arrays kunnen met de module [!UICONTROL Iterator] worden omgezet in een reeks bundels. Zie [[!UICONTROL Iterator] module &#x200B;](/help/workfront-fusion/references/modules/iterator-module.md) voor meer informatie.

![&#x200B; Reeks bundels &#x200B;](assets/series-of-bundles.png)
