---
content-type: reference
title: Richtlijnen voor foutafhandeling
description: In dit artikel worden instructies beschreven die u kunt gebruiken voor foutafhandeling in uw Adobe Workfront Fusion-scenario's.
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
source-git-commit: 99621f57da1eb294834a0eacfe527dcf017408e9
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Richtlijnen voor foutafhandeling

Met instructies voor foutafhandeling kunt u kiezen wat er gebeurt wanneer er een fout optreedt.

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++## Richtlijnen voor foutafhandeling

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
>* Workfront Fusion biedt momenteel geen Throw-module waarmee u gemakkelijk voorwaardelijk fouten kunt genereren (genereren), hoewel een tijdelijke oplossing kan worden gebruikt om de functionaliteit ervan na te bootsen.
>
>  Voor meer informatie, zie [&#x200B; `throw` foutenwerkaround &#x200B;](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md) vormen.

## Bronnen

* Voor informatie bij het terugschroeven van prijzen en de fase van het Terugschroeven van prijzen, zie [&#x200B; Terugdraaiing &#x200B;](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) in de uitvoering van het artikelScenario, cycli, en fasen.
* Voor informatie over de fase van het Vastleggen, zie [&#x200B; Vastleggen &#x200B;](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit) in de uitvoering van het artikelScenario, cycli, en fasen.
