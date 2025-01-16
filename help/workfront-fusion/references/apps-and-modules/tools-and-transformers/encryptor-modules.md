---
title: Versleuteling
description: Met Adobe Workfront Fusion Encryptor-modules kunt u alle tekstgegevens versleutelen. Ze ondersteunen momenteel berichtversleuteling via AES256 en PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Versleuteling

[!DNL Adobe Workfront Fusion] [!UICONTROL Encryptor] -modules kunt u alle tekstgegevens versleutelen. Zij steunen momenteel berichtencryptie via AES256 en PGP ([!UICONTROL OpenPGP]).

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
   <p>Vereiste voor verouderde licentie: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en -integratie], [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering]</p>
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

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Berichtversleuteling en -ontsleuteling met PGP

Wanneer het coderen en het decrypteren via PGP, is het noodzakelijk om keychain te gebruiken en een privé of openbare sleutel (of allebei) tot stand te brengen.

Voor meer informatie over openbare en privé sleutels, zie [ Verklarende woordenlijst van de Fusie van Adobe Workfront ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md). <!--For more information on keychains, see [Keys in [!DNL Adobe Workfront Fusion]]().-->

## [!UICONTROL Encryptor] modules en hun velden

Wanneer u [!UICONTROL Encryptor] modules configureert, worden de volgende velden weergegeven. Een bolde titel in een module wijst op een vereist gebied.

### Een PGP-bericht versleutelen

Met deze module kunt u een bericht versleutelen met openbare en persoonlijke sleutels.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Voer de persoonlijke sleutel van de afzender in. Hierdoor kan de identiteit van de afzender worden geverifieerd.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Voer de openbare sleutel van de ontvanger in.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Voer het bericht in dat u wilt versleutelen.</td>
    </tr>

### Een PGP-bericht decoderen

Deze module staat u toe om een bericht te decrypteren gebruikend openbare en privé sleutels.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Voer de persoonlijke sleutel van de ontvanger in.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Voer de openbare sleutel van de ontvanger in. Hierdoor kan de identiteit van de afzender worden geverifieerd.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Wijs het bericht toe dat u wilt decoderen.</td>
    </tr>
</table>
