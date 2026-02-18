---
title: Model Context Protocol (MCP)-modules
description: De module ModelContextProtocol (MCP) staat u toe om een gebruikersherinnering te verwerken gebruikend MCP.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 748055ad-d305-4513-9a5c-9c970b74a96e
source-git-commit: 5dfca593b17a234c80c807470026a7b192cbf7fa
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# ModelContextProtocol (MCP) module

<!--SET UP REDIRECTS-->

ModelContextProtocol (MCP) is een manier om AI taalmodellen met andere toepassingen veilig te verbinden. U vormt servers MCP, die het AI model toestaan om tot de toepassing toegang te hebben. Vervolgens kunt u een melding naar het AI-model sturen en gegevens van de toepassing terugsturen.

U kunt bijvoorbeeld een MCP-server configureren om een AI-model te verbinden met Gmail. Wanneer u de vraag &quot;Geef me mijn laatste 5 e-mails van Gmail,&quot;verzendt kan het tot uw Gmail toegang hebben en de e-mails terugkeren.

De module ModelContextProtocol (MCP) staat u toe om een gebruikersherinnering te verwerken gebruikend een taalmodel en servers MCP.

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





## De module van het Context Protocol van het model en zijn gebieden

Wanneer u de MCP module vormt, toont Adobe Workfront Fusion de hieronder vermelde gebieden. Een bolde titel in een module wijst op een vereist gebied.

### Prompt gebruiker verwerken

Deze actiemodule verwerkt een herinnering, gebruikend het taalmodel en servers MCP u specificeert.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>LLM-toets</td> 
   <td> Selecteer een bestaande sleutel LLM, of creeer nieuwe door <b> te klikken voeg </b> toe en ga de volgende informatie in: 
     <ul>
       <li><b> Zeer belangrijke naam </b>: Ga een naam voor de nieuwe sleutel in.</li>
       <li><b> LLM </b>: Selecteer het grote taalmodel dat deze sleutel met wordt geassocieerd.</li>
       <li><b> Sleutel </b>: Ga of kaart uw API sleutel voor het geselecteerde model in.</li>
       <li><b> Model </b>: Selecteer het model LLM dat de sleutel zal gebruiken.</li>
       <li><b> Max Tokens </b>: Ga of kaart het maximumaantal tokens in dat LLM in zijn reactie kan produceren.<p>Een token is meestal gelijk aan vier tekens, of 0,75 van een woord in het Engels. 'Hello world' zou twee tokens gelijk maken, en 'Authentication' zou één aan twee tokens gelijk stellen.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>MCP-servers</td> 
   <td> <p>Voor elke server MCP die u met wilt verbinden, <b> toevoegen </b> klikken en de volgende informatie ingaan: </p> 
     <ul>
       <li><b> Verbinding </b>: Selecteer de verbinding die de Fusie zal gebruiken om met de server te verbinden MCP.</li>
       <li><b> gastheer van de Server MCP </b>: Ga URL van de server MCP in.</li>
       <li><b> Naam van de Server MCP </b>: Ga of kaart een naam voor deze server MCP in.</li>
       <li><b> Kopballen </b>: Voeg om het even welke toepasselijke kopballen toe.</li>
       <li><b> Type van Server MCP </b>: Selecteer het servertype.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Uw vraag invoeren </td> 
   <td> <p>Ga of kaart de herinnering in die u wilt verwerken.</p> </td> 
  </tr> 
 </tbody> 
</table>


