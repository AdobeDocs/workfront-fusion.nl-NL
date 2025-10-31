---
title: Voeg een module aan een scenario toe
description: Dit artikel beschrijft het basisproces om een module aan een scenario toe te voegen.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Voeg een module aan een scenario toe

Een scenario bestaat uit een reeks modules die aangeven hoe gegevens binnen een app moeten worden getransformeerd of moeten worden overgebracht tussen apps en webservices. U bouwt een module door modules toe te voegen en te vormen.

Dit artikel beschrijft het basisproces om een module aan een scenario toe te voegen. Voor specifiekere instructies over manieren om een scenario toe te voegen, zie de andere artikelen onder [&#x200B; modules toevoegen: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

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

+++## Voeg de eerste module aan een scenario toe

De eerste module van een scenario is gewoonlijk een trekkermodule.

Voor meer informatie over trekkermodules, zie [&#x200B; modules van de Trekker &#x200B;](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) op het overzicht van de artikelmodule.

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Begin creërend een scenario door **te klikken creeer een nieuw scenario** in de hoger-juiste hoek van het scherm.

   De scenario redacteur opent, met een placeholder (vraagteken) module en de lijst van beschikbare schakelaars.

   ![&#x200B; Placeholder module &#x200B;](assets/placeholder-module.png)

1. Selecteer de schakelaar of de webhaak die dit scenario zal beginnen. U kunt de naam van de schakelaar in de onderzoeksbar van de lijst typen om de lijst te filtreren.
1. Configureer de module.

   Voor instructies bij het vormen van specifieke modules, zie het artikel voor de gekozen toepassingen, die in [&#x200B; worden vermeld de toepassingen van de Fusie en hun moduleverwijzingen: artikelindex &#x200B;](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Als u de eerste module uit een scenario hebt verwijderd en het wilt vervangen, klik placeholder (vraagteken) module om de lijst van schakelaars te openen.

## Een andere module aan een scenario toevoegen

1. Als u zich niet in de scenario-editor bevindt van het scenario waarin u een module wilt toevoegen, klikt u op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Om een module aan een andere module toe te voegen, houd over het juiste handvat van de module waardaarna u een module wilt toevoegen, dan klik **een andere module** toevoegen wanneer het verschijnt.

   De lijst van schakelaars opent, tonend om het even welke schakelaars die reeds in het scenario worden gebruikt.

1. (Facultatief) om een andere schakelaar te selecteren, **voeg een andere module** in de lijst toe, dan selecteer de schakelaar. U kunt de naam van de schakelaar in de onderzoeksbar van de lijst typen om de lijst te filtreren.
1. Configureer de module.

   Voor instructies bij het vormen van specifieke modules, zie het artikel voor de gekozen toepassingen, die in [&#x200B; worden vermeld de toepassingen van de Fusie en hun moduleverwijzingen: artikelindex &#x200B;](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Voeg een module tussen bestaande modules in een scenario in

1. Als u zich niet in de scenario-editor bevindt van het scenario waarin u een module wilt toevoegen, klikt u op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik op het stippelpad tussen de modules waarin u een module wilt invoegen.
1. In het menu dat verschijnt, voegt de uitgezochte **een module** toe.

De lijst van schakelaars opent, tonend om het even welke schakelaars die reeds in het scenario worden gebruikt.

1. (Facultatief) om een andere schakelaar te selecteren, **voeg een andere module** in de lijst toe, dan selecteer de schakelaar. U kunt de naam van de schakelaar in de onderzoeksbar van de lijst typen om de lijst te filtreren.
1. Configureer de module.

   Voor instructies bij het vormen van specifieke modules, zie het artikel voor de gekozen toepassingen, die in [&#x200B; worden vermeld de toepassingen van de Fusie en hun moduleverwijzingen: artikelindex &#x200B;](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Als u een koppeling naar een specifieke module wilt maken, voegt u `?moduleId=<module-id>` toe aan de URL bij de weergave van de volgende pagina&#39;s:
>
>* Scenario-bewerkingspagina (URL eindigt bij `/edit`)
>* Een specifieke uitvoering van een scène (URL eindigt in `/logs/<log-id>`)
>
>`<module-id>` verwijst naar het getal naast het modulelabel wanneer het scenario wordt weergegeven.
>
>Dit kan nuttig zijn wanneer het zuiveren scenario&#39;s of het kopiëren moduleconfiguratie.
