---
title: Connect Adobe Workfront Fusion voor Google Services met bijgewerkte beveiligingsmaatregelen
description: Google heeft beperkingen geïntroduceerd op de manier waarop gebruikers hun API kunnen gebruiken. In dit artikel wordt beschreven hoe u Adobe Workfront Fusion kunt verbinden met Google. Hierbij worden deze beveiligingsmaatregelen voor updates in aanmerking genomen.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Connect Adobe Workfront Fusion voor Google Services met bijgewerkte beveiligingsmaatregelen

Google heeft beperkingen geïntroduceerd op de manier waarop gebruikers hun API kunnen gebruiken. In dit artikel wordt beschreven hoe u Adobe Workfront Fusion kunt verbinden met Google. Hierbij worden deze beveiligingsmaatregelen voor updates in aanmerking genomen.

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

## Beperkingen voor Google Services

Google heeft vanaf 1 juni 2020 beperkingen ingevoerd voor het gebruik van de API door gebruikers. Deze beveiligingsmaatregelen beschermen Google-gebruikers tegen lekkage of misbruik van hun persoonsgegevens op Google.

Deze beperkingen gelden voor de toepassingen Gmail en Google Drive.

Voor meer informatie over deze beperkingen, zie &quot;Aanvullende Vereisten voor Specifieke API Scopes&quot;in het [ Google API het Beleid van de Gegevens van de Gebruiker van de Diensten ](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)

Om toegang te krijgen tot beperkt bereik, moet de verbonden dienst (Adobe Workfront Fusion of elke andere dienst die de gegevens van de gebruiker via de API benadert) worden geverifieerd en moet een beoordelingsverklaring hebben om aan te tonen dat de dienst veilig en transparant is over hoe zij de gegevens gebruiken. Workfront Fusion voldoet aan alle Google-vereisten voor toegang tot beperkte bereikregels. De meeste verbonden services van derden in Workfront Fusion hebben echter geen beoordelingsverklaring en voldoen daarom niet aan de voorwaarden van Google. Daarom mag Workfront Fusion geen gegevens naar deze services verzenden.

## Uitzonderingen op Google Services-beperkingen

Er zijn een paar uitzonderingen die het mogelijk maken om gegevens naar een niet-erkende derdedienst te verzenden die niet de Brief van Beoordeling heeft zonder om het even welke nieuwe beperkingen te schenden. Ze verschillen op basis van Google Workspace met de Workfront Fusion OAuth-client, Google Workspace met een andere OAuth-client of @gmail.com en @googlemail.com.

* [Google Workspace met Workfront Fusion OAuth-client](#google-workspace-with-workfront-fusion-oauth-client)
* [Google Workspace met een andere OAuth-client](#google-workspace-with-another-oauth-client)
* [@gmail.com en @googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace met Workfront Fusion OAuth-client

Workfront Fusion maakt gebruik van de domeinbrede installatieuitzondering. Installatie in het gehele domein is geschikt voor Google Workspace-gebruikers en staat gebruikers toe om niet-goedgekeurde services zonder beperkingen te integreren. Als u een Google Workspace-gebruiker bent, hoeft u geen extra stappen uit te voeren en kunt u rechtstreeks verbinding maken met niet-goedgekeurde services.

### Google Workspace met een andere OAuth-client

Google Workspace-gebruikers die liever hun eigen OAuth-client gebruiken in plaats van de Workfront Fusion OAuth-client, kunnen verbinding maken met Google Services via de aanpak voor intern gebruik. Deze optie is bedoeld voor geavanceerde gebruikers. Voor instructies, zie [ Connect Adobe Workfront Fusion aan de Diensten van Google gebruikend een douaneOAuth cliënt ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

### @gmail.com en @googlemail.com {#gmailcom-and-googlemailcom}

Gebruikers die via @gmail.com of @googlemail.com toegang krijgen tot Google Services, kunnen verbinding maken met Google Services via de aanpak Persoonlijk gebruik. Deze optie is bedoeld voor geavanceerde gebruikers. Voor instructies, zie [ Connect Adobe Workfront Fusion aan de Diensten van Google gebruikend een douaneOAuth cliënt ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## Veelgestelde vragen

* [Welke toepassingen in Adobe Workfront Fusion worden beïnvloed?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Heb ik een Google Workspace-account?](#do-i-have-a-g-suite-account)
* [Wat moet ik doen als ik een @gmail.com of @googlemail.com gebruiker ben?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [Wat moet ik doen als ik Google Workspace-gebruiker ben?](#what-should-i-do-if-im-a-g-suite-user)

### Welke toepassingen in Adobe Workfront Fusion worden beïnvloed? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive, Gmail en E-mail (verbonden met Gmail-account).

### Heb ik een Google Workspace-account? {#do-i-have-a-g-suite-account}

Als uw e-mailadres eindigt met @gmail.com of @googlemail.com, is uw account geen Google Workspace-account. Als uw Google-account eindigt met een aangepast domein zoals @my-company.com, is het een Google Workspace-account.

### Wat moet ik doen als ik @gmail.com of @googlemail.com gebruiker ben? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

Deze nieuwe beperkingen gelden alleen als u Google Drive of Gmail integreert. Als u verbinding wilt maken met Google Drive of Gmail, kunt u

* Overschakelen naar Google Workspace

  of

* Maak een aangepaste OAuth-client. Deze optie is bedoeld voor geavanceerde gebruikers.

  Voor instructies, zie [ Connect Adobe Workfront Fusion aan de Diensten van Google gebruikend een douaneOAuth cliënt ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Als u een andere service dan Google Drive of Gmail wilt integreren, zijn deze beperkingen niet van toepassing.

### Wat moet ik doen als ik Google Workspace-gebruiker ben? {#what-should-i-do-if-im-a-g-suite-user}

Er is geen vereiste actie.
