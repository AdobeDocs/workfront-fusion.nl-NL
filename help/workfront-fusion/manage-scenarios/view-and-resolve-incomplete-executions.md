---
title: Onvolledige uitvoeringen weergeven en oplossen
description: In de map [!UICONTROL Incomplete executions] worden scenario-uitvoeringen opgeslagen die niet zijn voltooid vanwege een fout. Elke opgeslagen onvolledige uitvoering kan handmatig of automatisch worden opgelost.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# Onvolledige uitvoeringen weergeven en oplossen

In de map [!UICONTROL Incomplete executions] worden scenario-uitvoeringen opgeslagen die niet zijn voltooid vanwege een fout. Elke opgeslagen onvolledige uitvoering kan handmatig of automatisch worden opgelost.

>[!NOTE]
>
>Standaard is het opslaan van onvolledige uitvoeringen uitgeschakeld. Schakel de optie [!UICONTROL Allow storing incomplete executions] in de geavanceerde instellingen van het scenario in om deze optie in te schakelen.
>
>Voor meer informatie over scenario montages, zie [&#x200B; scenario montages &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md) vormen.

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
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
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
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] Workfront-abonnement: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>[!UICONTROL Ultimate] Workfront-abonnement: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configuraties op toegangsniveau*</td> 
   <td> 
     <p>U moet een Workfront Fusion-beheerder zijn voor uw organisatie.</p>
     <p>U moet een Workfront Fusion-beheerder zijn voor uw team.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Onvolledige uitvoeringen weergeven

Als een module een fout tijdens zijn verrichting ontmoet, wordt een nieuwe onvolledige uitvoering toegevoegd aan de Onvolledige uitvoeringenomslag. Elke onvolledige uitvoering bevat de blauwdruk van het scenario en alle bundels die in de ontbroken module kunnen worden in kaart gebracht. De lijst met onvolledige uitvoeringen kan worden geopend door te klikken op de tab [!UICONTROL Incomplete Executions] op de pagina met de details van het scenario.

<!--

![Incomplete executions tab](assets/incomplete-executions-tab-350x102.png)

-->

Voor meer informatie, zie [&#x200B; Fouten resulterend in onvolledige uitvoeringen &#x200B;](#errors-resulting-into-incomplete-executions) in dit artikel.

>[!NOTE]
>
>De huidige groottelimiet van de onopgeloste onvolledige uitvoeringenomslag per scenario is 10 MB. Als uw scenario deze grens overschrijdt, kunt u de volgende fout zien:
>
>`DLQ limit per scenario has been exceeded`
>
>Teams zijn beperkt tot in totaal 500 MB voor alle onopgeloste onvolledige uitvoeringen.
>
>Voor meer informatie, zie [&#x200B; gegevensverlies &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) toelaten in artikel vormt scenario montages.


## Onvolledige uitvoeringen oplossen via het tabblad Onvolledige uitvoeringen

Wanneer een nieuwe onvolledige uitvoering wordt opgeslagen, kunt u deze als volgt oplossen:

1. Open het desbetreffende scenario.
1. Klik op de tab **[!UICONTROL Incomplete Executions]** .
1. Zoek de onvolledige uitvoering die u wilt oplossen en klik op **[!UICONTROL Details]** .
1. Open het logboek van de module waar alle verrichtingen van de module worden getoond.
1. Zoek de mislukte bewerking en klik op **[!UICONTROL Resolve]** :

   ![&#x200B; Los knoop &#x200B;](assets/resolve-btn-350x188.png) op



## Onvolledige uitvoeringen oplossen via het tabblad Historie

Als u het logboek van alle verrichtingen van de module wilt zien alvorens u probeert om de onvolledige uitvoering op te lossen, kunt u de onvolledige uitvoering van de [!UICONTROL History] omslag oplossen:

1. Open het desbetreffende scenario.
1. Klik op de tab **[!UICONTROL History]** .
1. Zoek de mislukte uitvoering van het scenario en klik op **[!UICONTROL Details]** .
1. Open het logboek van de module waar alle verrichtingen van de module worden getoond.
1. Zoek de mislukte bewerking en klik op **[!UICONTROL Resolve]** :

   ![&#x200B; Los knoop &#x200B;](assets/resolve-btn-350x188.png) op

## Opties in verband met onvolledige uitvoeringen

De volgende opties in het deelvenster [!UICONTROL Scenario settings] bepalen of en hoe de onvolledige uitvoeringen worden opgeslagen:

* Toestaan dat onvolledige uitvoeringen worden opgeslagen
* Opeenvolgende verwerking
* Gegevensverlies inschakelen

Voor meer informatie over deze opties, zie [&#x200B; scenario montages &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md) vormen.

## Fouten die tot onvolledige uitvoering leiden

Er zijn verschillende soorten fouten die leiden tot het opslaan van onvolledige uitvoeringen. Deze kunnen het volgende omvatten:

* Validatiefouten die het gevolg zijn van onvolledige of onjuiste gegevens, voornamelijk als gevolg van een ontbrekend item dat wordt verwacht om alle gegevens in een module te kunnen verwerken.
* Fouten die optreden als gevolg van de onbeschikbaarheid van de eindbestemming als gevolg van een tijdelijke of langdurige verbindingsfout (bijvoorbeeld tijdens verbinding met e-mail of externe FTP-server).

Als een fout op de eerste module in het scenario voorkomt, houdt de uitvoering onmiddellijk tegen en geen onvolledige uitvoering wordt opgeslagen.

Als een fout op een andere module voorkomt en er geen foutenmanagerroute in bijlage is, komt één van het volgende voor:

* Een onvolledige uitvoeringsrecord met automatisch opnieuw proberen wordt opgeslagen voor de volgende fouttypen:

   * `ConnectionError`
   * `RateLimitError`
   * `OutOfSpaceError`
   * `ModuleTimeoutError`

* Een onvolledige uitvoeringsrecord zonder automatisch opnieuw proberen wordt opgeslagen voor de volgende fouttypen:

   * `DataError`
   * `InvalidConfigurationError`
   * `InvalidAccessTokenError`
   * `UnexpectedError`
   * `MaxFileSizeExceededError`
   * `MaxResultsExceededError`

* Als het fouttype iets anders is dan hierboven, mislukt de uitvoering.
