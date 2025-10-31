---
title: Een bestand toewijzen tussen modules
description: Sommige modules kunnen bestanden verwerken. Deze modules kunnen een uitvoerbestand retourneren dat voor verdere verwerking moet worden verzonden of een bestand vereisen dat voor verwerking aan hen wordt doorgegeven. Voordat deze modules kunnen samenwerken om bestanden te verwerken, moeten ze aan elkaar worden toegewezen.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Een bestand toewijzen tussen modules

Sommige modules kunnen bestanden verwerken. Deze modules kunnen een uitvoerbestand retourneren dat voor verdere verwerking moet worden verzonden, of een bestand vereisen dat voor verwerking aan hen wordt doorgegeven. Bestanden kunnen me worden toegewezen, zodat een bestandsuitvoer door de ene module kan worden verwerkt door een andere module.

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

## Bestanden van bronmodules toewijzen aan doelmodules

De modules kunnen dossiers verwerken vereisen twee stukken van informatie:

* Bestandsnaam
* Bestandsinhoud (gegevens)

Als om het even welke vorige modules een dossier uitvoeren, kunt u de bronmodule selecteren, en de naam en de gegevens van de dossieroutput door die module worden in kaart gebracht aan de doelmodule.

U kunt deze naam en gegevens ook handmatig invoeren of toewijzen vanuit vorige modules. Dit kan handig zijn wanneer u bijvoorbeeld de naam van een bestand wijzigt.

>[!NOTE]
>
>Als u een bestand vanaf een URL moet verwerken, raden we u aan het bestand met de module `HTTP > Get a File` te downloaden van de URL en het bestand vervolgens van de module `HTTP > Get a File` toe te wijzen aan het veld van de gewenste module in uw scenario.
>
>![&#x200B; dossier van de Kaart &#x200B;](assets/map-source-file.png)

Een bestand toewijzen:

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waarin u een bestand wilt toewijzen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. In de doelmodule, die het doel is u aan in kaart brengt, bepaal de plaats van het **dossier van Source** gebied.
1. Als u een bestandsuitvoer wilt toewijzen door een vorige module, selecteert u de module die het bestand uitvoert.

   ![&#x200B; Workfront downloaddocument &#x200B;](assets/wf-download-document.png)

1. Als u de naam en gegevens handmatig wilt toewijzen, selecteert u Kaart en voert u de naam en gegevens van het bestand in of wijst u deze toe.

   ![&#x200B; Gebruik de kaartoptie &#x200B;](assets/use-the-map-option.png)

1. Ga verder vormend de module, of klik **O.K.**.
