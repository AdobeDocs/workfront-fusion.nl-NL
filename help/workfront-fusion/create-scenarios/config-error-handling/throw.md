---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: errors
title: Workaround-fout genereren
description: In sommige gevallen kunt u de scenario-uitvoering die door Terugdraaiing of Vastleggingsfase wordt gevolgd forceren willen tegenhouden of de verwerking van een route ophouden en naar keuze het in de rij van Mening opslaan en onvolledige uitvoeringen in de Fusie van Adobe Workfront oplossen.
author: Becky
feature: Workfront Fusion
exl-id: 4bf2a6c7-16b2-4545-9adf-be3947a7017d
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# Oplossing voor een fout configureren `throw`

In sommige gevallen, kunt u de scenario-uitvoering die door Terugdraaiing of Vastleggingsfase wordt gevolgd forceren willen tegenhouden, of de verwerking van een route ophouden en naar keuze het in de rij van onvolledige uitvoeringen opslaan.

Momenteel, kunnen de fout behandelende richtlijnen niet buiten het werkingsgebied van een foutenhandlerroute worden gebruikt, en Adobe Workfront Fusion biedt geen module aan die u zou toelaten om (werpen) fouten gemakkelijk voorwaardelijk te produceren.

U kunt de volgende tijdelijke oplossing gebruiken om de foutfunctionaliteit van `throw` na te bootsen.

Voor informatie over onvolledige uitvoeringen, zie [&#x200B; Mening en los onvolledige uitvoeringen in de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md) op.

Voor informatie over fout behandelende richtlijnen, zie [&#x200B; Richtlijnen voor fout behandeling in de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

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

+++

## Oplossing voor `throw`

Om een fout voorwaardelijk te werpen, kunt u een module vormen om het opzettelijk tijdens zijn verrichting te maken ontbreken. U kunt bijvoorbeeld de module [!UICONTROL JSON] > [!UICONTROL Parse JSON] gebruiken, die is geconfigureerd om optioneel een fout te genereren (`BundleValidationError` in dit geval):

![&#x200B; fout JSON &#x200B;](assets/json-parse-json.png)

Vervolgens kunt u een van de foutafhandelingsinstructies aan de foutafhandelingsroute koppelen:

* **Terugdraaiing**: Drijf de scenariouitvoering om de terugdraaifase te stoppen en uit te voeren.
* **begaat**: Dwing de scenario uitvoering om te stoppen en uit te voeren begaan fase.
* **negeert**: Stop de verwerking van een route.
* **Breek**: Stop de verwerking van een route en sla het in de rij van onvolledige uitvoeringenomslag op.

In het volgende voorbeeld wordt het gebruik van de instructie [!DNL Rollback] getoond:

![&#x200B; de richtlijn van het Terugschroeven van prijzen &#x200B;](assets/rollback-directive.png)
