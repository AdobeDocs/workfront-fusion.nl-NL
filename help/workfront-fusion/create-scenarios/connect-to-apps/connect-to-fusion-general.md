---
title: Verbinding maken - Basisinstructies
description: Vele  [!DNL Adobe Workfront Fusion]  schakelaars vereisen geen douaneconfiguratie wanneer het creëren van een verbinding. In dit artikel wordt het standaardproces voor het maken van verbindingen beschreven.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: 6aec65919e79a9e9d950a11de53bfbb1051ca20b
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Verbinding maken - Basisinstructies

Veel [!DNL Adobe Workfront Fusion] -connectors vereisen geen aangepaste configuratie wanneer u een verbinding maakt. In dit artikel wordt het standaardproces voor het maken van verbindingen beschreven.

>[!NOTE]
>
>
>Als Adobe Workfront Fusion geen app aanbiedt voor de webservice die u in uw scenario wilt gebruiken, kunt u verbinding maken met de webservice via de modules [!DNL Workfront Fusion] HTTP en Webhooks, zoals in de volgende artikelen wordt uitgelegd:
>
>* [ verbind de Fusie van Adobe Workfront met de Webdienst die API tokenvergunning gebruikt ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [ vorm een webhaak voor een Webdienst zonder een schakelaar ](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket 
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
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Selecteer of Prime Workfront Plan: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultimate Workfront Plan: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Verbinding maken

Als u een verbinding met een bepaalde toepassing wilt maken, moet u zich in een module voor die toepassing bevinden. Als u bijvoorbeeld een verbinding met Workfront wilt maken, moet u zich in een Workfront-module bevinden.

Een verbinding maken binnen een module [!DNL Workfront Fusion] :

1. Klik in een willekeurige module voor de opgegeven toepassing op **[!UICONTROL Add]** naast het vak [!UICONTROL Connection] om het deelvenster **[!UICONTROL Create a connection]** te openen.
1. (Optioneel) Wijzig de standaardinstelling **[!UICONTROL Connection name]** .
1. Selecteer op het gebied van milieu of dit een productie- of niet-productieomgeving is.
1. Selecteer in het veld Type of dit een service of een persoonlijke account is.
1. (Voorwaardelijk) Als de toepassing geavanceerde verbindingsinstellingen nodig heeft, zoals een id, sleutel of [!UICONTROL secret] , voert u die gegevens in.

   U moet mogelijk op **[!UICONTROL Show advanced settings]** klikken om de velden weer te geven waarin u dit soort informatie kunt invoeren.

1. Klik op **[!UICONTROL Continue]**.
1. Voer in het aanmeldingsvenster dat wordt weergegeven uw aanmeldingsgegevens in om u aan te melden bij de app als u dat nog niet hebt gedaan.
1. (Voorwaardelijk) Als een knop **[!UICONTROL Allow]** wordt weergegeven, controleert u de handelingen die de aansluiting kan uitvoeren en klikt u op de knop om de app aan te sluiten op [!DNL Workfront Fusion] .

   >[!NOTE]
   >
   >* De velden Omgeving en Type dienen alleen ter informatie en hebben geen invloed op de functionaliteit van de verbinding. Deze informatie wordt weergegeven in het gebied Verbindingen van Fusion, zodat u kunt bepalen welke verbinding voor een bepaald gebruiksgeval in uw organisatie moet worden gebruikt.
   >* Sommige Microsoft-toepassingen gebruiken dezelfde verbinding, die is gekoppeld aan individuele gebruikersmachtigingen. Daarom bij het creëren van een verbinding, toont het scherm van de toestemmingstoestemming om het even welke toestemmingen die eerder aan de verbinding van deze gebruiker werden verleend, naast om het even welke nieuwe toestemmingen nodig voor de huidige toepassing.
   >
   >   Bijvoorbeeld, als een gebruiker &quot;Gelezen lijst&quot;toestemmingen heeft die via de schakelaar van Excel worden verleend en dan een verbinding in de schakelaar van Vooruitzichten creeert om e-mails te lezen, zal het scherm van de toestemmingstoestemming zowel de reeds verleende &quot;Gelezen lijst&quot;toestemming en de onlangs vereiste &quot;Schrijf e-mail&quot;toestemming tonen.
