---
title: De MS Graph REST API aanroepen
description: Roep de MS Graph REST API aan via de Adobe Workfront Fusion HTTP &> Een OAuth 2.0-aanvraagmodule maken
author: Becky
feature: Workfront Fusion
exl-id: f411c807-955d-44fe-98b1-3ebba3fe0861
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 1%

---

# De MS Graph REST API aanroepen

Veel Microsoft-webservices zijn toegankelijk via de Microsoft Graph API. U kunt een verbinding met de Microsoft Graph API tot stand brengen, door Workfront Fusion HTTP > Make an OAuth 2.0 request module te gebruiken.

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

## Workfront Fusion registreren in de Microsoft Application Registration Portal

Als u een verbinding met de Microsoft Graph REST API wilt maken, moet u eerst Adobe Workfront Fusion registreren.

1. Begin registrerend een nieuwe toepassing zoals die in [ wordt beschreven Register een toepassing met het de identiteitsplatform van Microsoft ](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) in de documentatie van Microsoft.

   Als onderdeel van de registratie vereist Microsoft de volgende informatie:

   <table style="table-layout:auto">
      <tr>
        <td>Toepassingsnaam</td>
        <td>Voer een naam voor de toepassing in, bijvoorbeeld "Mijn Workfront Fusion-toepassing".</td>
      </tr>
      <tr>
        <td>URL omleiden</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/oauth2</code></td>
      </tr>
    </table>

1. Noteer de toepassings-id wanneer u de registratie van de app hebt voltooid.

   >[!IMPORTANT]
   >
   >U hebt de toepassings-id nodig om uw verbinding in Workfront Fusion in te stellen.

1. Een clientgeheim genereren. Noteer dit geheim.

   Voor instructies, zie [ een toepassing met het de identiteitsplatform van Microsoft ](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) in de documentatie van Microsoft registreren.

   >[!IMPORTANT]
   >
   >U hebt clientgeheim nodig om uw verbinding in Workfront Fusion in te stellen.

1. Configureer de machtigingen voor uw toepassing.

   Voor details bij het bepalen van en het vormen van deze gebieden, zie de &quot;toestemmingen voor de Grafiek van Microsoft&quot;sectie in [ toegang zonder een gebruiker ](https://docs.microsoft.com/en-us/graph/auth-v2-service) in de documentatie van Microsoft krijgen.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Welk type machtigingen vereist uw toepassing?</td> 
      <td>Selecteer <code>Delegated permissions</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Machtigingen selecteren</td> 
      <td> <p>Selecteer de volgende machtigingen:</p> 
       <ul> 
        <li> <p><code>offline_access</code> </p> </li> 
        <li> <p><code>openid</code> </p> </li> 
        <li> <p>Eventuele andere machtigingen die vereist zijn voor uw integratie (bijvoorbeeld: <code>User.Read</code>)</p> </li> 
       </ul> <p><b> Belangrijk </b>: U zult de geselecteerde toestemmingen aan opstelling uw verbinding in de Fusie van Workfront nodig hebben.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Ga aan [ verder vormen uw de Grafiek API verbinding van MS in de Fusie van Workfront ](#configure-your-ms-graph-api-connection-in-workfront-fusion).

## Uw MS Graph API-verbinding configureren in Workfront Fusion

Nadat u de Fusie van Workfront zoals die in [ wordt besproken registreert de Fusie van Workfront in het Portaal van de Registratie van de Toepassing van Microsoft ](#register-workfront-fusion-in-the-microsoft-application-registration-portal), kunt u uw verbinding in HTTP vormen > maak een Oauth 2.0 verzoekmodule.

1. Voeg HTTP > een OAuth 2.0 vraagmodule aan uw scenario toe.
1. Klik **toevoegen** naast het verbindingsgebied.
1. Configureer de verbindingsvelden als volgt:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Verbindingsnaam</td> 
      <td>Voer een naam in voor de verbinding.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Omgeving</p> </td> 
      <td>Selecteer of u verbinding maakt met een productie- of niet-productieaccount. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Type</p> </td> 
      <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Stroomtype</p> </td> 
      <td>Selecteer <code>Authorization Code</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">URI toestaan</td> 
      <td>Voer <code>https://login.microsoftonline.com/common/oauth2/v2.0/authorize</code> in. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Token-URI</td> 
      <td>Voer <code>https://login.microsoftonline.com/common/oauth2/v2.0/token</code> in. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Toepassingsgebied</td> 
      <td> <p>Ga de toestemmingen in die u binnen wanneer het registreren selecteerde, zoals die in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref"> worden besproken de Fusie van het Register Workfront in het Portaal van de Registratie van de Toepassing van Microsoft </a>.</p> <p>Voor elk werkingsgebied, klik <b> toevoegen </b> en type in de toestemming.</p> <p>Voorbeeld: <code>offline_access</code> .</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Scheidingsteken bereik</td> 
      <td>Selecteer <code>SPACE</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Client-id</td> 
      <td>Ga identiteitskaart van de Toepassing van stap 2 in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref"> Workfront Fusion van het Register in het Portaal van de Registratie van de Toepassing van Microsoft </a> in.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Clientgeheim</td> 
      <td>Ga het Geheim van de Cliënt in dat u in stap 3 in <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref"> Workfront Fusion van het Register in het Portaal van de Registratie van de Toepassing van Microsoft </a> produceerde.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Parameters toestaan</td> 
      <td> <p>Voeg de volgende machtigingsparameters toe. Voor elke parameter u toevoegt, <b> klikt toevoegt punt </b> en gaat het volgende in: </p> 
       <ul> 
        <li> <p>Sleutel:<code> response_mode</code> Waarde: <code>query</code></p> </li> 
        <li> <p>Sleutel: <code>prompt </code> Waarde: <code>consent</code></p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Toegang krijgen tot token-parameters</td> 
      <td>U hoeft niets in dit veld in te voeren.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Tokenparameters vernieuwen</td> 
      <td> 
       <ol> 
        <li value="1"> <p>Klik <b> toevoegen punt </b>.</p> </li> 
        <li value="2"> <p>Op het <b> Zeer belangrijke </b> gebied, ga <code>scope</code> in.</p> </li> 
        <li value="3"> <p>Op het <b> gebied van de Waarde </b>, ga alle werkingsgebied in dat u in het werkingsgebiedgebied inging, door ruimten wordt gescheiden.</p> <p>Voorbeeld: <code>offline_access openid User.Read</code></p> </li> 
       </ol> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Aangepaste koppen</td> 
      <td>U hoeft niets in dit veld in te voeren.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Plaatsing token</td> 
      <td><code>In the header</code> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klik **verdergaan**.
1. In het venster dat verschijnt, keur **** goed om de verbinding te voltooien en op de module terug te komen.
