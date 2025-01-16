---
title: Wederzijdse TLS gebruiken in HTTP-modules in Adobe Workfront Fusion
description: U kunt Wederzijdse TLS gebruiken in uw Adobe Workfront Fusion HTTP-modules, zodat beide zijden van de informatietransactie de identiteit van de ander kunnen verifiëren.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Wederzijdse TLS gebruiken in HTTP-modules in [!DNL Adobe Workfront Fusion]

>[!NOTE]
>
>Voor Adobe Workfront Fusion is naast een Adobe Workfront-licentie een [!DNL Adobe Workfront Fusion] -licentie vereist.

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

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td> 
   <td> <p>[!UICONTROL Pro] of hoger</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] [!DNL Adobe Workfront] -abonnement hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

&#42; om te weten te komen welk plan, vergunningstype, of toegang u hebt, contacteer uw [!DNL Workfront] beheerder.

&#42;&#42; voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Uw [!DNL Workfront Fusion] openbare certificaat opgeven


Wanneer u met een HTTP-aanvraag verbinding maakt met een webservice, vereist de webservice gewoonlijk een [!DNL Workfront Fusion] openbaar certificaat voor verificatie. Hierdoor kan de webservice het certificaat dat in de HTTP-aanvraag wordt aangeboden, vergelijken met het certificaat in het bestand, zodat u zeker weet dat het certificaat zich op de lijst van gewenste personen van de webservice bevindt.

Raadpleeg de documentatie bij de webservice voor instructies over het uploaden van het openbare [!DNL Adobe Workfront Fusion] -certificaat naar een webservice.

>[!NOTE]
>
>U moet mogelijk andere informatie opgeven naast het certificaat. Raadpleeg de API-documentatie van de webservice voor informatie over wat een webservice nodig heeft.

U kunt de volgende koppelingen gebruiken om de openbare certificaten van Workfront Fusion te downloaden:

### Certificaten voor 23 april 2023-7 mei 2024

>[!IMPORTANT]
>
>* Deze [!DNL Workfront Fusion] openbare certificaten verlopen op 7 mei 2025. Nadat uw certificaat is verlopen, moet u een nieuw certificaat uploaden naar de webservice. We raden u aan:
>
>   * Noteer de vervaldatum en stel een herinnering voor uzelf in om het certificaat te uploaden naar uw webservice.
>   * Bladwijzer deze pagina om de nieuwe certificaten gemakkelijk te vinden.
>
>* Dit zijn mTLS-certificaten die geen jokertekens bevatten.

* [ [!DNL Workfront Fusion]  Certificaat 2023 van de download](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem)
* [ [!DNL Workfront Fusion]  EU-certificaat 2023 downloaden](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem)

  Voor gebruik in de EU

<!--

### Certificates for November 14, 2022 - July 15, 2023

>[!IMPORTANT]
>
>* These [!DNL Workfront Fusion] public certificates expire on July 15, 2023.
>* These are wildcard mTLS certificates.

* [Download [!DNL Workfront Fusion] Certificate 2023](https://cdn.experience.workfront.com/Documentation/Workfront+Fusion+2.0+public+certificates/app_workfrontfusion_com-jul-15-2023+updated.cer)
* [Download [!DNL Workfront Fusion] EU Certificate 2023](https://cdn.experience.workfront.com/Documentation/Workfront+Fusion/app-eu_workfrontfusion_com-jul-15-2023.cer)

   For use in the EU 

   -->

## Wederzijdse TLS inschakelen in HTTP-modules van [!DNL Workfront Fusion]

Alle aanvraagmodules [!DNL Workfront Fusion] [!UICONTROL HTTP] hebben de optie om wederzijdse TLS in te schakelen.

Wederzijdse TLS inschakelen in een aanvraagmodule [!UICONTROL HTTP] :

1. Voeg een aanvraagmodule [!UICONTROL HTTP] toe aan uw scenario.
1. Beginnen met het configureren van de module.

   <!--For instructions on configuring an [!UICONTROL HTTP] request module, see the appropriate article under [[!UICONTROL Universal connectors] modules](/help/workfront-fusion/references/apps-and-modules/universal-connectors/).-->

1. Schakel **[!UICONTROL Show advanced settings]** onder aan de module in.
1. Schakel **[!UICONTROL Use Mutual TLS]** in.
