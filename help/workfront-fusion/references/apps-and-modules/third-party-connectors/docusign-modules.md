---
title: DocuSign-modules
description: De  [!DNL Adobe Workfront Fusion DocuSign]  modules laten u toe om envelopstatus te controleren en terug te winnen, enveloppen te zoeken en terug te winnen, of een document te downloaden en te verzenden om in uw  [!DNL DocuSign]  rekening te ondertekenen.
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 0%

---

# DocuSign-modules

Met de Adobe Workfront Fusion [!DNL DocuSign] -modules kunt u de envelopstatus controleren en ophalen, enveloppen zoeken en ophalen, of een document downloaden en verzenden om u aan te melden bij uw [!DNL DocuSign] -account.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Connectorgebaseerde (verouderde): Workfront Fusion for Work Automation and Integration </p>
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

## Vereisten

Als u [!DNL DocuSign] -modules wilt gebruiken, moet u een [!DNL DocuSign] -account hebben.

## DocuSign API-informatie

De DocuSign-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL DocuSign] met Workfront Fusion {#connect-docusign-to-workfront-fusion}

Verbinding maken voor uw [!DNL DocuSign] -modules:

1. Klik op **[!UICONTROL Add]** naast het vak [!UICONTROL Connection] wanneer u de eerste module van [!DNL DocuSign] gaat configureren.
1. Voer het volgende in:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Voer een naam in voor de nieuwe [!DNL DocuSign] verbinding.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td>Selecteer of u verbinding maakt met een productie in een niet-productieomgeving.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>Geef op of de account waarmee u verbinding wilt maken, een productieaccount of een demo-account is.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik **verdergaan** om de verbinding te bewaren en aan de module terug te keren.

## [!DNL DocuSign] modules en hun velden

Wanneer u [!DNL DocuSign] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL DocuSign] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)

### Triggers

#### [!UICONTROL Watch envelopes]

Deze triggermodule start een scenario wanneer een omhulsel wordt verzonden, geleverd, ondertekend, voltooid of afgewezen.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL DocuSign] rekening aan Workfront Fusion, zie <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref"> Connect Document aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecteer de account die de records bevat die u wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p> Selecteer het type gebeurtenis dat u wilt controleren.</p> 
    <ul> 
     <li>[!UICONTROL Document completed]</li> 
     <li>[!UICONTROL Document declined]</li> 
     <li>[!UICONTROL Document sent]</li> 
     <li>[!UICONTROL Document signed]</li> 
     <li>[!UICONTROL New document in Inbox]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Outputs]</p> </td> 
   <td> <p>Selecteer de velden die u wilt opnemen in de uitvoer van de module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module wilt werken met tijdens elke cyclus van de scenariouitvoering.</td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Add a custom field]](#add-a-custom-field)
* [[!UICONTROL Add Recipient to Envelope]](#add-recipient-to-envelope)
* [[!UICONTROL Create a new envelope]](#create-a-new-envelope)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download a document]](#download-a-document)
* [[!UICONTROL Modify custom field]](#modify-custom-field)
* [[!UICONTROL Read an envelope]](#read-an-envelope)
* [[!UICONTROL Send envelope]](#send-envelope)
* [[!UICONTROL Upload a file to an envelope]](#upload-a-file-to-an-envelope)

#### [!UICONTROL Add a custom field]

Deze actiemodule voegt een aangepast veld toe aan het document

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL DocuSign] rekening aan Workfront Fusion, zie <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL DocuSign] met Workfront Fusion </a> in dit artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecteer de account die het document bevat waaraan u een aangepast veld wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Voer de id in van de envelop die het document bevat waar u een aangepast veld wilt toevoegen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Typ of wijs een naam toe voor het nieuwe veld dat u wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Schakel deze optie in als u wilt dat het toegevoegde veld een verplicht veld is.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Schakel deze optie in als u wilt dat het veld zichtbaar is.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Voer de waarde (inhoud) van het toegevoegde veld in of wijs deze toe. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Recipient to Envelope]

Deze actiemodule voegt één of meerdere ontvangers aan een bestaande envelop toe. Als de envelop al is verzonden, wordt de ontvanger een e-mail verzonden. Deze module is niet geldig voor enveloppen die reeds zijn voltooid.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Voor instructies over het aansluiten van uw rekening DocuSign aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Account] </td>
   <td> <p>Selecteer de account die de envelop bevat waar u ontvangers wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>Selecteer of kaart identiteitskaart van de envelop waar u de ontvanger wilt toevoegen.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Recipient type]</td>
   <td> <p> Selecteer het type ontvanger dat u aan de envelop wilt toevoegen.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon copy]</p> </li> 
     <li> <p>[!UICONTROL Certified delivery]</p> </li> 
     <li> <p>[!UICONTROL In-person signer]</p> </li> 
     <li> <p>[!UICONTROL Intermediary]</p> </li> 
     <li> <p>[!UICONTROL Signer]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>Voer het e-mailadres in of wijs het e-mailadres toe van de ontvanger die u aan de envelop wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Name]</td>
   <td>Voer de naam in of wijs de naam toe van de ontvanger die u aan de envelop wilt toevoegen.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Routing order]</td>
   <td> <p>Ga of kaart het verpletterende aantal voor de ontvanger in. Het verpletteren van aantal bepaalt de orde waarin de ontvangers uw documenten ontvangen en ondertekenen.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Email body]</td>
   <td>Voer de hoofdtekst (inhoud) van de e-mail die naar de ontvanger is verzonden in of wijs deze toe.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Email subject]</td>
   <td>Voer het onderwerp in van de e-mail die naar de ontvanger is verzonden of wijs het onderwerp ervan toe.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private message]</td>
   <td> Als u een privébericht naar de ontvanger wilt verzenden, voert u de tekst van het bericht in of wijst u deze toe. <p>Alleen de geselecteerde ontvanger ziet het privébericht en het algemene bericht. Het privébericht mag maximaal 1000 tekens bevatten.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Authentication]</td> 
   <td> <p>Selecteer de authentificatiemethode die u wilt gebruiken om de identiteit van de ontvanger te bevestigen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL None]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Access code]</strong> </p> <p>Voer de toegangscode in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>Ga of kaart het telefoonaantal in.</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>Ga of kaart het telefoonaantal in.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a new envelope]

Deze actiemodule leidt tot een nieuw omhulsel van een malplaatje. De id van de nieuwe envelop wordt geretourneerd, evenals de status van de nieuwe envelop.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td>

<td> <p>Voor instructies over het aansluiten van uw rekening DocuSign aan de Fusie van Workfront, zie de artikelen onder <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Account] </td>
   <td> <p>Selecteer de account die de envelop bevat waar u een bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template]</td>
   <td> <p> Selecteer de sjabloon waarvan u de nieuwe envelop wilt maken. Sjablonen zijn beschikbaar op basis van de geselecteerde [!UICONTROL Account] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL After creation]
   </td> 
   <td> <p>Selecteer of u de envelop wilt opslaan als een concept of deze voor ondertekening wilt verzenden.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template recipients]</td>
    <td>Voor elke ontvanger die u aan deze envelop wilt toevoegen, <b> klikt toevoegt punt </b> en gaat de volgende details in:
    <ul>
    <li><b>Toegangscode</b><p>Ga of kaart de code in die de ontvanger gebruikt om tot de envelop toegang te hebben.<p></li>
    <li><b>E-mail</b><p>Voer het e-mailadres van de ontvanger in of wijs dit toe.<p></li>
    <li><b>Naam</b><p>Voer de naam van de ontvanger in of wijs deze toe.<p></li>
    <li><b>Rolnaam</b><p>Voer de rolnaam van de ontvanger in of wijs deze toe.<p></li>
    <li><b>Routeringsvolgorde</b><p>Ga of kaart het verpletterende aantal voor de ontvanger in. Het verpletteren van aantal bepaalt de orde waarin de ontvangers uw documenten ontvangen en ondertekenen.<p></li>
    </ul>
    </td>
    </tr>
  <tr> 
   <td role="rowheader">
     [!UICONTROL Allow Print and Sign]
   </td> 
   <td> <p>Schakel deze optie in als de ontvanger het document mag afdrukken en het papier mag ondertekenen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Allow Reassign]
   </td> 
   <td> <p>Schakel deze optie in als u wilt dat de ontvanger de documenten opnieuw aan een andere gebruiker kan toewijzen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Allow Recipient Recursion]
   </td> 
   <td> <p>Schakel deze optie in als u herhaling door ontvangers wilt toestaan.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Authoritative copy]
   </td> 
   <td> <p>Schakel deze optie in om de documenten in deze envelop te markeren als gezaghebbende kopieën.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Auto Navigation]
   </td> 
   <td> <p>Schakel deze optie in om automatische navigatie voor de ontvanger in te stellen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Brand ID]
   </td> 
   <td> <p>Voer de id van het merk in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Markup Enabled]
   </td> 
   <td> <p>Schakel deze optie in om Documentmarkeringen in te schakelen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Expire Enabled]
   </td> 
   <td> <p>Schakel deze optie in om een vervaldatum voor deze envelop in te stellen. Als u deze optie inschakelt, vult u de volgende velden in:<ul><li><b>Verlopen na</b><p>Voer het aantal dagen in waarna deze envelop vervalt of wijs het aantal dagen toe.</p></li><li><b>Waarschuwing bij verlopen</b><p>Voer het aantal dagen voor het verlopen van de e-mail voor een herinnering in of wijs dit aantal toe aan de ontvanger.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Body]
   </td> 
   <td> <p>Voer de tekst (inhoud) in van de e-mail die bij deze envelop is gevoegd of wijs deze envelop toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL Subject]
   </td> 
   <td> <p>Voer het onderwerp in van de e-mail die bij deze envelop is gevoegd of wijs het onderwerp ervan toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste API-aanroep uitvoeren.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL DocuSign] rekening aan Workfront Fusion, zie <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL DocuSign] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Account]</td> 
   <td>Voer de account in of wijs de account toe die u wilt gebruiken om toegang te krijgen tot de [!DNL DocuSign] API.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Een pad invoeren of toewijzen ten opzichte van <code>https://&lt;BASE_URI>/v2/accounts/&lt;ACCOUNT_ID>.</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object. Dit bepaalt het inhoudstype van het verzoek.</p> <p>Bijvoorbeeld:<code> {"Content-type":"application/json"}</code></p> <p>Opmerking: als u fouten krijgt en het moeilijk is om de oorsprong ervan te bepalen, kunt u overwegen koppen te wijzigen op basis van de documentatie van Workfront. Als uw Aangepaste API-aanroep een HTTP-aanvraagfout van 422 retourneert, probeert u een header "Content-Type":"text/plain".</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Voer het maximale aantal resultaten in waarmee u tijdens één uitvoeringscyclus wilt werken of wijs het maximumaantal resultaten toe.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Voorbeeld:** Omhulsels van de Lijst

De volgende API-aanroep retourneert enveloppen vanaf de opgegeven datum in uw [!DNL DocuSign] -account:

**URL**: `/v2.1/accounts/{accountId}/envelopes/`

**Methode**: `GET`

**Koord van de Vraag**:

* **Sleutel**: `from_date`

* **Waarde**: `YYYY-MM-DD`

Hiermee geeft u aan wanneer de aanvraag begint te controleren op statuswijzigingen voor enveloppen in de account.

![ Opstelling van het Document van het Voorbeeld ](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)

Het resultaat is te vinden in de Uitvoer van de module onder Bundel > Body > Omhulsels.

In ons voorbeeld werden 6 enveloppen geretourneerd:

![ Voorbeeld documenteert output ](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

>[!ENDSHADEBOX]

#### [!UICONTROL Download a document]

Deze actiemodule downloadt één document.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL DocuSign] rekening aan Workfront Fusion, zie <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL DocuSign] met Workfront Fusion </a> in dit artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecteer de account die het document bevat dat u wilt downloaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Voer de id in van de envelop die u wilt downloaden of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Document ID]</p> </td> 
   <td> <p>Voer de id in van het document dat u wilt downloaden of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Certificate]</td> 
   <td>Schakel deze optie in om het envelopondertekeningscertificaat op te nemen in de download.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents by User ID]</td> 
   <td>Schakel deze optie in als u wilt dat ontvangers documenten kunnen ophalen aan de hand van de gebruikersnaam. Bijvoorbeeld, als een gebruiker in twee verschillende verpletterende orden met verschillende visibilities inbegrepen is, die deze optie gebruikt keert alle documenten van beide routings terug.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encrypt]</td> 
   <td>Schakel deze optie in als u wilt dat de PDF-bytes die in de reactie worden geretourneerd, worden gecodeerd voor alle sleutelbeheerders die op uw [!DNL DocuSign] -account zijn geconfigureerd.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Selecteer de taal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Changes]</td> 
   <td>Schakel deze optie in om gewijzigde velden voor de geretourneerde PDF te markeren in geel en om optionele handtekeningen of initialen in rood te omtrekken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watermark]</td> 
   <td> <p>Schakel deze optie in om de functie Watermerk in te schakelen. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify custom field]

Deze actiemodule wijzigt een aangepast veld met de veldnaam.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL DocuSign] rekening aan Workfront Fusion, zie <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL DocuSign] met Workfront Fusion </a> in dit artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecteer de account die het document bevat waarin u een aangepast veld wilt wijzigen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Voer de id in van de envelop die het document bevat waar u een aangepast veld wilt wijzigen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field ID]</td> 
   <td>Voer de id in van het veld dat u wilt wijzigen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Typ of wijs de naam van het veld toe dat u wilt wijzigen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Schakel deze optie in als u wilt dat het gewijzigde veld een verplicht veld is.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Schakel deze optie in als u wilt dat het veld zichtbaar is.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Voer de waarde (inhoud) van het gewijzigde veld in of wijs deze toe. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read an envelope]

Deze actiemodule leest informatie over een omhulsel in [!DNL DocuSign] met behulp van de omhulings-id.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL DocuSign] rekening aan Workfront Fusion, zie <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL DocuSign] met Workfront Fusion </a> in dit artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecteer de account die het document bevat waarvan u gegevens wilt lezen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Voer de id in van de envelop die het document bevat waarvan u gegevens wilt lezen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer van de module wilt weergeven. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send envelope]

Deze actiemodule verzendt een ontwerp envelop naar zijn ontvangers.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL DocuSign] rekening aan Workfront Fusion, zie <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL DocuSign] met Workfront Fusion </a> in dit artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecteer de account die de conceptenvelop bevat die u naar de ontvangers wilt verzenden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Voer de id in van de conceptenvelop die u naar de ontvangers wilt verzenden of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file to an envelope]

Deze module uploadt een gespecificeerd dossier aan een bestaande envelop in DocuSign.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL DocuSign] rekening aan Workfront Fusion, zie <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL DocuSign] met Workfront Fusion </a> in dit artikel.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Selecteer de account die de envelop bevat waar u een bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Voer de id van de envelop in of wijs deze toe waar u een bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecteer een bronbestand uit een vorige module of voer de naam en gegevens van het bronbestand in.</td> 
  </tr> 
 </tbody> 
</table>
