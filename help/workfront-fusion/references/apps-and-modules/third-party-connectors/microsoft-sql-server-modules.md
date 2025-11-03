---
title: Microsoft SQL Server-modules
description: Met Adobe Workfront Fusion kunt u verbinding maken met Microsoft SQL Server.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server] modules

U kunt Adobe Workfront Fusion gebruiken om verbinding te maken met [!UICONTROL Microsoft SQL Server] .

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## De [!DNL Microsoft SQL Server] -service verbinden met Workfront Fusion

Voor instructies over het aansluiten van uw [!DNL Microsoft SQL Server] rekening aan [!UICONTROL Workfront Fusion], zie [&#x200B; een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies &#x200B;](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Sommige Microsoft-toepassingen gebruiken dezelfde verbinding, die is gekoppeld aan individuele gebruikersmachtigingen. Daarom bij het creëren van een verbinding, toont het scherm van de toestemmingstoestemming om het even welke toestemmingen die eerder aan de verbinding van deze gebruiker werden verleend, naast om het even welke nieuwe toestemmingen nodig voor de huidige toepassing.
>
>Bijvoorbeeld, als een gebruiker &quot;Gelezen lijst&quot;toestemmingen heeft die via de schakelaar van Excel worden verleend en dan een verbinding in de schakelaar van Vooruitzichten creeert om e-mails te lezen, zal het scherm van de toestemmingstoestemming zowel de reeds verleende &quot;Gelezen lijst&quot;toestemming en de onlangs vereiste &quot;Schrijf e-mail&quot;toestemming tonen.

## [!DNL Microsoft SQL Server] modules gebruiken

U kunt uw aangepaste logica rechtstreeks op uw databaseserver uitvoeren via opgeslagen procedures. Adobe Workfront Fusion laadt de interface van invoer-/uitvoerparameters en recordset dynamisch, zodat elke parameter of waarde afzonderlijk kan worden toegewezen. Voordat u begint met het configureren van uw scenario, moet u ervoor zorgen dat de account die u gebruikt om verbinding te maken met uw database, leestoegang heeft tot `INFORMATION_SCHEMA.ROUTINES` - en `INFORMATION_SCHEMA.PARAMETERS` -weergaven.

Wanneer [!DNL Fusion] de verbinding met de [!DNL SQL server] bestemming vestigt, identificeert de [!DNL Fusion] gebruiker de Gastheer (de domeinnaam of het IP-adres waar de server wordt gehost) en de poort. [!DNL Fusion] kan verbinding maken met elke beschikbare host en poort.

Voor informatie over specifieke IP adressen die door de Fusie van Workfront worden gebruikt, zie [&#x200B; IP Adressen voor de toegang tot van de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Raadpleeg de documentatie van [!DNL Microsoft SQL Server] voor meer informatie over het maken van een opgeslagen procedure.

>[!NOTE]
>
>Workfront Fusion biedt geen ondersteuning voor meerdere recordsets. Alleen de eerste wordt verwerkt.

## Fout bij oplossen [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Lock wait timeout exceeded; try restarting transaction]

Deze fout treedt op wanneer u dezelfde gegevens wijzigt met behulp van meerdere modules. Dit wordt veroorzaakt door SQL-transacties.

Wanneer een SQL-module wordt uitgevoerd, wordt een transactie gestart. De transactie wordt gebeëindigd nadat het scenario volledig wordt uitgevoerd.

Als een andere module probeert om tot de zelfde gegevens toegang te hebben, moet het wachten tot de vorige transactie wordt gebeëindigd. Aangezien de eerste transactie zal worden gebeëindigd nadat het scenario wordt gebeëindigd, kan de tweede transactie nooit beginnen.

### Oplossing:

Schakel Automatisch vastleggen in. Automatisch vastleggen voltooit (legt) elke transactie direct nadat de module is uitgevoerd.

1. Klik het [!UICONTROL Scenario settings] pictogram van de de montagespictogram van het pictogram ![&#x200B; Scenario &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png) bij de bodem van het scherm.
1. Klik op het selectievakje **[!UICONTROL Auto commit]** .
1. Klik op **[!UICONTROL OK]** om de scenario-instellingen op te slaan.
