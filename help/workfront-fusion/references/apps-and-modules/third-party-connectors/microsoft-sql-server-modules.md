---
title: Microsoft SQL Server-modules
description: U kunt  [!DNL Adobe Workfront Fusion]  gebruiken om met de Server van Microsoft te verbinden SQL.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server] modules

Met [!DNL Adobe Workfront Fusion] kunt u verbinding maken met [!UICONTROL Microsoft SQL Server] .

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

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



## De service [!DNL Microsoft SQL Server] verbinden met [!DNL Workfront Fusion]

Voor instructies over het aansluiten van uw [!DNL Microsoft SQL Server] rekening aan [!UICONTROL Workfront Fusion], zie [ een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Sommige Microsoft-toepassingen gebruiken dezelfde verbinding, die is gekoppeld aan individuele gebruikersmachtigingen. Daarom bij het creëren van een verbinding, toont het scherm van de toestemmingstoestemming om het even welke toestemmingen die eerder aan de verbinding van deze gebruiker werden verleend, naast om het even welke nieuwe toestemmingen nodig voor de huidige toepassing.
>
>Bijvoorbeeld, als een gebruiker &quot;Gelezen lijst&quot;toestemmingen heeft die via de schakelaar van Excel worden verleend en dan een verbinding in de schakelaar van Vooruitzichten creeert om e-mails te lezen, zal het scherm van de toestemmingstoestemming zowel de reeds verleende &quot;Gelezen lijst&quot;toestemming en de onlangs vereiste &quot;Schrijf e-mail&quot;toestemming tonen.

## [!DNL Microsoft SQL Server] modules gebruiken

U kunt uw aangepaste logica rechtstreeks op uw databaseserver uitvoeren via opgeslagen procedures. [!DNL Adobe Workfront Fusion] laadt de interface van invoer-/uitvoerparameters en recordset dynamisch, zodat elke parameter of waarde afzonderlijk kan worden toegewezen. Voordat u begint met het configureren van uw scenario, moet u ervoor zorgen dat de account die u gebruikt om verbinding te maken met uw database, leestoegang heeft tot `INFORMATION_SCHEMA.ROUTINES` - en `INFORMATION_SCHEMA.PARAMETERS` -weergaven.

Wanneer [!DNL Fusion] de verbinding met de [!DNL SQL server] bestemming vestigt, identificeert de [!DNL Fusion] gebruiker de Gastheer (de domeinnaam of het IP-adres waar de server wordt gehost) en de poort. [!DNL Fusion] kan verbinding maken met elke beschikbare host en poort.

Voor informatie over specifieke IP adressen die door [!DNL Workfront Fusion] worden gebruikt, zie [ IP Adressen voor toegang tot  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Raadpleeg de documentatie van [!DNL Microsoft SQL Server] voor meer informatie over het maken van een opgeslagen procedure.

>[!NOTE]
>
>[!DNL Workfront Fusion] ondersteunt geen meerdere recordsets. Alleen de eerste wordt verwerkt.

## Fout bij oplossen [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Lock wait timeout exceeded; try restarting transaction]

Deze fout treedt op wanneer u dezelfde gegevens wijzigt met behulp van meerdere modules. Dit wordt veroorzaakt door SQL-transacties.

Wanneer een SQL-module wordt uitgevoerd, wordt een transactie gestart. De transactie wordt gebeëindigd nadat het scenario volledig wordt uitgevoerd.

Als een andere module probeert om tot de zelfde gegevens toegang te hebben, moet het wachten tot de vorige transactie wordt gebeëindigd. Aangezien de eerste transactie zal worden gebeëindigd nadat het scenario wordt gebeëindigd, kan de tweede transactie nooit beginnen.

### Oplossing:

Schakel Automatisch vastleggen in. Automatisch vastleggen voltooit (legt) elke transactie direct nadat de module is uitgevoerd.

1. Klik het [!UICONTROL Scenario settings] pictogram van de de montagespictogram van het pictogram ![ Scenario ](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png) bij de bodem van het scherm.
1. Klik op het selectievakje **[!UICONTROL Auto commit]** .
1. Klik op **[!UICONTROL OK]** om de scenario-instellingen op te slaan.
