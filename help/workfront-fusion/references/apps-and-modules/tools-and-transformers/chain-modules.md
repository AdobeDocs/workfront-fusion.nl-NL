---
title: Ketenmodules
description: Gebruikend deze modules, kunt u scenario's samen ketenen, makend één vraag een andere.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: 454e06527fe1a624f36be3b7f3682ff49a61d42d
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Ketenmodules

Gebruikend de modules van de Keten, kunt u één scenario met een andere verbinden.

<!--This article will be about the specific module configuration-->

Voor instructies bij het plannen van ketende scenario&#39;s, zie [ de veelvoudige scenario&#39;s van de Keten samen ](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


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
   <p>Geen Workfront Fusion-licentievereiste</p>
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

## Ketenmodules en velden daarvan

### Triggers

#### Gegevens van bovenliggend item ontvangen

Deze module is de trekkermodule in het kindscenario, en door Vraag een module van het kindscenario in het ouderscenario teweeggebracht. Het ontvangt gegevens van het ouderscenario, dat in het kindscenario kan worden verwerkt.

Om de Receive gegevens van oudermodule te vormen:

1. Als u een bestaande gegevensstructuur wilt gebruiken, selecteert u in het veld Gegevensstructuur de gegevensstructuur die wordt gebruikt voor de invoergegevens van het scenario.

   of

   Om een nieuwe gegevensstructuur tot stand te brengen om als de inputgegevens van het scenario te gebruiken, **toe te voegen** naast het gebied van de gegevensstructuur en de gegevensstructuur tot stand te brengen.

   Voor instructies bij het creëren van een gegevensstructuur, zie [ structuren van Gegevens ](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Klik **O.K.** om de module te bewaren.

### Handelingen

#### Roep een kindscenario

Deze module wordt gevestigd in het ouderscenario. De gebieden wijzen op de gegevensstructuurreeks in Receive gegevens van oudermodule in het kindscenario.

>[!NOTE]
>
>* U kunt een bestaand kindscenario selecteren, of nieuwe creëren door deze module.
>* U kunt de gegevensstructuur creëren wanneer het creëren van kindscenario.

Om de Vraag een module van het kindscenario te vormen

1. Voeg de Vraag een module van het kindscenario aan uw scenario toe.
1. Om een bestaand kindscenario, op het gebied van de Keten te gebruiken, selecteer het kindscenario dat u wilt roepen.

   of

   Als u een nieuw onderliggend scenario wilt maken, klikt u op Toevoegen naast het veld Keten. Het kindscenario verschijnt in een afzonderlijk venster, met Receive gegevens van ouder en Terugkeer reactie van oudermodules op zijn plaats.

   De gebieden die in de trekkermodule van het kindscenario worden gevormd verschijnen in Vraag een module van het kindscenario.

1. Ga of kaart de informatie in die aan het kindscenario in Vraag een module van het kindscenario moet worden overgegaan.
1. Klik **O.K.** om de module te bewaren.

>[!NOTE]
>
>Als u een nieuw kindscenario voor deze module creeert, opent het kindscenario in een afzonderlijk browser venster, toestaand u om zowel de ouder als kindscenario&#39;s tezelfdertijd te zien en te vormen.

#### Reactie op bovenliggende toepassing retourneren

Dit is in het kindscenario, en verzendt gegevens in de geselecteerde structuur naar het ouderscenario. U kunt deze gegevens in recentere modules in het ouderscenario in kaart brengen.

Als uw kindscenario veelvoudige routes heeft, adviseren wij toevoegend deze module aan een route die altijd loopt en na een andere route uitvoert.

De module Responder toevoegen configureren:

1. Als u een bestaande gegevensstructuur wilt gebruiken, selecteert u in het veld Gegevensstructuur de gegevensstructuur die wordt gebruikt voor de gegevens die het onderliggende scenario naar het bovenliggende scenario retourneert.

   of

   Om een nieuwe gegevensstructuur voor de gegevens tot stand te brengen, **voeg** naast het gebied van de gegevensstructuur toe en creeer de gegevensstructuur.

   Voor instructies bij het creëren van een gegevensstructuur, zie [ structuren van Gegevens ](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Klik **O.K.** om de module te bewaren.

