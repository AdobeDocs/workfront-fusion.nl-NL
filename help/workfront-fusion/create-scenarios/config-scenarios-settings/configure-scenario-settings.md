---
content-type: reference
title: Scenario-instellingen configureren
description: U kunt specifieke montages voor scenario's in het paneel van scenario-montages vormen.
author: Becky
feature: Workfront Fusion
exl-id: 105e3d39-b0ef-4c22-901d-fb4f29e685a9
source-git-commit: 85b7a5e07ef7d3169b31f91bc54d4cb246199443
workflow-type: tm+mt
source-wordcount: '1253'
ht-degree: 0%

---

# Scenario-instellingen configureren

U kunt specifieke montages voor scenario&#39;s in het paneel van scenario-montages vormen.

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
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## De scenario-instellingen openen

1. Klik **Scenario&#39;s** in het linkerpaneel.
1. Zoek het gewenste scenario en klik op de naam.
1. Klik overal op het scenario om de scenarioredacteur in te gaan.
1. Klik op het tandwielpictogram links onder op de pagina.

   ![ montages van het Scenario ](assets/scenario-settings-350x221.png)

   In het deelvenster [!UICONTROL Scenario settings] dat wordt weergegeven, kunt u verschillende geavanceerde instellingen voor het scenario configureren.
1. Schakel indien nodig de Scenario-instellingen in of uit. Zie [ de montagesopties van het Scenario ](#scenario-settings-options) hieronder.

## Opties voor Scenario-instellingen

### [!UICONTROL Sequential processing]

Met deze optie worden alle executies op volgorde uitgevoerd. Deze optie is vooral van belang voor Webhooks en voor Onvolledige uitvoeringen.

Wanneer de opeenvolgende verwerking wordt toegelaten, zijn de parallelle uitvoeringen van het scenario gehandicapt.

**Onmiddellijke Webhooks**: Als een webhaaktrekker als `instant` wordt gevormd en &quot;Opeenvolgende verwerking&quot;wordt toegelaten, dan zullen alle onmiddellijke webhaakpayloads een rij worden gevormd en in de orde worden verwerkt dat zij aankomen. Dit kan handig zijn wanneer gebeurtenissen van externe systemen in een exacte volgorde worden verwerkt.

>[!NOTE]
>
>Er zullen automatische verwerkingstermijnen zijn aangezien elke lading wordt verwerkt alvorens volgende is begonnen.

**Onvolledige Uitvoeringen**: Als de &quot;Onvolledige Uitvoeringen&quot;ook wordt toegelaten, als een fout tijdens de uitvoering van een scenario voorkomt, wordt het scenario gepauzeerd. Een van de volgende gebeurtenissen vindt dan plaats:

* Als de Opeenvolgende verwerkingsoptie **** wordt toegelaten, houdt de Fusie van Workfront op verwerkend de reeds bestaande opeenvolging tot alle onvolledige uitvoeringen worden opgelost.
* Als de Opeenvolgende verwerkingsoptie **** gehandicapt is, blijft het scenario volgens zijn programma lopen, vergezeld van herhaalde pogingen om de onvolledige uitvoeringen opnieuw uit te voeren.

  Voor meer informatie over onvolledige uitvoeringen, zie [ Mening en los onvolledige uitvoeringen ](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md) op.

  >[!NOTE]
  >
  >De opeenvolgende verwerking kan een vertraging in de uitvoering van een scenario veroorzaken. Als er onvolledige uitvoeringen nog in de rij zijn wanneer een onmiddellijk scenario trekkers of een gepland scenario om wordt geplaatst uit te voeren, zal dat scenario na alle uitvoeringen uitvoeren alvorens het in de rij volledig is.
  >
  >Als het gebruiksgeval voor uw scenario&#39;s geen opeenvolgende verwerking vereist, adviseren wij onbruikbaar makend de opeenvolgende verwerkingsoptie.

  Voor meer informatie bij het plannen, zie [ Plan een scenario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

### Gegevens zijn vertrouwelijk

Zodra een scenario is uitgevoerd, kunt u door gebrek vertoningsinformatie tonen over welke gegevens door modules in het scenario werden verwerkt. Schakel de optie [!UICONTROL Data is confidential] in als u niet wilt dat deze gegevens worden opgeslagen.

>[!IMPORTANT]
>
>Als u deze optie inschakelt, kan het moeilijk zijn fouten op te lossen die tijdens de uitvoering van een scenario kunnen optreden.

### [!UICONTROL Allow storing incomplete executions]

Deze optie bepaalt hoe Adobe Workfront Fusion verder gaat als er een fout optreedt tijdens de uitvoering van een scenario. Als deze optie is ingeschakeld, wordt het scenario gepauzeerd en naar de onvolledige uitvoermap verplaatst. Dit geeft u de mogelijkheid om de kwestie te bevestigen en verder uit te voeren van waar het scenario werd tegengehouden. Als deze optie is uitgeschakeld, stopt de uitvoering van het scenario en wordt een terugdraaifase gestart.

Voor meer informatie over onvolledige uitvoeringen, zie [ Mening en los onvolledige uitvoeringen ](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md) op.

### Gegevensverlies inschakelen

Deze optie heeft te maken met het inschakelen van gegevensverlies als Workfront Fusion een bundel niet opslaat in de wachtrij van onvolledige uitvoeringen (bijvoorbeeld vanwege een gebrek aan vrije ruimte). Als deze optie is ingeschakeld, gaan de gegevens verloren om onderbrekingen in de uitvoering van het algemene scenario te voorkomen. Dit is nuttig voor scenario&#39;s waar de hoogste prioriteit is ononderbroken uitvoering en de inkomende onjuiste gegevens niet zo belangrijk zijn.

Buiten dat, wanneer het uitvoeren van een scenario, kan een module soms een dossier ontmoeten dat groter is dan de maximaal toegestane grootte. In dit geval gaat Workfront Fusion verder volgens de instelling van de optie [!UICONTROL Enable data loss] en wordt een waarschuwingsbericht weergegeven.

Voor meer informatie over onvolledige uitvoeringen, zie [ Mening en los onvolledige uitvoeringen ](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md) op.

Voor meer informatie over maximumdossiergrootte, zie [ de prestatiesgidsen van de Fusie ](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#files).

Voor meer informatie over waarschuwingen, zie [ types van Fout ](/help/workfront-fusion/references/errors/error-processing.md).

### [!UICONTROL Auto commit]

De instellingen [!UICONTROL Auto commit] zijn van toepassing op transacties en definiëren de manier waarop een scenario moet worden verwerkt. Als Auto begaan optie is, begint de commit fase op elke module onmiddellijk na de voltooiing van de verrichtingsfase. Als de optie Automatisch vastleggen is uitgeschakeld, wordt pas een bewerking uitgevoerd als alle modules worden uitgevoerd (dit is de standaardmodus).

### Maximumaantal cycli

>[!NOTE]
>
>U moet **tonen Geavanceerde montages** checkbox toelaten om deze optie te zien.


Het plaatsen van meer cycli kan nuttig zijn wanneer u verbindingsonderbreking aan een derdedienst wilt verhinderen en ervoor zorgen dat alle verslagen binnen de één scenario looppas worden verwerkt.

* Als het scenario met een opiniepeilingtrigger begint, bepaalt het plaatsen het maximum aantal cycli die tijdens de uitvoering van het scenario worden toegestaan.

  Voor meer informatie over opiniepeilingstrekkers, zie [ Opiniepeilende trekkers ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#polling-triggers) in het overzicht van de artikelmodule.

* Als het scenario met een onmiddellijke trekker begint, wordt het plaatsen genegeerd en alle hangende gebeurtenissen worden verwerkt tijdens één enkele scenariouitvoering, één gebeurtenis per één cyclus.

  Voor meer informatie over onmiddellijke trekkers, zie [ Onmiddellijke trekkers ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) in het overzicht van de artikelmodule.

* Als het scenario niet met een trekker (instant/polling) begint, wordt het gespecificeerde maximumaantal cycli altijd uitgevoerd.

>[!BEGINSHADEBOX]

**Voorbeelden:** Workfront > [!UICONTROL Watch record] horloges voor nieuwe kwesties die binnen komen, en Workfront > [!UICONTROL Convert object] zet het nieuwe verzoek in een project om en wijst het het aangewezen malplaatje toe.

![ montages van het Scenario ](assets/scenario-settings-ex-1-350x157.png)

Een instelling [!UICONTROL more cycles] wordt alleen toegepast wanneer u de uitvoering van het scenario plant. Wanneer u de knop [!UICONTROL Run once] gebruikt, wordt rekening gehouden met de cyclusinstellingen.

#### Max. aantal cycli is ingesteld op 1 (standaardwaarde)

![ Maximum aantal cycli ](assets/max-number-cycles-1-350x201.png)

Het Max aantal cycli in de module Workfront > Watch records is ingesteld op `10` .
Als 100 verzoeken worden voorgelegd aan Workfront, en het Max aantal cyclusgebied wordt geplaatst aan 10, dan worden 90 dossiers onverwerkt verlaten na één scenario looppas. De volgende 10 dossiers worden verwerkt in de volgende geplande scenario uitvoering.

#### Max. aantal cycli is ingesteld op 10

Het Max aantal cycli in de module Workfront > Watch records is ingesteld op `10` .

Als 100 bestanden worden toegevoegd aan de map Dropbox en de optie Max. aantal cycli is ingesteld op 10, worden 10 bestanden verwerkt tijdens de eerste cyclus, de volgende 10 bestanden in de tweede cyclus, de volgende 10 bestanden in de derde cyclus enzovoort, totdat alle bestanden zijn verwerkt.

Alle bestanden worden verwerkt binnen 1 scenario-uitvoering.

U kunt de reeds in werking gestelde cycli in de details van het Scenario zien:

![ het detail van het Scenario ](assets/scenario-detail-350x207.png)

Voor meer informatie over deze pagina, zie {de details van 0} Scenario [.](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-details.md)

>[!ENDSHADEBOX]

### Aantal opeenvolgende fouten

Definieert het maximum aantal opeenvolgende uitvoeringspogingen voordat de uitvoering van een scenario wordt gedeactiveerd (exclusief `DataError` , `DuplicateDataError` , `ModuleTimeoutError` en `ConnectionError` ).

Voor meer informatie over fouten, zie [ types van Fout ](/help/workfront-fusion/references/errors/error-processing.md).

>[!NOTE]
>
>Als een scenario met een onmiddellijke trekker begint, wordt het plaatsen genegeerd en het scenario wordt onmiddellijk gedeactiveerd zodra de eerste fout is voorgekomen.

### Werkgroep

>[!NOTE]
>
>Deze instelling is alleen zichtbaar als aan de volgende twee voorwaarden is voldaan:
>
>* U bent een organisatiebeheerder of eigenaar
>* Er zijn meerdere arbeidersgroepen aan uw organisatie gekoppeld.

Dit het plaatsen wijst het scenario aan een specifieke arbeiderspool toe verbonden aan uw organisatie, die u toestaat om middelen aan prioritaire scenario&#39;s te wijden.

<!--

>[!NOTE]
>
>Organizations can request provisioning of one additional worker pool (for a total of 2).

-->
