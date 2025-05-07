---
title: Wederzijdse TLS gebruiken in HTTP-modules in Adobe Workfront Fusion
description: U kunt Wederzijdse TLS gebruiken in uw Adobe Workfront Fusion HTTP-modules, zodat beide zijden van de informatietransactie de identiteit van de ander kunnen verifiëren.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 89017451c8e0b821616adda861222127e100a08d
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Wederzijdse TLS gebruiken in HTTP-modules in [!DNL Adobe Workfront Fusion]

## Overzicht van wederzijdse TLS

Wanneer u gegevens via internet verzendt, is het belangrijk ervoor te zorgen dat deze naar de juiste locatie worden verzonden en dat alleen de beoogde ontvanger deze kan lezen. Als TLS is ingeschakeld, gebruikt de client (computer die om informatie vraagt) certificaten om de identiteit van de server (computer die informatie verschaft) te verifiëren. Hierdoor worden veilige HTTP-verbindingen gemaakt.

Met wederzijdse TLS kan deze identiteitsbevestiging op beide manieren verlopen. Wanneer de server zijn certificaat verzendt om zijn identiteit aan de cliënt te verifiëren, vraagt het ook het certificaat van de cliënt. Dit zorgt ervoor dat de server geen informatie naar een plaats of een gebruiker verzendt die het zou misbruiken.

>[!INFO]
>
>**Voorbeeld:**
>
>* **TLS**: Wanneer een persoon &quot;MyGreatBank.com&quot;in browser typt, willen zij zeker zijn dat zij naar Mijn Grote Bank gaan, niet een website die hun bankgegevens zou kunnen misbruiken of verkopen. Ze willen ook zeker weten dat hun bankrekeninggegevens gecodeerd zijn.
>
>   Wanneer de browser (de client) verbinding maakt met MyGreatBank.com (de server), vereist TLS een certificaat van MyGreatBank.com om de identiteit ervan te verifiëren. Het certificaat wordt geleverd door een certificeringsinstantie zoals [!DNL DigiCert] of [!DNL Thawte] . Omdat de browser de certificeringsinstantie vertrouwt, is de verbinding mogelijk.
>
>* **Wederzijdse TLS**: MySoftware.com is een softwarecliënt die informatie van MyGreatBank.com API vereist. MyGreatBank staat alleen vertrouwde clients toe verbinding te maken met hun servers. Naast de regelmatige controle van het TLS op de identiteit van MyGreatBank.com, verifieert het proces van de TLS/Certificate Authority dus ook het verzoek van MySoftware.com.

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

## Uw [!DNL Workfront Fusion] openbare certificaat opgeven

Wanneer u met een HTTP-aanvraag verbinding maakt met een webservice, vereist de webservice gewoonlijk een [!DNL Workfront Fusion] openbaar certificaat voor verificatie. Hierdoor kan de webservice het certificaat dat in de HTTP-aanvraag wordt aangeboden, vergelijken met het certificaat in het bestand, zodat u zeker weet dat het certificaat zich op de lijst van gewenste personen van de webservice bevindt.

Raadpleeg de documentatie bij de webservice voor instructies over het uploaden van het openbare [!DNL Adobe Workfront Fusion] -certificaat naar een webservice.

>[!NOTE]
>
>U moet mogelijk andere informatie opgeven naast het certificaat. Raadpleeg de API-documentatie van de webservice voor informatie over wat een webservice nodig heeft.

U kunt de volgende koppelingen gebruiken om de openbare certificaten van Workfront Fusion te downloaden. Om van uw datacenter de plaats te bepalen, zie [ uw datacenter ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md) in artikel vormen IP Adressen voor Fusie in de lijst van gewenste personen van uw organisatie identificeren.

### Certificaten voor 2025

>[!IMPORTANT]
>
>* Deze [!DNL Workfront Fusion] openbare certificaten verlopen op **4 April, 2026** (VS en EU) of **25 November, 2025** (Azure). Nadat uw certificaat is verlopen, moet u een nieuw certificaat uploaden naar de webservice. We raden u aan:
>
>   * Noteer de vervaldatum en stel een herinnering voor uzelf in om het certificaat te uploaden naar uw webservice.
>   * Bladwijzer deze pagina om de nieuwe certificaten gemakkelijk te vinden.
>
>* Dit zijn mTLS-certificaten die geen jokertekens bevatten.

| Datacenter | Koppeling downloaden | Geldige datums |
|---|---|---|
| VS-datacenter |  [!DNL Workfront Fusion]  Certificaat 2025 van de Download [&#128279;](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-us-mtls-certificate.pem) | 3 maart 2025 tot 4 april 2026 |
| EU-datacenter | [ Certificaat 2025 van de Download  [!DNL Workfront Fusion]  EU ](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-eu-mtls-certificate.pem) | 3 maart 2025 tot 4 april 2026 |
| Azure Cluster | [ Download  [!DNL Workfront Fusion]  Azure Certificaat 2025 ](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-az-mtls-certificate.pem) | 24 oktober 2024 tot 25 november 2025 |

<!--

### Certificates for 2024

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2025, available above.
>* These [!DNL Workfront Fusion] public certificates expire on **May 7, 2025**. After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
|---|---|---|
| US Datacenter | [Download [!DNL Workfront Fusion] Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |
| EU Datacenter | [Download [!DNL Workfront Fusion] EU Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |

-->

## Wederzijdse TLS inschakelen in HTTP-modules van [!DNL Workfront Fusion]

Alle aanvraagmodules [!DNL Workfront Fusion] [!UICONTROL HTTP] hebben de optie om wederzijdse TLS in te schakelen.

Wederzijdse TLS inschakelen in een aanvraagmodule [!UICONTROL HTTP] :

1. Voeg een aanvraagmodule [!UICONTROL HTTP] toe aan uw scenario.
1. Beginnen met het configureren van de module.

   Voor instructies bij het vormen van een [!UICONTROL HTTP] verzoekmodule, zie het aangewezen artikel onder [ Universele schakelaars ](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

1. Schakel **[!UICONTROL Show advanced settings]** onder aan de module in.
1. Schakel **[!UICONTROL Use Mutual TLS]** in.
