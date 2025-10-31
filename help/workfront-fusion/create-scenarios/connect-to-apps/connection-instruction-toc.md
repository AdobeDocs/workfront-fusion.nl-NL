---
title: Verbindingen maken
description: Een verbinding moet voldoen aan de vereisten die zijn ingesteld door de API van de app of webservice waarmee de verbinding wordt gemaakt. Daarom zijn de instructies voor het instellen van een verbinding afhankelijk van de app of webservice. Dit artikel kan u helpen bij het identificeren en zoeken van de instructies voor het verbinden van Adobe Workfront Fusion met uw gekozen app of webservice.
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---

# Verbindingen maken

Een verbinding moet voldoen aan de vereisten die zijn ingesteld door de API van de app of webservice waarmee de verbinding wordt gemaakt. Daarom zijn de instructies voor het instellen van een verbinding afhankelijk van de app of webservice. Dit artikel kan u helpen bij het identificeren en zoeken van de instructies voor het verbinden van Adobe Workfront Fusion met uw gekozen app of webservice.

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
   <td role="rowheader">Adobe Workfront Fusion-licentie</td> 
   <td>
   <p>Exploitatie gebaseerd: geen Workfront Fusion-licentievereisten</p>
   <p>Connectorgebaseerde (verouderde): als u verbinding wilt maken met toepassingen buiten de Workfront-productreeks, hebt u Workfront Fusion for Work Automation and Integration nodig </p>
   </td> 
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

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Verbinding maken met een app of webservice waarvoor geen configuratie is vereist

In de meeste gevallen kunt u de module gebruiken om een verbinding te maken met weinig of geen extra informatie. Workfront Fusion handelt de verificatie automatisch af.

Voor instructies bij het creëren van een verbinding zonder speciale overwegingen, zie [ een verbinding creëren - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

## Verbinding maken met een Adobe-app of -service

Als u verbinding wilt maken met een Adobe-app of -service, hebt u mogelijk informatie van de Adobe Admin Console nodig, zoals uw organisatie-id of technische account-id.

U kunt de Adobe Authenticator-module ook gebruiken om verbinding te maken met elke Adobe API via één verbinding. Hierdoor kunt u gemakkelijker verbinding maken met Adobe-producten die nog geen speciale Fusion-connector hebben.

Voor specifieke instructies, zie [ het artikel voor de schakelaar ](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products).

## Verbinding maken met een [!DNL Microsoft] -app of -webservice

Met de meeste [!DNL Microsoft] -toepassingen in Workfront Fusion kunt u zonder extra informatie een verbinding maken.

De volgende omstandigheden vereisen extra stappen bij het maken van een verbinding:

* Microsoft Dynamics 365-modules gebruiken.

  Voor instructies, zie [ Microsoft Dynamics 365 modules ](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).

* Verbinding maken met de Microsoft Graph API via een HTTP-module

  Voor instructies, zie [ Vraag de REST API van de Grafiek van MS ](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).

## Verbinding maken met een [!DNL Google] -app of -webservice

Het proces voor het maken van verbinding met [!DNL Google] -apps kan afwijken, afhankelijk van het type [!DNL Google] -account dat u gebruikt. Bovendien kunnen beveiligingsmaatregelen van [!DNL Google] extra configuratie vereisen wanneer u verbinding maakt met Workfront Fusion.

Zie voor meer informatie:

* [Adobe Workfront Fusion met Google Services verbinden met behulp van een aangepaste OAuth-client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [Connect Adobe Workfront Fusion voor Google Services met bijgewerkte beveiligingsmaatregelen](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## Andere toepassingen waarvoor aanvullende configuratie vereist is

Sommige apps en services volgen de basisconfiguratie voor Workfront Fusion-verbindingen niet. U vindt instructies voor het verbinden van deze apps in het artikel voor die app.

Voor specifieke instructies, zie [ het artikel voor de schakelaar ](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications).
