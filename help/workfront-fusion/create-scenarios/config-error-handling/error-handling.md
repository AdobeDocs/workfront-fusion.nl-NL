---
title: Foutafhandeling toevoegen
description: Wanneer de fouten tijdens de uitvoering van een scenario voorkomen, is het gewoonlijk omdat de dienst wegens een mislukking niet beschikbaar is, antwoordt de dienst met onverwachte gegevens, of de bevestiging van inputgegevens ontbreekt.
author: Becky
feature: Workfront Fusion
exl-id: 82ddaf73-ecf9-4fd6-8f8e-909351023c77
source-git-commit: d7072a2dca50bf47f20d1f25dba4d3fb819d3ddc
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---

# Foutafhandeling toevoegen

Fouten kunnen optreden tijdens de uitvoering van een scenario.

Er kan bijvoorbeeld een fout optreden omdat:

* Een service is niet beschikbaar vanwege een fout
* Een service reageert met onverwachte gegevens
* Validatie van invoergegevens mislukt
* Andere redenen

Als een module een fout tijdens de scenariouitvoering ontmoet, en er geen fout behandelende route in bijlage aan de module of zijn route is, voert de standaardfout behandelende logica uit.

Door een foutenmanager aan een module of een route toe te voegen, kunt u de standaardfout behandelende logica met uw vervangen. Adobe Workfront Fusion biedt vijf verschillende instructies die aan het einde van de fouthandlerroutes kunnen worden ingevoegd.

Voor meer informatie over standaardfout behandeling, zie [ de types van Fout ](/help/workfront-fusion/references/errors/error-processing.md).

Voor meer informatie over fout behandelende richtlijnen, zie [ Richtlijnen voor fout behandeling ](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

>[!NOTE]
>
>Workfront Fusion ondersteunt foutafhandeling op routeniveau, zodat u de logica voor foutafhandeling één keer per route kunt definiëren in plaats van fouthandlers aan elke afzonderlijke module te koppelen.
>Omdat de route-vlakke fout behandeling een meer scalable, verenigbare, en architecturaal schone manier is om fouten, vooral in geavanceerde, multi-tak automatisering te beheren, adviseren wij gebruikend route-vlakke foutenbehandeling als beste praktijken.

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

## Locatie en hiërarchie van fouthandlers

U kunt foutenmanagers aan individuele modules, of aan routers toevoegen.

Een fouthandler die aan een module is gekoppeld, activeert alleen fouten die tijdens de verwerking van die specifieke module zijn aangetroffen.

Een foutenmanager in bijlage aan een router brengt voor fouten teweeg die door om het even welke module op de route van die router worden ontmoet. Dit omvat fouten die op om het even welke kindroutes worden ontmoet die geen foutenmanager op hun eigen router hebben.

Fouten worden afgehandeld door de volgende hiërarchie:

1. Module
2. Router
3. Bovenliggende router
4. Standaardfoutafhandeling

>[!BEGINSHADEBOX]

### Voorbeeld

Overweeg het volgende voorbeeldscenario:

![ scenario dat van het Voorbeeld routes en foutenmanagers toont ](assets/error-handling-route-example-with-numbers.png)

1. Deze module heeft een fouthandler. Om het even welke fout op deze module wordt behandeld door de Commit richtlijn.
1. Deze module heeft geen fouthandler. Als deze module een fout ontmoet, wordt de fout behandeld door de manager op de router die de route van de module creeerde. Om het even welke fout op deze module wordt behandeld door de richtlijn van het Terugschroeven van prijzen.
1. Deze module heeft geen foutenmanager, noch heeft de router die de route van de module creeerde, maar er is een foutenmanager op de volgende router omhoog. Om het even welke fout op deze module wordt behandeld door de richtlijn van het Break.

>[!NOTE]
>
>* Als een module geen foutenmanager op de module, zijn router, of om het even welke ouderrouters heeft, worden om het even welke fouten op die module behandeld door standaardfout behandeling.
>* Om een globale foutenmanager tot stand te brengen, creeer een router dichtbij het begin van uw scenario en maak fout behandeling aan die router vast.


>[!ENDSHADEBOX]

## Een fouthandler toevoegen

U kunt een foutenmanager aan een module of aan een router toevoegen.

* [Een fouthandler toevoegen aan een module](#add-an-error-handler-to-a-module)
* [Voeg een foutenmanager aan een router toe](#add-an-error-handler-to-a-router)

### Een fouthandler toevoegen aan een module

Om een foutenmanager aan een module toe te voegen:

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u een fout behandelende route wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik met de rechtermuisknop op de module waarna u een fouthandlerroute wilt toevoegen en selecteer **[!UICONTROL Add error handler]** :

   ![ de managerroute van de Fout ](assets/error-handler-route.png)

   Een route van de foutenmanager wordt toegevoegd aan de module. Als de module de laatste module in een route is, volgt de foutenmanager direct de module. Als de module meer modules na het heeft, wordt een afzonderlijke route van de foutenmanager toegevoegd.

   In de module voor foutafhandeling ziet u een lijst met richtlijnen en de toepassingen die in uw scenario worden gebruikt.

   ![ route van de Fout ](assets/error-route.png)

1. Selecteer een van de instructies.

   of

   Voeg één of meerdere modules aan de route van de foutenmanager toe.

   Als u meer modules aan de route toevoegt, wordt de Ignore richtlijn toegepast door gebrek. Als er een fout is, worden de verdere modules op die route verwerkt.

   Voor meer informatie over richtlijnen, zie [ Fout behandelende richtlijnen ](#error-handling-directives) in dit artikel.

1. (Optioneel) Voeg een filter toe aan de foutafhandelingsroute. Voor instructies, zie [ het filtreren en het nestelen aan fout behandelende routes ](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md) toevoegen.

>[!NOTE]
>
>Merk op dat een route van de foutenmanager uit transparante cirkels bestaat, terwijl een regelmatige route uit stevige cirkels bestaat.

### Voeg een foutenmanager aan een router toe

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u een fout behandelende route wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik met de rechtermuisknop op de router waar u een fouthandlerroute wilt toevoegen en selecteer **[!UICONTROL Add error handler]** :

   ![ de managerroute van de Fout ](assets/error-handler-on-router.png)

   Een route van de foutenmanager wordt toegevoegd aan de router.

   In de module voor foutafhandeling ziet u een lijst met richtlijnen en de toepassingen die in uw scenario worden gebruikt.

   ![ route van de Fout ](assets/error-handler-route-from-router.png)

1. Selecteer een van de instructies.

   of

   Voeg één of meerdere modules aan de route van de foutenmanager toe.

   Als u meer modules aan de route toevoegt, wordt de Ignore richtlijn toegepast door gebrek. Als er een fout is, worden de verdere modules op die route verwerkt.

   Voor meer informatie over richtlijnen, zie [ Fout behandelende richtlijnen ](#error-handling-directives) in dit artikel.

1. (Optioneel) Voeg een filter toe aan de foutafhandelingsroute. Voor instructies, zie [ het filtreren en het nestelen aan fout behandelende routes ](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md) toevoegen.

## Instructies voor foutafhandeling

De richtlijnen worden hieronder kort toegelicht. Voor meer informatie, zie [ Richtlijnen voor fout behandeling ](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

Er zijn vijf richtlijnen, die in de volgende categorieën kunnen worden gegroepeerd gebaseerd op of een scenario uitvoering na de fout voortgaat.

De volgende richtlijnen zorgen ervoor dat de uitvoering van een scenario wordt voortgezet:

* **[!UICONTROL Resume]**: Hiermee kunt u een vervangende uitvoer voor de module opgeven met de fout. De status van de uitvoering van het scenario is gemarkeerd als geslaagd.
* **[!UICONTROL Ignore]** : negeert de fout. De status van de uitvoering van het scenario is gemarkeerd als geslaagd.
* **[!UICONTROL Break]**: slaat de invoer in de wachtrij van onvolledige uitvoeringen op. De status van de uitvoering van het scenario wordt gemarkeerd als waarschuwing.

  Voor meer informatie, zie [ Mening en los onvolledige uitvoeringen ](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md) op.

Als de uitvoering van een scenario moet stoppen wanneer een fout optreedt, gebruikt u een van de volgende instructies:

* **[!UICONTROL Rollback]**: stopt de uitvoering van het scenario onmiddellijk en markeert de status als fout.
* **[!UICONTROL Commit]**: stopt de uitvoering van het scenario onmiddellijk en markeert de status als geslaagd.

## Bronnen

Zie voor meer informatie over foutafhandeling:

* [Richtlijnen voor foutafhandeling in Adobe Workfront Fusion](/help/workfront-fusion/references/errors/directives-for-error-handling.md)
* [Filteren en nesten toevoegen aan foutafhandelingsroutes](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md)
