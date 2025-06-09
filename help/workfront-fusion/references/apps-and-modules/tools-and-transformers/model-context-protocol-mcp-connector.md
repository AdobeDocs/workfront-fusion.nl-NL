---
title: Model Context Protocol (MCP)-modules
description: De module ModelContextProtocol (MCP) staat u toe om een gebruikersherinnering te verwerken gebruikend MCP.
author: Becky
feature: Workfront Fusion
source-git-commit: d8ae176db714d2b9f041b74a62e8276171745c4b
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Model Context Protocol (MCP)-modules

ModelContextProtocol (MCP) is een manier om AI taalmodellen met andere toepassingen veilig te verbinden. U vormt servers MCP, die het AI model toestaan om tot de toepassing toegang te hebben. Vervolgens kunt u een melding naar het AI-model sturen en gegevens van de toepassing terugsturen.

U kunt bijvoorbeeld een MCP-server configureren om een AI-model te verbinden met Gmail. Wanneer u de vraag &quot;Geef me mijn laatste 5 e-mails van Gmail,&quot;verzendt kan het tot uw Gmail toegang hebben en de e-mails terugkeren.

De module ModelContextProtocol (MCP) staat u toe om een gebruikersherinnering te verwerken gebruikend een taalmodel en servers MCP.

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
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten</p>
   <p>of</p>
   <p>Verouderd: Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Select- of Prime Workfront-pakket: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultimate Workfront-pakket: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## De module van het Context Protocol van het model en zijn gebieden

Wanneer u de MCP module vormt, [!DNL Adobe Workfront Fusion] toont de hieronder vermelde gebieden. Een bolde titel in een module wijst op een vereist gebied.

### Prompt gebruiker verwerken

Deze actiemodule verwerkt een herinnering, gebruikend het taalmodel en servers MCP u specificeert.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Large language model (LLM) key]</td> 
   <td> <p>Ga of kaart API sleutel voor het grote taalmodel in u voor deze herinnering wilt gebruiken. </p> <p>Momenteel wordt alleen de Anthropic API-sleutel ondersteund.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MCP servers]</td> 
   <td> <p>Voor elke server MCP die u voor deze herinnering beschikbaar wilt maken, <b> klik toevoegen punt </b> en ga de naam en de gastheer van de server in. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter your prompt]</td> 
   <td> <p>Voer de vraag voor het grote taalmodel in of wijs deze toe. </p> </td> 
  </tr> 
 </tbody> 
</table>
