---
content-type: reference
title: Richtlijnen voor foutafhandeling
description: Dit artikel beschrijft richtlijnen die u voor fout behandeling in uw  [!DNL Adobe Workfront Fusion]  scenario's kunt gebruiken.
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Richtlijnen voor foutafhandeling

Met instructies voor foutafhandeling kunt u kiezen wat er gebeurt wanneer er een fout optreedt.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie</td> 
   <td> Nieuw: Standaard<p>of</p><p>Huidig: Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licentie</td> 
   <td>
   <p>Huidig: Geen [!DNL Workfront Fusion] vereiste licentie.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] [!DNL Workfront] -abonnement: uw organisatie moet het abonnement aanschaffen [!DNL Adobe Workfront Fusion] .</li><li>[!UICONTROL Ultimate] [!DNL Workfront] abonnement: [!DNL Workfront Fusion] is opgenomen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet [!DNL Adobe Workfront Fusion] aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>


Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Richtlijnen voor foutafhandeling

De volgende instructies voor foutafhandeling zijn beschikbaar in Workfront Fusion.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Terugdraaien</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>De uitvoering van het scenario wordt onmiddellijk gestopt.</li><li>Een terugdraaifase is begonnen op alle modules, in een poging om hen allen aan hun aanvankelijke staat terug te keren. </li><li>Latere modules worden niet verwerkt.</p></li><li> <p>In de meeste gevallen wordt het scenario gedeactiveerd na het aantal opeenvolgende fouten dat is opgegeven onder Scenario-instellingen. Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors" class="MCXref xref"> Aantal opeenvolgende fouten </a>.</p> </li><li><p>De status van de uitvoering van het scenario is gemarkeerd als "Fout."</p></li></ul> <p><b> Nota </b>: Dit is het standaardgedrag als geen route van de foutenmanager aan de module in bijlage is en <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions" class="MCXref xref"> toestaat het opslaan van onvolledige uitvoeringen </a> toestaat het opslaan van onvolledige uitvoeringen die onder [!UICONTROL Scenario settings] plaatsen wordt niet gecontroleerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Vastleggen</p> <p> <img src="assets/commit.png"> </p> </td> 
   <td> <ul><li><p>De uitvoering van het scenario wordt onmiddellijk gestopt.</li><li>Een fase Vastleggen is begonnen op alle modules. </li><li>Latere modules worden niet verwerkt.</p></li><li> <p>Alle onverwerkte bundels worden genegeerd.</p> </li><li><p>De status van de uitvoering van het scenario is gemarkeerd als "succes." </p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Hervatten</p> <p> <img src="assets/resume.png"> </p> </td> 
   <td> <ul><li><p>Er wordt een vervangend uitvoerbestand opgegeven en geleverd aan de module die een fout aantreft.</p> </li><li><p>Vervolgens worden modules verwerkt.</p></li><li> <p>De status van de uitvoering van het scenario is gemarkeerd als "succes."</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Negeren</p> <p> <img src="assets/ignore.png"> </p> </td> 
   <td><ul><li> <p>De fout wordt genegeerd.</li><li> Latere modules worden niet verwerkt.</p> </li><li><p>Als er onverwerkte bundels zijn, gaat de uitvoering van het scenario normaal voort.</p> </li><li><p>De status van de uitvoering van het scenario is gemarkeerd als "succes."</p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Break</p> <p> <img src="assets/break.png"> </p> </td> 
   <td><ul><li> <p>De status van de uitvoering van het scenario wordt opgeslagen in de wachtrij met onvolledige uitvoeringen waar de fout handmatig kan worden opgelost. Voor meer informatie, zie <a href="/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref"> Mening en los onvolledige uitvoeringen </a> op.</p> <p>Er zijn echter enkele uitzonderingen. Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow" class="MCXref xref"> toestaan het opslaan van onvolledige uitvoeringen </a> in artikel vormt scenario montages </a>.</p></li><li> <p>Latere modules worden niet verwerkt.</p></li><li> <p>Als er onverwerkte bundels zijn, gaat de uitvoering van het scenario normaal voort.</p> </li><li><p>De status van de uitvoering van het scenario wordt gemarkeerd als "waarschuwing" wanneer de optie [!UICONTROL Automatically complete execution] is uitgeschakeld.</p></li></ul> <p>Zie de sectie <a href="#break" class="MCXref xref">[!UICONTROL Break]</a> in dit artikel voor meer informatie</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Opnieuw</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>In sommige gevallen kan het nuttig zijn om een falende module opnieuw uit te voeren wanneer er een kans is dat de reden voor de mislukking over tijd zou kunnen overgaan.</p> <p>Workfront Fusion biedt momenteel niet de instructie Retry, maar er kunnen verschillende oplossingen worden gebruikt om de functionaliteit ervan na te bootsen. Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/config-error-handling/retry.md" class="MCXref xref"> fout behandeling </a> opnieuw proberen.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Instructies voor foutafhandeling kunnen niet worden gebruikt buiten een foutafhandelingsroute.
>* [!DNL Workfront Fusion] biedt momenteel geen module Throw die u in staat zou stellen om gemakkelijk voorwaardelijke fouten te genereren (genereren), hoewel een tijdelijke oplossing kan worden gebruikt om de functionaliteit ervan na te bootsen.
>
>  Voor meer informatie, zie [ `throw` foutenwerkaround ](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md) vormen.

## Bronnen

* Voor informatie bij het terugschroeven van prijzen en de fase van het Terugschroeven van prijzen, zie [ Terugdraaiing ](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) in de uitvoering van het artikelScenario, cycli, en fasen.
* Voor informatie over de fase van het Vastleggen, zie [ Vastleggen ](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit) in de uitvoering van het artikelScenario, cycli, en fasen.
