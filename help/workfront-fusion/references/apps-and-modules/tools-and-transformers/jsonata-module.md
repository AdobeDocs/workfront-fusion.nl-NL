---
title: JSONata-modules
description: De Adobe Workfront Fusion JSONata-connector biedt een module voor het verwerken van gegevens in JSON-indeling, zodat Adobe Workfront Fusion verder kan werken met de gegevensinhoud.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# [!UICONTROL JSONata] modules

Met de Adobe Workfront Fusion [!UICONTROL JSONata] -connector kunt u JSON-objecten opvragen. Voor deze module is geen verbinding vereist.

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

## JSONata-modules en hun velden

### Evalueren

Deze actiemodule zoekt een JSON-object en retourneert een array.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expression]</td> 
   <td>Voer de expressie in die u wilt gebruiken om het JSON-object te evalueren. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data] </td> 
   <td> Voer het JSON-object in dat u wilt evalueren.  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringify output] </td> 
   <td> Schakel deze optie in om uitvoer om te zetten in een tekenreeks.  </td> 
  </tr> 
  </tbody>
  </table>

>[!BEGINSHADEBOX]

**Voorbeeld**:

Het doel is een array met namen van het volgende JSON-object te retourneren:

```JSON
{
  "people": [
    { "name": "Alice", "age": 30 },
    { "name": "Bob", "age": 25 },
    { "name": "Charlie", "age": 35 }
  ]
}
```

1. Typ `people.name` in het veld Expressie.
1. Voer in het gegevensveld het JSON-object in.

De module retourneert een array met namen die uit het JSON-object zijn opgehaald.

>[!ENDSHADEBOX]



### JSONata MCP

Deze actiemodule genereert JSONata-expressies door de opgegeven in- en uitvoerschema&#39;s te analyseren. U verstrekt de schema&#39;s, welke ModelContextProtocol (MCP) gebruikt om de uitdrukking te produceren die de input in de output transformeert.




<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Selecteer de verbinding die u gebruikt om met het grote taalmodel (LLM) te verbinden dat u voor deze module wilt gebruiken.</p> <p>Momenteel wordt alleen de Anthropic API-sleutel ondersteund.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input schema]</td> 
   <td> <p>Voer het invoerschema dat voor deze expressie moet worden gebruikt in of wijs dit toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output schema]</td> 
   <td> <p>Voer het uitvoerschema dat u voor deze expressie wilt gebruiken in of wijs dit toe.</p> </td> 
  </tr> 
 </tbody> 
</table>
