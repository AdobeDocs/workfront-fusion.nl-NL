---
title: JSONata-modules
description: De Adobe Workfront Fusion JSONata-connector biedt een module voor het verwerken van gegevens in JSON-indeling, zodat Adobe Workfront Fusion verder kan werken met de gegevensinhoud.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# [!UICONTROL JSONata] modules

Met de Adobe Workfront Fusion [!UICONTROL JSONata] -connector kunt u JSON-objecten opvragen. Voor deze module is geen verbinding vereist.

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
