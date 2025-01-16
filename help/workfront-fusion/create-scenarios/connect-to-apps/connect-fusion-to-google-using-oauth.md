---
title: Adobe Workfront Fusion met Google Services verbinden met behulp van een aangepaste OAuth-client
description: Met Adobe Workfront Fusion kunt u verbinding maken met Google Services via een aangepaste OAuth-client. Voor deze procedure is een bestaande Google-account vereist.
author: Becky
feature: Workfront Fusion
exl-id: 2f0bc289-4ecf-4a31-9d7b-641bbca6fc95
source-git-commit: 362952ec85b0df2306ba117ba530e95201330cca
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# Adobe Workfront Fusion met Google Services verbinden met behulp van een aangepaste OAuth-client

Met Adobe Workfront Fusion kunt u verbinding maken met Google Services via een aangepaste OAuth-client. Voor deze procedure is een bestaande Google-account vereist.

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
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
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

## Vereisten

U hebt een bestaande Google-account nodig om deze verbinding te maken.

## Connect Fusion to Google-services met een aangepaste OAuth-client

Als u deze verbinding wilt maken, moet u een project maken en configureren op het Google Cloud-platform en vervolgens de verbinding configureren in Fusion op basis van dat project.

>[!NOTE]
>
>Deze procedure is bedoeld voor:
>
>* Persoonlijk gebruik (`@gmail.com` en `@googlemail.com` gebruikers)
>* Intern gebruik (Google Workspace-gebruikers die liever een aangepaste OAuth-client gebruiken)

* [Een project maken op een Google Cloud-platform](#create-a-project-on-google-cloud-platform)
* [ vorm OAuth toestemmingsmontages ](#configure-oauth-consent-settings)
* [OAuth-referenties maken](#create-oauth-credentials)
* [Verbinding maken met Google in Workfront Fusion](#connect-to-google-in-workfront-fusion)

### Een project maken op een Google Cloud-platform

Een project maken op het Google Cloud-platform:

1. Beginnen met het maken van een project op het Google Cloud Platform.

   Voor instructies, zie [ tot een project van de Wolk van Google ](https://developers.google.com/workspace/guides/create-project) in de documentatie van de Gogle leiden.
1. Wanneer u API&#39;s inschakelt, moet u de Google Drive API en de API van alle Google-toepassingen die u wilt gebruiken (zoals de Google Sheets API) inschakelen.
1. Voltooi het maken van het project.
1. Ga aan de sectie [ verder vormen OAuth toestemmingsmontages ](#configure-oauth-consent-settings) in dit artikel.

### Instellingen voor OAuth-toestemming configureren

1. Beginnen met het configureren van OAuth voor uw project

   Voor instructies, zie [ het OAuth toestemmingsscherm vormen en werkingsgebied ](https://developers.google.com/workspace/guides/configure-oauth-consent) in de documentatie van Google kiezen.
1. Selecteer **Extern**, dan klik **creeer**.

   >[!NOTE]
   >
   >Er wordt geen bedrag in rekening gebracht wanneer u deze optie selecteert. Zie Google-informatie over uitzonderingen op verificatievereisten voor meer informatie.

1. Vul de vereiste velden als volgt in:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Toepassingsnaam</p> </td> 
      <td> <p>Voer de naam in van de toepassing die om toestemming vraagt.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b> Voorbeeld: </b></span></span> de Fusie van Adobe Workfront </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">E-mail met gebruikersondersteuning</td> 
      <td>Voer een e-mailadres in waarmee gebruikers contact met u kunnen opnemen als ze vragen hebben over hun toestemming wanneer ze verbinding maken met deze app.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">E-mailadressen</td> 
      <td>Voer een of meer e-mailadressen in die Google kan gebruiken om u op de hoogte te stellen van wijzigingen in uw project.</td> 
     </tr> 
    </tbody> 
   </table>

1. Onder Erkende domeinen, klik **voegt domein** toe, en gaat `workfrontfusion.com` in.
1. Voeg het volgende bereik toe:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Service/API</th> 
      <th>Vereist bereik</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td> <p>Gmail</p> </td> 
      <td> <p>https://mail.google.com/</p> <p>https://www.googleapis.com/auth/gmail.labels</p> <p>https://www.googleapis.com/auth/gmail.send</p> <p>https://www.googleapis.com/auth/gmail.readonly</p> <p>https://www.googleapis.com/auth/gmail.compose</p> <p>https://www.googleapis.com/auth/gmail.insert</p> <p>https://www.googleapis.com/auth/gmail.modify</p> <p>https://www.googleapis.com/auth/gmail.metadata</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Google Drive</p> </td> 
      <td> <p>https://www.googleapis.com/auth/drive</p> <p>https://www.googleapis.com/auth/drive.readonly</p> </td> 
     </tr> 
    </tbody> 
   </table>

   Mogelijk moet u de lijst uitvouwen of naar de volgende pagina in de lijst gaan om ze allemaal te kunnen zien.

1. (Optioneel) Voeg testgebruikers toe aan het project.
1. Onderzoek uw informatie voor nauwkeurigheid, dan klik **terug naar dashboard**.

   >[!NOTE]
   >
   >U hoeft het toestemmingsscherm en de aanvraag voor verificatie door Google niet in te dienen.

1. Ga aan [ creëren OAuth Credentials ](#create-oauth-credentials) verder.

### OAuth-referenties maken

1. Ga naar het maken van OAuth client ID-referenties.

   Voor instructies, zie [ toegangsgeloofsbrieven ](https://developers.google.com/workspace/guides/create-credentials) in de documentatie van Google creëren.

   >[!NOTE]
   >
   >Als dit niet de eerste API of service (Gmail of Google Drive) is die u hebt ingeschakeld, hoeft u geen nieuwe referenties te maken.

1. Vul de vereiste velden als volgt in:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Toepassingstype</td> 
      <td> <p> Webtoepassing</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Naam</td> 
      <td>Workfront Fusion </td> 
     </tr> 
    </tbody> 
   </table>

1. Onder Toegelaten opnieuw richt URIs, ga **één** van het volgende in:

   * Voor Gmail of Google Drive: `https://app.workfrontfusion.com/oauth/cb/google-restricted`

   * Voor andere Google-toepassingen: `https://app.workfrontfusion.com/oauth/cb/google`

1. Klik **creëren**.

   De weergave Client ID en Client Secret.

1. Kopieer de client-id en het clientgeheim naar een beveiligde locatie. U gebruikt ze om verbinding te maken met Workfront Fusion.
1. Ga verder [ met Google in de Fusie van Workfront ](#connect-to-google-in-workfront-fusion) verbinden.

### Verbinding maken met Google in Workfront Fusion

Het proces om een verbinding aan Google tot stand te brengen verschilt afhankelijk van of u een module van de dienst van Google (zoals Google Sheets of Google Docs) gebruikt, of als u met Google via HTTP >Make een OAuth2.0 verzoekmodule verbindt.

* [Verbinding maken met Google in een Google-service](#connect-to-google-in-a-google-service)
* [Verbinding maken met Google in de module HTTP > Een OAuth2.0-aanvraag maken](#connect-to-google-in-the-http--make-an-oauth20-request-module)

#### Verbinding maken met Google in een Google-service

1. Zoek in Workfront Fusion de Google-module waarvoor u een verbinding moet maken.
1. Klik **creeer een verbinding**, dan klik **tonen geavanceerde montages**.
1. Vul de velden Verbindingsnaam, Omgeving en Type naar wens in.
1. Ga identiteitskaart van de Cliënt in en Geheime cliënt u in [ wordt teruggewonnen creeert OAuth Credentials ](#create-oauth-credentials) op de respectieve gebieden, dan klik **verdergaan**.

1. Meld u aan met uw Google-account.

   **Deze app wordt niet geverifieerd** venstervertoningen. De app die in de venstertitel wordt vermeld, is de OAuth-client die u hierboven hebt gemaakt.

1. Klik **Geavanceerd**, dan klik **gaan naar de Fusie van Workfront (onveilig)** om toegang toe te staan gebruikend uw douaneOAuth cliënt.

1. Klik **toestaan** om de toestemming van de Fusie van Workfront te verlenen.
1. In het venster dat verschijnt, staat de klik **** opnieuw toe om uw keuzen te bevestigen.

   De verbinding met de gewenste Google-service met een aangepaste OAuth-client wordt tot stand gebracht.

#### Verbinding maken met Google in de module HTTP > Een OAuth2.0-aanvraag maken {#connect-to-google-in-the-http--make-an-oauth20-request-module}

Voor instructies bij het verbinden met Google in HTTP > maak een OAuth2.0 verzoekmodule, zie [ Instructies voor het creëren van een verbinding aan Google in HTTP > maak een OAuth 2.0 verzoekmodule ](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module) in het artikel HTTP > maak een OAuth 2.0 verzoekmodule.

## Mogelijke foutenmelding:[ 403 Toegang niet Gevormde ]

Als het foutbericht van `403 Access Not Configured` wordt weergegeven, moet u de bijbehorende API inschakelen in uw Google Cloud Platform. Om API toe te laten, volg de stappen in de sectie [ een project op het Platform van de Wolk van Google ](#create-a-project-on-google-cloud-platform) in dit artikel creëren.
